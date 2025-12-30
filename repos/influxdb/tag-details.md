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
$ docker pull influxdb@sha256:532bb4f29eee869458f977d5b37cff52cde4fa83e7c3d94ee2f02d942f230f7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:00d481ea7045e6a951ff09d4d4fbb1d625f0571a8e0a4f4c6f09afb4a941052d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116168236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d8a73b4bf7947216fc1547d554ad6ee3d8641ee6a368f2ef92789277d0ab26`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:07 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 30 Dec 2025 01:32:03 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 30 Dec 2025 01:32:03 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:32:03 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Dec 2025 01:32:03 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Dec 2025 01:32:03 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:32:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:32:03 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Dec 2025 01:32:03 GMT
USER influxdb
# Tue, 30 Dec 2025 01:32:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:32:03 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e965e3d3ec6a91dec80966c8b4a3628f30528e45c9298fd7332b692e3638e6b`  
		Last Modified: Tue, 30 Dec 2025 01:31:35 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990ed7842c51cf9e672613372196f48552cd91b5831862d3964006b4d9de77fd`  
		Last Modified: Tue, 30 Dec 2025 01:32:25 GMT  
		Size: 43.7 MB (43655186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a2bd3e973e02e4b9aa596b501545e20225489b8cf555a2999c2c31bc73559e`  
		Last Modified: Tue, 30 Dec 2025 01:32:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b3bec654a54de7eadf0b3ae38f80a32f2d961e45d521cf9459ce490656be90`  
		Last Modified: Tue, 30 Dec 2025 01:32:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e2451c73b1a0ae73b8b13576c4b97ccf9e24654320fa9aa90645c78a37802c`  
		Last Modified: Tue, 30 Dec 2025 01:32:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:be4ffb4f74fbe68b5988d25725056a3207aea2f436827de686744bc616192ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0118856354bc1c71f9ab344f495a8377e021c74a5405396eac5714f8403cee`

```dockerfile
```

-	Layers:
	-	`sha256:55cb7f2eb746364c9b55abb2241de6a328d8b3cb5437c8d8c2c688893eb78e31`  
		Last Modified: Tue, 30 Dec 2025 06:20:31 GMT  
		Size: 5.1 MB (5078620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cfc9e57fe0a200b32a10e77d6be93bac58e88509408174d3d2f5627c4991c24`  
		Last Modified: Tue, 30 Dec 2025 06:20:32 GMT  
		Size: 15.5 KB (15486 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0590da3c09adca7935e1153736422c0eb9d058ef102f851d86631126310d446b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113079194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9346b0aef6ea301c58b687538fe426d297fcd9823075ea8d3e0fdcc7cd6f21da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:33:09 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 30 Dec 2025 01:33:57 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 30 Dec 2025 01:33:57 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:33:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Dec 2025 01:33:57 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Dec 2025 01:33:57 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:33:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:33:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Dec 2025 01:33:57 GMT
USER influxdb
# Tue, 30 Dec 2025 01:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:33:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0015662db9fbc9a53df2aca9a165229a6d8ad3d25c43f8ed173940dd3aa9e5af`  
		Last Modified: Tue, 30 Dec 2025 02:30:00 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843639ff00c9b3c8376d917944323b00bdd66cf9cf6d9931918633ea06e41e7a`  
		Last Modified: Tue, 30 Dec 2025 01:34:21 GMT  
		Size: 41.1 MB (41118752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2480fd899fdaa65b1559c75e34aa898aef99fc897cc15eb1795722cf07bcade9`  
		Last Modified: Tue, 30 Dec 2025 01:34:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbaaa638d8afb93bd1734d69e709ecc6030b3e4de2b148448b0823d5173e6d0`  
		Last Modified: Tue, 30 Dec 2025 01:34:17 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e46cba3bf0701ec48941930813e903bcfd2800c6de08696f835260a7dd0fe13`  
		Last Modified: Tue, 30 Dec 2025 01:34:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:4aadd344427f7c25de6764bb3e8c000bedbf03a9701828aafad34b4244b8704f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db3517c9fe6c57752745297ef69c5a9db389bb1c2c75db2cc1f3c036bcaeed0`

```dockerfile
```

-	Layers:
	-	`sha256:4fd99f291923c911952352c04b822e58d8df32f391a25e0b1fcd1095ff1bee1a`  
		Last Modified: Tue, 30 Dec 2025 06:20:37 GMT  
		Size: 5.1 MB (5078085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a211873935ff197424e03169d59665cb42c181faad7255450f9d2cff73216e`  
		Last Modified: Tue, 30 Dec 2025 06:20:37 GMT  
		Size: 15.6 KB (15579 bytes)  
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
		Last Modified: Mon, 08 Dec 2025 00:30:58 GMT  
		Size: 38.1 MB (38069965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd812bdffaf5a51fdc5ad2690ccb55dec4a092395243bf366e01cf45511ac7`  
		Last Modified: Mon, 08 Dec 2025 04:15:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccae7d91ef8bb0ea37a95450db36eaa796c974b09f7a0589106acf87072085a`  
		Last Modified: Mon, 08 Dec 2025 00:30:56 GMT  
		Size: 1.0 KB (1004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce755337386479f3084609d415719dae3d4f17e49deeb6a099a77ddeca8e2cb`  
		Last Modified: Mon, 08 Dec 2025 00:30:56 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e2d3d495f76618c744d89e0710cd06db610e65e6019e022899e6a4de4fc2e2`  
		Last Modified: Mon, 08 Dec 2025 00:30:57 GMT  
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
		Last Modified: Mon, 08 Dec 2025 14:34:39 GMT  
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
		Last Modified: Sun, 07 Dec 2025 13:54:57 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f28be0243b3bb965b6c9b2e07c70b019eb69070fb075e2cc8660b856e4efba`  
		Last Modified: Sun, 07 Dec 2025 22:15:36 GMT  
		Size: 1.3 MB (1304645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f38f6a643f7a256b8eaf81222d2fb2520d2be7423f755c8fa2624e6324abf87`  
		Last Modified: Sun, 07 Dec 2025 22:15:39 GMT  
		Size: 35.5 MB (35545508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbc3962e590201f79eb734b9201590ddc739436a716accc9e14fb795530a3aa`  
		Last Modified: Sun, 07 Dec 2025 22:15:38 GMT  
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
		Last Modified: Sun, 07 Dec 2025 22:15:40 GMT  
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
$ docker pull influxdb@sha256:552cc47796ffc3ea48c8beb8ec72df9c3d88a44364c4b061be9a6e49049643b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f2d873b560f91a4844865b9ec46d1696a2a9a15644617817ff4337199b5f3f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114681045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd34c12e1524ec5270786b553ed03f23e5ddf2e99b024ea2682674b565007a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:32:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 01:32:13 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 30 Dec 2025 01:32:13 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 30 Dec 2025 01:32:13 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Dec 2025 01:32:13 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Dec 2025 01:32:13 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:32:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:32:13 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Dec 2025 01:32:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:32:13 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b731bb16c7594c6bd8bcbe629f567a72ae19818f34036bc888aeca106b751c`  
		Last Modified: Tue, 30 Dec 2025 01:32:33 GMT  
		Size: 3.4 KB (3443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7f62550878765215dfd8d75feddcdd6a133edbacadbee609a808dc3572ffde`  
		Last Modified: Tue, 30 Dec 2025 01:32:37 GMT  
		Size: 42.2 MB (42165687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bb9e84b651b37de8ef2686f0d9f8f572ac62967604a412befdcffcdff7d516`  
		Last Modified: Tue, 30 Dec 2025 01:32:33 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50019ea5bd0db215773ef81136787324b9d3ec0d04c59ee348c2f75760cf1022`  
		Last Modified: Tue, 30 Dec 2025 01:32:33 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f6be1825b865f5bbc901d1ac0936a31bf534d0ec2ee48b1baa5fdbe277279`  
		Last Modified: Tue, 30 Dec 2025 01:32:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:45df8736cd4b0f88d187b16f8ba28fbd286577118f840f775cace9c173662fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4698428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63dcdcb1b2ba869321af21747ecb550469f508adb520cd0b70c76552f9f6c22`

```dockerfile
```

-	Layers:
	-	`sha256:5505bd99e439de34aea8ef55dc6168fa642740b43f7601b8fe4d0714773ed2f7`  
		Last Modified: Tue, 30 Dec 2025 06:20:38 GMT  
		Size: 4.7 MB (4683763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1b853aa8423a72284ce6815334411c2d449be444775f077966e6da7f9706a3`  
		Last Modified: Tue, 30 Dec 2025 06:20:38 GMT  
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
		Last Modified: Tue, 09 Dec 2025 22:39:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b114d197f0b29a6932d8b9d445b0628a19b4157668f6eb76571600ecaf25723`  
		Last Modified: Mon, 15 Dec 2025 20:40:19 GMT  
		Size: 1.2 MB (1224592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3358124fd2820053c690bcf986afef42d2564531fcff8ba0b814614bc23b3bbe`  
		Last Modified: Mon, 15 Dec 2025 20:40:22 GMT  
		Size: 42.1 MB (42105919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d4466a6a2e285d8482d3dce7c47f8f5a2bbdf6c366916cfb45ea2790337a9`  
		Last Modified: Mon, 15 Dec 2025 20:40:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e120ca154a1d12d672fecfc7212adcc4973d001dce2328028c3ab256b7f20b9`  
		Last Modified: Tue, 09 Dec 2025 22:39:05 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a0d8b4e8d0cf5b5a88b2dc5d203d42a530f015d833f41790286c1098b9be04`  
		Last Modified: Tue, 09 Dec 2025 22:39:04 GMT  
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
		Last Modified: Mon, 15 Dec 2025 20:40:19 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:36fe9af0202113412287271033c8032648c941a5c3f6c1bcfb13d4b5ef2746f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:136a7f0bd384f8d5dc616c10c1c36c7f490d8826d176b6f24c37ce6455ebf6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91110271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:260c30150fd0ab76b0ed7bbd4830e3669773b5490490cb5b9646f83817289bc9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:32:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 01:32:34 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 30 Dec 2025 01:32:34 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 30 Dec 2025 01:32:34 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Dec 2025 01:32:34 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Dec 2025 01:32:34 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:32:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:32:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:32:34 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f60211d18e403bf2feb092ec2e2eecf7c24ecd4f98182ebb56dac2b0cb3c17c`  
		Last Modified: Tue, 30 Dec 2025 01:32:49 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4dde773a3e3e187d2b5653bf3c946227ceaa42e64b198f0e1e3af94a4bfe4d`  
		Last Modified: Tue, 30 Dec 2025 01:32:54 GMT  
		Size: 18.6 MB (18596114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9267ac8b05957039f87d5012eaa2463a7f90e0edb6590acaf7c7d276518bb97f`  
		Last Modified: Tue, 30 Dec 2025 01:32:49 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3e1d329a8efd802d1cff59aa47999eee8a71387311fdedd356e8ed8dfe01aa`  
		Last Modified: Tue, 30 Dec 2025 01:32:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:f362bafcca6dbb102af650b4c8cd35d9ded2f39ce9be3fa925ee5d13eff3aa3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4603630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7c61849b5dd5b2d298d609a7b281cf0b4cbe5277e3057aa141212d916f7a05`

```dockerfile
```

-	Layers:
	-	`sha256:b272a01eb684c1ef2c1de6cb2f48659a38a95eba5c5e665649726e8ae80ddd5a`  
		Last Modified: Tue, 30 Dec 2025 06:20:43 GMT  
		Size: 4.6 MB (4590606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:011794fa649be9a259e677a85c62eb40261f1a748200d8e30546198fdde42af4`  
		Last Modified: Tue, 30 Dec 2025 06:20:44 GMT  
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
		Last Modified: Tue, 09 Dec 2025 23:02:45 GMT  
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
		Last Modified: Mon, 15 Dec 2025 19:26:02 GMT  
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
		Last Modified: Mon, 15 Dec 2025 19:26:02 GMT  
		Size: 676.6 KB (676622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24dde11f34792d696d7baefa980d47a9bb0ec06c1640475e5f37e93aa05a49ae`  
		Last Modified: Mon, 15 Dec 2025 19:26:01 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8`

```console
$ docker pull influxdb@sha256:532bb4f29eee869458f977d5b37cff52cde4fa83e7c3d94ee2f02d942f230f7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:00d481ea7045e6a951ff09d4d4fbb1d625f0571a8e0a4f4c6f09afb4a941052d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116168236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d8a73b4bf7947216fc1547d554ad6ee3d8641ee6a368f2ef92789277d0ab26`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:07 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 30 Dec 2025 01:32:03 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 30 Dec 2025 01:32:03 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:32:03 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Dec 2025 01:32:03 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Dec 2025 01:32:03 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:32:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:32:03 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Dec 2025 01:32:03 GMT
USER influxdb
# Tue, 30 Dec 2025 01:32:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:32:03 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e965e3d3ec6a91dec80966c8b4a3628f30528e45c9298fd7332b692e3638e6b`  
		Last Modified: Tue, 30 Dec 2025 01:31:35 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990ed7842c51cf9e672613372196f48552cd91b5831862d3964006b4d9de77fd`  
		Last Modified: Tue, 30 Dec 2025 01:32:25 GMT  
		Size: 43.7 MB (43655186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a2bd3e973e02e4b9aa596b501545e20225489b8cf555a2999c2c31bc73559e`  
		Last Modified: Tue, 30 Dec 2025 01:32:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b3bec654a54de7eadf0b3ae38f80a32f2d961e45d521cf9459ce490656be90`  
		Last Modified: Tue, 30 Dec 2025 01:32:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e2451c73b1a0ae73b8b13576c4b97ccf9e24654320fa9aa90645c78a37802c`  
		Last Modified: Tue, 30 Dec 2025 01:32:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:be4ffb4f74fbe68b5988d25725056a3207aea2f436827de686744bc616192ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0118856354bc1c71f9ab344f495a8377e021c74a5405396eac5714f8403cee`

```dockerfile
```

-	Layers:
	-	`sha256:55cb7f2eb746364c9b55abb2241de6a328d8b3cb5437c8d8c2c688893eb78e31`  
		Last Modified: Tue, 30 Dec 2025 06:20:31 GMT  
		Size: 5.1 MB (5078620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cfc9e57fe0a200b32a10e77d6be93bac58e88509408174d3d2f5627c4991c24`  
		Last Modified: Tue, 30 Dec 2025 06:20:32 GMT  
		Size: 15.5 KB (15486 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0590da3c09adca7935e1153736422c0eb9d058ef102f851d86631126310d446b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113079194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9346b0aef6ea301c58b687538fe426d297fcd9823075ea8d3e0fdcc7cd6f21da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:33:09 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 30 Dec 2025 01:33:57 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 30 Dec 2025 01:33:57 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:33:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Dec 2025 01:33:57 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Dec 2025 01:33:57 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:33:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:33:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Dec 2025 01:33:57 GMT
USER influxdb
# Tue, 30 Dec 2025 01:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:33:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0015662db9fbc9a53df2aca9a165229a6d8ad3d25c43f8ed173940dd3aa9e5af`  
		Last Modified: Tue, 30 Dec 2025 02:30:00 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843639ff00c9b3c8376d917944323b00bdd66cf9cf6d9931918633ea06e41e7a`  
		Last Modified: Tue, 30 Dec 2025 01:34:21 GMT  
		Size: 41.1 MB (41118752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2480fd899fdaa65b1559c75e34aa898aef99fc897cc15eb1795722cf07bcade9`  
		Last Modified: Tue, 30 Dec 2025 01:34:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbaaa638d8afb93bd1734d69e709ecc6030b3e4de2b148448b0823d5173e6d0`  
		Last Modified: Tue, 30 Dec 2025 01:34:17 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e46cba3bf0701ec48941930813e903bcfd2800c6de08696f835260a7dd0fe13`  
		Last Modified: Tue, 30 Dec 2025 01:34:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:4aadd344427f7c25de6764bb3e8c000bedbf03a9701828aafad34b4244b8704f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db3517c9fe6c57752745297ef69c5a9db389bb1c2c75db2cc1f3c036bcaeed0`

```dockerfile
```

-	Layers:
	-	`sha256:4fd99f291923c911952352c04b822e58d8df32f391a25e0b1fcd1095ff1bee1a`  
		Last Modified: Tue, 30 Dec 2025 06:20:37 GMT  
		Size: 5.1 MB (5078085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a211873935ff197424e03169d59665cb42c181faad7255450f9d2cff73216e`  
		Last Modified: Tue, 30 Dec 2025 06:20:37 GMT  
		Size: 15.6 KB (15579 bytes)  
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
		Last Modified: Mon, 08 Dec 2025 00:30:58 GMT  
		Size: 38.1 MB (38069965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd812bdffaf5a51fdc5ad2690ccb55dec4a092395243bf366e01cf45511ac7`  
		Last Modified: Mon, 08 Dec 2025 04:15:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccae7d91ef8bb0ea37a95450db36eaa796c974b09f7a0589106acf87072085a`  
		Last Modified: Mon, 08 Dec 2025 00:30:56 GMT  
		Size: 1.0 KB (1004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce755337386479f3084609d415719dae3d4f17e49deeb6a099a77ddeca8e2cb`  
		Last Modified: Mon, 08 Dec 2025 00:30:56 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e2d3d495f76618c744d89e0710cd06db610e65e6019e022899e6a4de4fc2e2`  
		Last Modified: Mon, 08 Dec 2025 00:30:57 GMT  
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
		Last Modified: Mon, 08 Dec 2025 14:34:39 GMT  
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
		Last Modified: Sun, 07 Dec 2025 13:54:57 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f28be0243b3bb965b6c9b2e07c70b019eb69070fb075e2cc8660b856e4efba`  
		Last Modified: Sun, 07 Dec 2025 22:15:36 GMT  
		Size: 1.3 MB (1304645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f38f6a643f7a256b8eaf81222d2fb2520d2be7423f755c8fa2624e6324abf87`  
		Last Modified: Sun, 07 Dec 2025 22:15:39 GMT  
		Size: 35.5 MB (35545508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbc3962e590201f79eb734b9201590ddc739436a716accc9e14fb795530a3aa`  
		Last Modified: Sun, 07 Dec 2025 22:15:38 GMT  
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
		Last Modified: Sun, 07 Dec 2025 22:15:40 GMT  
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
$ docker pull influxdb@sha256:552cc47796ffc3ea48c8beb8ec72df9c3d88a44364c4b061be9a6e49049643b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f2d873b560f91a4844865b9ec46d1696a2a9a15644617817ff4337199b5f3f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114681045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd34c12e1524ec5270786b553ed03f23e5ddf2e99b024ea2682674b565007a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:32:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 01:32:13 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 30 Dec 2025 01:32:13 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 30 Dec 2025 01:32:13 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Dec 2025 01:32:13 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Dec 2025 01:32:13 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:32:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:32:13 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Dec 2025 01:32:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:32:13 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b731bb16c7594c6bd8bcbe629f567a72ae19818f34036bc888aeca106b751c`  
		Last Modified: Tue, 30 Dec 2025 01:32:33 GMT  
		Size: 3.4 KB (3443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7f62550878765215dfd8d75feddcdd6a133edbacadbee609a808dc3572ffde`  
		Last Modified: Tue, 30 Dec 2025 01:32:37 GMT  
		Size: 42.2 MB (42165687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bb9e84b651b37de8ef2686f0d9f8f572ac62967604a412befdcffcdff7d516`  
		Last Modified: Tue, 30 Dec 2025 01:32:33 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50019ea5bd0db215773ef81136787324b9d3ec0d04c59ee348c2f75760cf1022`  
		Last Modified: Tue, 30 Dec 2025 01:32:33 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f6be1825b865f5bbc901d1ac0936a31bf534d0ec2ee48b1baa5fdbe277279`  
		Last Modified: Tue, 30 Dec 2025 01:32:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:45df8736cd4b0f88d187b16f8ba28fbd286577118f840f775cace9c173662fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4698428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63dcdcb1b2ba869321af21747ecb550469f508adb520cd0b70c76552f9f6c22`

```dockerfile
```

-	Layers:
	-	`sha256:5505bd99e439de34aea8ef55dc6168fa642740b43f7601b8fe4d0714773ed2f7`  
		Last Modified: Tue, 30 Dec 2025 06:20:38 GMT  
		Size: 4.7 MB (4683763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1b853aa8423a72284ce6815334411c2d449be444775f077966e6da7f9706a3`  
		Last Modified: Tue, 30 Dec 2025 06:20:38 GMT  
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
		Last Modified: Tue, 09 Dec 2025 22:39:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b114d197f0b29a6932d8b9d445b0628a19b4157668f6eb76571600ecaf25723`  
		Last Modified: Mon, 15 Dec 2025 20:40:19 GMT  
		Size: 1.2 MB (1224592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3358124fd2820053c690bcf986afef42d2564531fcff8ba0b814614bc23b3bbe`  
		Last Modified: Mon, 15 Dec 2025 20:40:22 GMT  
		Size: 42.1 MB (42105919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d4466a6a2e285d8482d3dce7c47f8f5a2bbdf6c366916cfb45ea2790337a9`  
		Last Modified: Mon, 15 Dec 2025 20:40:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e120ca154a1d12d672fecfc7212adcc4973d001dce2328028c3ab256b7f20b9`  
		Last Modified: Tue, 09 Dec 2025 22:39:05 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a0d8b4e8d0cf5b5a88b2dc5d203d42a530f015d833f41790286c1098b9be04`  
		Last Modified: Tue, 09 Dec 2025 22:39:04 GMT  
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
		Last Modified: Mon, 15 Dec 2025 20:40:19 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-meta`

```console
$ docker pull influxdb@sha256:36fe9af0202113412287271033c8032648c941a5c3f6c1bcfb13d4b5ef2746f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:136a7f0bd384f8d5dc616c10c1c36c7f490d8826d176b6f24c37ce6455ebf6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91110271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:260c30150fd0ab76b0ed7bbd4830e3669773b5490490cb5b9646f83817289bc9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:32:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 01:32:34 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 30 Dec 2025 01:32:34 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 30 Dec 2025 01:32:34 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Dec 2025 01:32:34 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Dec 2025 01:32:34 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:32:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:32:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:32:34 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f60211d18e403bf2feb092ec2e2eecf7c24ecd4f98182ebb56dac2b0cb3c17c`  
		Last Modified: Tue, 30 Dec 2025 01:32:49 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4dde773a3e3e187d2b5653bf3c946227ceaa42e64b198f0e1e3af94a4bfe4d`  
		Last Modified: Tue, 30 Dec 2025 01:32:54 GMT  
		Size: 18.6 MB (18596114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9267ac8b05957039f87d5012eaa2463a7f90e0edb6590acaf7c7d276518bb97f`  
		Last Modified: Tue, 30 Dec 2025 01:32:49 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3e1d329a8efd802d1cff59aa47999eee8a71387311fdedd356e8ed8dfe01aa`  
		Last Modified: Tue, 30 Dec 2025 01:32:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:f362bafcca6dbb102af650b4c8cd35d9ded2f39ce9be3fa925ee5d13eff3aa3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4603630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7c61849b5dd5b2d298d609a7b281cf0b4cbe5277e3057aa141212d916f7a05`

```dockerfile
```

-	Layers:
	-	`sha256:b272a01eb684c1ef2c1de6cb2f48659a38a95eba5c5e665649726e8ae80ddd5a`  
		Last Modified: Tue, 30 Dec 2025 06:20:43 GMT  
		Size: 4.6 MB (4590606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:011794fa649be9a259e677a85c62eb40261f1a748200d8e30546198fdde42af4`  
		Last Modified: Tue, 30 Dec 2025 06:20:44 GMT  
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
		Last Modified: Tue, 09 Dec 2025 23:02:45 GMT  
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
		Last Modified: Mon, 15 Dec 2025 19:26:02 GMT  
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
		Last Modified: Mon, 15 Dec 2025 19:26:02 GMT  
		Size: 676.6 KB (676622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24dde11f34792d696d7baefa980d47a9bb0ec06c1640475e5f37e93aa05a49ae`  
		Last Modified: Mon, 15 Dec 2025 19:26:01 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12`

```console
$ docker pull influxdb@sha256:db03b9c599588cd5caded6df8b8258841017bf186898c6133a4f99b4d6134395
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12` - linux; amd64

```console
$ docker pull influxdb@sha256:cc56fcc9a34e680b598a0872774c5e7eb804dafac7a1c18b6ef046f8f84322f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113843346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ab37e2f191a8e5edb169032e41f231436981ff1d892d26c55b98a8551cb3f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:07 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 30 Dec 2025 01:31:11 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 30 Dec 2025 01:31:11 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:11 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Dec 2025 01:31:11 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Dec 2025 01:31:11 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:31:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:31:11 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Dec 2025 01:31:11 GMT
USER influxdb
# Tue, 30 Dec 2025 01:31:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:31:11 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e965e3d3ec6a91dec80966c8b4a3628f30528e45c9298fd7332b692e3638e6b`  
		Last Modified: Tue, 30 Dec 2025 01:31:35 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6292f164503508bd543afb2a34fe3a9df346b5185c1d6b533e82eb84e45b3199`  
		Last Modified: Tue, 30 Dec 2025 01:31:36 GMT  
		Size: 41.3 MB (41330301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c2a75907ea23323ce785ffa3d2b8aacdc1336fdc7448ee4e2fc8f906453e05`  
		Last Modified: Tue, 30 Dec 2025 01:31:31 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b48ab2f267b5da8b6bc56c07983565bd98d7ce97f4b63f86871b3e8dd6549f`  
		Last Modified: Tue, 30 Dec 2025 01:31:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd636fa5f5219124bef8e703d9a3bee02decad4433a7ecc63f870be67872aa92`  
		Last Modified: Tue, 30 Dec 2025 01:31:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:570977006cdbac40f7823a4a04d09b0bf3b16924a1665c84967abb1439944acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce27c34f86f55d9a093af84374e74aef8dfe4ac240462a8c6ba707ad3ac75f49`

```dockerfile
```

-	Layers:
	-	`sha256:dcd925d27fb9b2f4d21f96d34501ed100a3a5a62d70a2bfe8d248f65b34327b0`  
		Last Modified: Tue, 30 Dec 2025 06:20:57 GMT  
		Size: 4.7 MB (4675813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c2b1dcf8bc6490d822eed6db0b24e8cc2dbd939b1b0d7a68121547280a5756`  
		Last Modified: Tue, 30 Dec 2025 06:20:58 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ba63f2ef02eea546ec391a5c74bbe4a18235c4111b08f0e9660086637464495d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110091273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6becab1d76e19bdfb79289a760c6696d16383aef9e1494890e16665e1e844d84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:33:09 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 30 Dec 2025 01:33:14 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 30 Dec 2025 01:33:14 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:33:14 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Dec 2025 01:33:14 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Dec 2025 01:33:14 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:33:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:33:14 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Dec 2025 01:33:14 GMT
USER influxdb
# Tue, 30 Dec 2025 01:33:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:33:14 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0015662db9fbc9a53df2aca9a165229a6d8ad3d25c43f8ed173940dd3aa9e5af`  
		Last Modified: Tue, 30 Dec 2025 02:30:00 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61d6e982ea791409bf21d8e23a84b7860dfca7912e7018219733e6a434676c8`  
		Last Modified: Tue, 30 Dec 2025 01:33:37 GMT  
		Size: 38.1 MB (38130834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a012bc391e69b57ea5517e7c056c5d8a9c9d4f59e435eb832c997c49c1e676`  
		Last Modified: Tue, 30 Dec 2025 01:33:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45bd22bb1bc8c8cb9d608308133099a0474d1a517e867250e867daf33be1d6e`  
		Last Modified: Tue, 30 Dec 2025 01:33:34 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa56e22c59ecf6c6fec2ebe644683ffe45a78b09624df350c1da7716bf332af`  
		Last Modified: Tue, 30 Dec 2025 01:33:34 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:fba0ab0f35a256bea04f9483b12ef2380bf8d716cc9695c541bc97262edb05a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4691822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d1a101816ce5db2c1e4978e1f70b9cf568c09989facf9c493d11a20eb8f26`

```dockerfile
```

-	Layers:
	-	`sha256:7df4522606ee7dffc068731ff8e9e842cf9af470d7224f86e0943e3bf6e7d21d`  
		Last Modified: Tue, 30 Dec 2025 06:21:03 GMT  
		Size: 4.7 MB (4675271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2e45d1be8016c619ae6434ff96bf998e1225b9ab819cdec410d9eaa9f4a4fc`  
		Last Modified: Tue, 30 Dec 2025 06:21:05 GMT  
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
		Last Modified: Mon, 08 Dec 2025 02:21:06 GMT  
		Size: 1.2 MB (1225336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c347910584b08baf1a48bdf46c5c50dd24038eb1302b7007f31ce71bc927b592`  
		Last Modified: Mon, 08 Dec 2025 02:21:08 GMT  
		Size: 41.3 MB (41251703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a935c4d2c88a22b2b988a0ccac55421ea76be53d52269f7b632dcf92c515813`  
		Last Modified: Mon, 08 Dec 2025 02:21:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a53405a7e90893d67726045e12be0b8d6c77efc4329d83b02742c7dc703c64`  
		Last Modified: Mon, 08 Dec 2025 02:21:06 GMT  
		Size: 993.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559f188f2dcf26e5cc25cbe55a6ec7068097f6735e694bf00a27874305fe66fa`  
		Last Modified: Mon, 08 Dec 2025 02:21:06 GMT  
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
		Last Modified: Mon, 08 Dec 2025 14:17:07 GMT  
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
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3778cd6b7947fa40773e4d96fb04b28656fd002578dc1ba35152916dba4eab3`  
		Last Modified: Mon, 08 Dec 2025 09:22:08 GMT  
		Size: 1.3 MB (1290589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193f43b6c8619cf1483f881f1bdef6dd939ea58e7d495e8416bfda3d15d098c2`  
		Last Modified: Mon, 08 Dec 2025 09:22:10 GMT  
		Size: 38.1 MB (38058839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a6f8e76e4d9c33472e64d72f702c7962ba0b5e4d61db1c648411752212f71`  
		Last Modified: Mon, 08 Dec 2025 09:22:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31e522d0a6aa09c893a40e88167d5532ce096d84694b5970672f058e64bc5d6`  
		Last Modified: Mon, 08 Dec 2025 09:22:08 GMT  
		Size: 990.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf7f3756e6d6b4556e7f0ff09c0a747d1b2defff34996459ba9c9fe8623c697`  
		Last Modified: Mon, 08 Dec 2025 09:22:09 GMT  
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
		Last Modified: Tue, 09 Dec 2025 03:07:15 GMT  
		Size: 761.1 KB (761088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ee247e175c8dccb7cd34515f34b1749a76fd37134eef6a64643a3885004fe1`  
		Last Modified: Tue, 09 Dec 2025 03:07:14 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data`

```console
$ docker pull influxdb@sha256:48c52be245532f368ef410e1116638665b77aa2d32fc6098afa2f188a3adbf52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data` - linux; amd64

```console
$ docker pull influxdb@sha256:59ff0c552413774b3d6b385faae73eb305a023eb4185c1b715ddd09f3a28f201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114827586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a43cbebfe667441d3f471acc3de4203c13b3e4855e1b47c2d5c1dd5ef03e2eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Dec 2025 01:31:18 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Dec 2025 01:31:18 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:31:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:31:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4703e68bd36f5bcb8b2214bab1bbb6ba374a5c20c043154da748f3361921dd`  
		Last Modified: Tue, 30 Dec 2025 01:31:43 GMT  
		Size: 42.3 MB (42315670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41017fe2f59e61beba6e4c0a2d83b618810945b92af80b28894f51be37d86051`  
		Last Modified: Tue, 30 Dec 2025 01:31:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1660405a86b92ee6b29340ec8076f9cc40e0f3ddebc4cb6f55dd2ed21de5ad0a`  
		Last Modified: Tue, 30 Dec 2025 01:31:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8b0220b4de5db27d8578d560c61c069579680553c7bd4de3421fa45cb19ffc`  
		Last Modified: Tue, 30 Dec 2025 01:31:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:b776b538cdbd99fa57093351c24de79ccc588a9473f49ef51726368cb46f5f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874ed27b2a5144ac9452ccc025be647aca0a231354bd6fef1200ccf51a9954ac`

```dockerfile
```

-	Layers:
	-	`sha256:abd6d9c653d6411a9471bb744ee4b2a895594421861c2e10bb06fa1d1db73ee9`  
		Last Modified: Tue, 30 Dec 2025 06:21:03 GMT  
		Size: 4.7 MB (4685451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27131ca66cd9a9515bd87afd32c5d0c14dc2e042ccb2120638b47804cd6aeab5`  
		Last Modified: Tue, 30 Dec 2025 06:21:04 GMT  
		Size: 13.8 KB (13779 bytes)  
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
		Last Modified: Tue, 09 Dec 2025 22:33:29 GMT  
		Size: 1.2 MB (1225329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e0170f82fea093122d3570e0d358e936d1db98ed05a0d6a48d33037501b351`  
		Last Modified: Tue, 09 Dec 2025 22:33:31 GMT  
		Size: 42.3 MB (42254311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b0661d8dbfc3b43d49ec386e18c197ae353dd5d5c77c548207da941ba2ee68`  
		Last Modified: Mon, 15 Dec 2025 19:34:03 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39225506d3b8f10fd5e6623059b8c1e0d7efadec626f71dcf9da78fee4f7e2a`  
		Last Modified: Tue, 09 Dec 2025 22:33:28 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d72d987f87daa2925154010870639046590c11fa247eb8c38fdd2ea9c6094b`  
		Last Modified: Mon, 15 Dec 2025 19:34:04 GMT  
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
		Last Modified: Mon, 15 Dec 2025 19:34:04 GMT  
		Size: 15.2 KB (15191 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta`

```console
$ docker pull influxdb@sha256:a0f9c61dc18ed8aefd14d5038d3ca12a98c2761518c24728c4d03f92eae05ad5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:b8d5353f82e2bcc9fabca62cba9ba7876392cb4c0d264632ad973591fd290736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91289725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9718ab8f0c96d9df0ca5ccac148026aeffc54aa8d69a6065947040a2c6e8accd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Dec 2025 01:31:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Dec 2025 01:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:31:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fac420b8d1add9a518c8be0cadbd02cf2b0d721e683660ab29558b57a53f39e`  
		Last Modified: Tue, 30 Dec 2025 01:31:57 GMT  
		Size: 18.8 MB (18779017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e85d0585009faa68a9368aae4bc84c767729a35826873821dfbc4aa6141e2b5`  
		Last Modified: Tue, 30 Dec 2025 01:31:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefee4201d499772783be5a913f67391bb488eff5f377af4f36a20755a5932a5`  
		Last Modified: Tue, 30 Dec 2025 01:31:56 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:97fd89bcfe95081acf6933a13aba093f1c0e44b2f8d66558881dbf209b861d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4602907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd5fb5e2737dbc4eeaad475dc69ad7263fd7b4e523f9efaa0a340db32911432`

```dockerfile
```

-	Layers:
	-	`sha256:5e1e2fa8558e6841daae3568cdf28ed1410c6d2d55f39e4eae5943032a64bbe7`  
		Last Modified: Tue, 30 Dec 2025 06:21:08 GMT  
		Size: 4.6 MB (4590614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d7e461b14c9d975dd22648bf2177071baab81c1c357c7d7e280b6ea515e3d3c`  
		Last Modified: Tue, 30 Dec 2025 06:21:09 GMT  
		Size: 12.3 KB (12293 bytes)  
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
		Last Modified: Mon, 15 Dec 2025 20:39:36 GMT  
		Size: 1.2 MB (1225337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8df8f8e418a27917114426b3d245a3728772fe30be9e1b0b609e79b9ccb3b1d`  
		Last Modified: Mon, 15 Dec 2025 20:39:39 GMT  
		Size: 18.7 MB (18722501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96fdeefb85b445c179f78bb53968e8210d7aaa4a30cccb4d6452d9ac4a7b000`  
		Last Modified: Fri, 12 Dec 2025 22:35:31 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5817ad78e6b46e06d7f07b733f09a0eddd15b789d78398b86fe406d8cd2fdf7`  
		Last Modified: Tue, 09 Dec 2025 22:35:17 GMT  
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
$ docker pull influxdb@sha256:db03b9c599588cd5caded6df8b8258841017bf186898c6133a4f99b4d6134395
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.2` - linux; amd64

```console
$ docker pull influxdb@sha256:cc56fcc9a34e680b598a0872774c5e7eb804dafac7a1c18b6ef046f8f84322f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113843346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ab37e2f191a8e5edb169032e41f231436981ff1d892d26c55b98a8551cb3f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:07 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 30 Dec 2025 01:31:11 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 30 Dec 2025 01:31:11 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:11 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Dec 2025 01:31:11 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Dec 2025 01:31:11 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:31:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:31:11 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Dec 2025 01:31:11 GMT
USER influxdb
# Tue, 30 Dec 2025 01:31:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:31:11 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e965e3d3ec6a91dec80966c8b4a3628f30528e45c9298fd7332b692e3638e6b`  
		Last Modified: Tue, 30 Dec 2025 01:31:35 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6292f164503508bd543afb2a34fe3a9df346b5185c1d6b533e82eb84e45b3199`  
		Last Modified: Tue, 30 Dec 2025 01:31:36 GMT  
		Size: 41.3 MB (41330301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c2a75907ea23323ce785ffa3d2b8aacdc1336fdc7448ee4e2fc8f906453e05`  
		Last Modified: Tue, 30 Dec 2025 01:31:31 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b48ab2f267b5da8b6bc56c07983565bd98d7ce97f4b63f86871b3e8dd6549f`  
		Last Modified: Tue, 30 Dec 2025 01:31:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd636fa5f5219124bef8e703d9a3bee02decad4433a7ecc63f870be67872aa92`  
		Last Modified: Tue, 30 Dec 2025 01:31:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:570977006cdbac40f7823a4a04d09b0bf3b16924a1665c84967abb1439944acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce27c34f86f55d9a093af84374e74aef8dfe4ac240462a8c6ba707ad3ac75f49`

```dockerfile
```

-	Layers:
	-	`sha256:dcd925d27fb9b2f4d21f96d34501ed100a3a5a62d70a2bfe8d248f65b34327b0`  
		Last Modified: Tue, 30 Dec 2025 06:20:57 GMT  
		Size: 4.7 MB (4675813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c2b1dcf8bc6490d822eed6db0b24e8cc2dbd939b1b0d7a68121547280a5756`  
		Last Modified: Tue, 30 Dec 2025 06:20:58 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ba63f2ef02eea546ec391a5c74bbe4a18235c4111b08f0e9660086637464495d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110091273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6becab1d76e19bdfb79289a760c6696d16383aef9e1494890e16665e1e844d84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:33:09 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 30 Dec 2025 01:33:14 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 30 Dec 2025 01:33:14 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:33:14 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Dec 2025 01:33:14 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Dec 2025 01:33:14 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:33:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:33:14 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Dec 2025 01:33:14 GMT
USER influxdb
# Tue, 30 Dec 2025 01:33:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:33:14 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0015662db9fbc9a53df2aca9a165229a6d8ad3d25c43f8ed173940dd3aa9e5af`  
		Last Modified: Tue, 30 Dec 2025 02:30:00 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61d6e982ea791409bf21d8e23a84b7860dfca7912e7018219733e6a434676c8`  
		Last Modified: Tue, 30 Dec 2025 01:33:37 GMT  
		Size: 38.1 MB (38130834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a012bc391e69b57ea5517e7c056c5d8a9c9d4f59e435eb832c997c49c1e676`  
		Last Modified: Tue, 30 Dec 2025 01:33:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45bd22bb1bc8c8cb9d608308133099a0474d1a517e867250e867daf33be1d6e`  
		Last Modified: Tue, 30 Dec 2025 01:33:34 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa56e22c59ecf6c6fec2ebe644683ffe45a78b09624df350c1da7716bf332af`  
		Last Modified: Tue, 30 Dec 2025 01:33:34 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:fba0ab0f35a256bea04f9483b12ef2380bf8d716cc9695c541bc97262edb05a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4691822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d1a101816ce5db2c1e4978e1f70b9cf568c09989facf9c493d11a20eb8f26`

```dockerfile
```

-	Layers:
	-	`sha256:7df4522606ee7dffc068731ff8e9e842cf9af470d7224f86e0943e3bf6e7d21d`  
		Last Modified: Tue, 30 Dec 2025 06:21:03 GMT  
		Size: 4.7 MB (4675271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2e45d1be8016c619ae6434ff96bf998e1225b9ab819cdec410d9eaa9f4a4fc`  
		Last Modified: Tue, 30 Dec 2025 06:21:05 GMT  
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
		Last Modified: Mon, 08 Dec 2025 02:21:06 GMT  
		Size: 1.2 MB (1225336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c347910584b08baf1a48bdf46c5c50dd24038eb1302b7007f31ce71bc927b592`  
		Last Modified: Mon, 08 Dec 2025 02:21:08 GMT  
		Size: 41.3 MB (41251703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a935c4d2c88a22b2b988a0ccac55421ea76be53d52269f7b632dcf92c515813`  
		Last Modified: Mon, 08 Dec 2025 02:21:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a53405a7e90893d67726045e12be0b8d6c77efc4329d83b02742c7dc703c64`  
		Last Modified: Mon, 08 Dec 2025 02:21:06 GMT  
		Size: 993.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559f188f2dcf26e5cc25cbe55a6ec7068097f6735e694bf00a27874305fe66fa`  
		Last Modified: Mon, 08 Dec 2025 02:21:06 GMT  
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
		Last Modified: Mon, 08 Dec 2025 14:17:07 GMT  
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
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3778cd6b7947fa40773e4d96fb04b28656fd002578dc1ba35152916dba4eab3`  
		Last Modified: Mon, 08 Dec 2025 09:22:08 GMT  
		Size: 1.3 MB (1290589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193f43b6c8619cf1483f881f1bdef6dd939ea58e7d495e8416bfda3d15d098c2`  
		Last Modified: Mon, 08 Dec 2025 09:22:10 GMT  
		Size: 38.1 MB (38058839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a6f8e76e4d9c33472e64d72f702c7962ba0b5e4d61db1c648411752212f71`  
		Last Modified: Mon, 08 Dec 2025 09:22:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31e522d0a6aa09c893a40e88167d5532ce096d84694b5970672f058e64bc5d6`  
		Last Modified: Mon, 08 Dec 2025 09:22:08 GMT  
		Size: 990.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf7f3756e6d6b4556e7f0ff09c0a747d1b2defff34996459ba9c9fe8623c697`  
		Last Modified: Mon, 08 Dec 2025 09:22:09 GMT  
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
		Last Modified: Tue, 09 Dec 2025 03:07:15 GMT  
		Size: 761.1 KB (761088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ee247e175c8dccb7cd34515f34b1749a76fd37134eef6a64643a3885004fe1`  
		Last Modified: Tue, 09 Dec 2025 03:07:14 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-data`

```console
$ docker pull influxdb@sha256:48c52be245532f368ef410e1116638665b77aa2d32fc6098afa2f188a3adbf52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-data` - linux; amd64

```console
$ docker pull influxdb@sha256:59ff0c552413774b3d6b385faae73eb305a023eb4185c1b715ddd09f3a28f201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114827586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a43cbebfe667441d3f471acc3de4203c13b3e4855e1b47c2d5c1dd5ef03e2eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Dec 2025 01:31:18 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Dec 2025 01:31:18 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:31:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:31:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4703e68bd36f5bcb8b2214bab1bbb6ba374a5c20c043154da748f3361921dd`  
		Last Modified: Tue, 30 Dec 2025 01:31:43 GMT  
		Size: 42.3 MB (42315670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41017fe2f59e61beba6e4c0a2d83b618810945b92af80b28894f51be37d86051`  
		Last Modified: Tue, 30 Dec 2025 01:31:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1660405a86b92ee6b29340ec8076f9cc40e0f3ddebc4cb6f55dd2ed21de5ad0a`  
		Last Modified: Tue, 30 Dec 2025 01:31:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8b0220b4de5db27d8578d560c61c069579680553c7bd4de3421fa45cb19ffc`  
		Last Modified: Tue, 30 Dec 2025 01:31:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:b776b538cdbd99fa57093351c24de79ccc588a9473f49ef51726368cb46f5f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874ed27b2a5144ac9452ccc025be647aca0a231354bd6fef1200ccf51a9954ac`

```dockerfile
```

-	Layers:
	-	`sha256:abd6d9c653d6411a9471bb744ee4b2a895594421861c2e10bb06fa1d1db73ee9`  
		Last Modified: Tue, 30 Dec 2025 06:21:03 GMT  
		Size: 4.7 MB (4685451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27131ca66cd9a9515bd87afd32c5d0c14dc2e042ccb2120638b47804cd6aeab5`  
		Last Modified: Tue, 30 Dec 2025 06:21:04 GMT  
		Size: 13.8 KB (13779 bytes)  
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
		Last Modified: Tue, 09 Dec 2025 22:33:29 GMT  
		Size: 1.2 MB (1225329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e0170f82fea093122d3570e0d358e936d1db98ed05a0d6a48d33037501b351`  
		Last Modified: Tue, 09 Dec 2025 22:33:31 GMT  
		Size: 42.3 MB (42254311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b0661d8dbfc3b43d49ec386e18c197ae353dd5d5c77c548207da941ba2ee68`  
		Last Modified: Mon, 15 Dec 2025 19:34:03 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39225506d3b8f10fd5e6623059b8c1e0d7efadec626f71dcf9da78fee4f7e2a`  
		Last Modified: Tue, 09 Dec 2025 22:33:28 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d72d987f87daa2925154010870639046590c11fa247eb8c38fdd2ea9c6094b`  
		Last Modified: Mon, 15 Dec 2025 19:34:04 GMT  
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
		Last Modified: Mon, 15 Dec 2025 19:34:04 GMT  
		Size: 15.2 KB (15191 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-meta`

```console
$ docker pull influxdb@sha256:a0f9c61dc18ed8aefd14d5038d3ca12a98c2761518c24728c4d03f92eae05ad5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:b8d5353f82e2bcc9fabca62cba9ba7876392cb4c0d264632ad973591fd290736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91289725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9718ab8f0c96d9df0ca5ccac148026aeffc54aa8d69a6065947040a2c6e8accd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Dec 2025 01:31:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Dec 2025 01:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:31:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fac420b8d1add9a518c8be0cadbd02cf2b0d721e683660ab29558b57a53f39e`  
		Last Modified: Tue, 30 Dec 2025 01:31:57 GMT  
		Size: 18.8 MB (18779017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e85d0585009faa68a9368aae4bc84c767729a35826873821dfbc4aa6141e2b5`  
		Last Modified: Tue, 30 Dec 2025 01:31:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefee4201d499772783be5a913f67391bb488eff5f377af4f36a20755a5932a5`  
		Last Modified: Tue, 30 Dec 2025 01:31:56 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:97fd89bcfe95081acf6933a13aba093f1c0e44b2f8d66558881dbf209b861d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4602907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd5fb5e2737dbc4eeaad475dc69ad7263fd7b4e523f9efaa0a340db32911432`

```dockerfile
```

-	Layers:
	-	`sha256:5e1e2fa8558e6841daae3568cdf28ed1410c6d2d55f39e4eae5943032a64bbe7`  
		Last Modified: Tue, 30 Dec 2025 06:21:08 GMT  
		Size: 4.6 MB (4590614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d7e461b14c9d975dd22648bf2177071baab81c1c357c7d7e280b6ea515e3d3c`  
		Last Modified: Tue, 30 Dec 2025 06:21:09 GMT  
		Size: 12.3 KB (12293 bytes)  
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
		Last Modified: Mon, 15 Dec 2025 20:39:36 GMT  
		Size: 1.2 MB (1225337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8df8f8e418a27917114426b3d245a3728772fe30be9e1b0b609e79b9ccb3b1d`  
		Last Modified: Mon, 15 Dec 2025 20:39:39 GMT  
		Size: 18.7 MB (18722501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96fdeefb85b445c179f78bb53968e8210d7aaa4a30cccb4d6452d9ac4a7b000`  
		Last Modified: Fri, 12 Dec 2025 22:35:31 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5817ad78e6b46e06d7f07b733f09a0eddd15b789d78398b86fe406d8cd2fdf7`  
		Last Modified: Tue, 09 Dec 2025 22:35:17 GMT  
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
$ docker pull influxdb@sha256:9e967a2283f54ecd401377f1ed677c882adc23dd4090fb5f0c7ebe98a8138a8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:cd9338522e3d5c507d281f031c99bf7553a28f5c0f599906518dd9851b384e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107224041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3408898af3df5a76c9a579faaf938d8a72178a7d1559302d8f85053d7a44f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:54:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:54:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 29 Dec 2025 23:54:58 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 29 Dec 2025 23:54:59 GMT
ENV GOSU_VER=1.19
# Mon, 29 Dec 2025 23:54:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:54:59 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 29 Dec 2025 23:54:59 GMT
ENV INFLUXDB_PR=-2
# Mon, 29 Dec 2025 23:54:59 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 29 Dec 2025 23:55:03 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 29 Dec 2025 23:55:03 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 29 Dec 2025 23:55:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 29 Dec 2025 23:55:04 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:55:04 GMT
CMD ["influxd"]
# Mon, 29 Dec 2025 23:55:04 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 29 Dec 2025 23:55:04 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 29 Dec 2025 23:55:04 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 29 Dec 2025 23:55:04 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 29 Dec 2025 23:55:04 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3eda513cda0dfb20cda875b352884f5f9032b1bad8cfd33b31bba3bfc4f079`  
		Last Modified: Mon, 29 Dec 2025 23:55:25 GMT  
		Size: 9.8 MB (9796291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2cc7314c76b61ace608bf8ce61fc60e2b8693ce32f76ea3695174aebdcc99e`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ced5038ff2dee1ab3a4fe7787b10f38a0f1dbe8f9719d6d98eca37538794b75`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fffb9e985775c37ccd426ddf9f40006fe74df96168e05188652d15c19bbee8`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 811.5 KB (811473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4b92236f46aac610b9dd8642f9d6c68d23ace8339918a777d8a670e4cdeba2`  
		Last Modified: Mon, 29 Dec 2025 23:55:29 GMT  
		Size: 50.4 MB (50447138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbce1186b18e56e3f22a64ec3f4a2ce82f33b46838ee5cefaeb83ffb0c4d4208`  
		Last Modified: Mon, 29 Dec 2025 23:55:25 GMT  
		Size: 11.8 MB (11773790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfc177b3dcd07b0056741edc461eaab058036e61f464b7b8d35de48a8fbae47`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6553a5f188eded8c1d292b51539522875b491fb29a92c351091de39ca27189`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5540325d51e4aeda9c6c8021fba87d440e37147d513355886c1ba5c102ae2f`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:6f946b312bf6b20a645d8cddfbb09bc81d0505515c8567b65c029a3500667f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a91951ab76298fccacefe4325b019cc6f16b12ed29038953cdc96190a784026`

```dockerfile
```

-	Layers:
	-	`sha256:65a1a3c4a54968fa4ab83e6375a19c9f31ef036bca8ca95f879606ceeb022f3a`  
		Last Modified: Tue, 30 Dec 2025 03:21:20 GMT  
		Size: 2.9 MB (2934227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b0cb0c2e3ef255c3c89ff570ddb7d8ec40e39ebcbf3b28a69c72bb0f3dd1227`  
		Last Modified: Tue, 30 Dec 2025 03:21:20 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:7d7288ba3a2827317f23ca682ee89d82c67b8886fb16b9eadd760c219542dd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103624752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14e20f215b379fe4f34b2e5c673986e33fe384442c1191723c7cc2bc44d1e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:56:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:56:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 29 Dec 2025 23:56:11 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 29 Dec 2025 23:56:12 GMT
ENV GOSU_VER=1.19
# Mon, 29 Dec 2025 23:56:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:56:12 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 29 Dec 2025 23:56:12 GMT
ENV INFLUXDB_PR=-2
# Mon, 29 Dec 2025 23:56:12 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 29 Dec 2025 23:56:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 29 Dec 2025 23:56:16 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 29 Dec 2025 23:56:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 29 Dec 2025 23:56:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:56:17 GMT
CMD ["influxd"]
# Mon, 29 Dec 2025 23:56:17 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 29 Dec 2025 23:56:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 29 Dec 2025 23:56:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 29 Dec 2025 23:56:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 29 Dec 2025 23:56:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2476917a5ea8832eb4f0ccb76bdf7f15d39e870e85c993e2824d21ebd21d80`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 9.6 MB (9626427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297409a2ba01c8ae930ab72e0cc776bd9e9b13780a1105208f20d437597ceb1d`  
		Last Modified: Mon, 29 Dec 2025 23:56:38 GMT  
		Size: 5.8 MB (5790401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a4bee7cf9792245fcffb60ef6ac8c43ac4e378e02d0b2c7fe104c044b84df9`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a67094e0b44d7b3294fc80e471c424c2f5dd2f125cf7dc63807b480448dc390`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 766.4 KB (766364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7208972ac46056e1f195f137e14374336c343a7da096d5c5e3a04e449d7d391a`  
		Last Modified: Mon, 29 Dec 2025 23:56:44 GMT  
		Size: 48.2 MB (48229404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82919091c9e4cb426deb55ae9dd4046c2e10d7106fd2c221abba170dfb6e013f`  
		Last Modified: Mon, 29 Dec 2025 23:56:38 GMT  
		Size: 11.1 MB (11099995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62de181bab838309f47cb36555a248525d527656ca1811404c29cbffaa64640`  
		Last Modified: Mon, 29 Dec 2025 23:56:40 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d852dd88b22838dc3b0f3fe973f7fca4de7e98fe5498e9b45946b99cc944390f`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813cb2d2c0591cc7bebf34b7ac9adec9eecda6617a91dbee62fa49e1fb790276`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:cd24e284afb5aebe35d7c24dcd0c94928cfc7cc5ea688c187bac54d8c7a2bf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ee92d9efbfd8a46ef5c0c9b592c00fade820b6b10c843fd163076184744be0`

```dockerfile
```

-	Layers:
	-	`sha256:76a8e1c7bf83b6ab8a38b0b4e219b6d3b8d02a2df2532aa1a40f3b516bcd029b`  
		Last Modified: Tue, 30 Dec 2025 03:21:24 GMT  
		Size: 2.9 MB (2933707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601dfd7508e497db9e6c80458304b1656f8e43f9a4591c72621f694cdb21b546`  
		Last Modified: Tue, 30 Dec 2025 03:21:25 GMT  
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
		Last Modified: Thu, 11 Dec 2025 21:22:08 GMT  
		Size: 9.9 MB (9862216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71475ef0f8f2c5f8c394cdda52333392709fc87e769397a0389fb1bb743d399b`  
		Last Modified: Thu, 11 Dec 2025 21:22:08 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315475c1c17f7a223ea2b8a1d9a1985ce438a3bae2dae153555a5d457b051c1`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc9021d0ef61725243ae72546a2a75243c5424fa7d0fc53f20c469d377cba3`  
		Last Modified: Thu, 11 Dec 2025 21:22:13 GMT  
		Size: 50.4 MB (50447116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c548f8f09a0ce506a8c2e69d75de76926e996dfe9a46448c756d6647e8a04c`  
		Last Modified: Thu, 11 Dec 2025 21:22:08 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e504a5513a054282de4e3d4006c910c7003f8804e45058cf073a0422f0212d1`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d818200c6c4e7df4884a358b6f80bca9c959914eced87214ae2c44e58fd35b`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
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
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce46991d2c4c48fd52d13891e1b5eb0777120c6d83d07fcc82f06c4340cfb6ba`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af32475cc26ad10355d0ebd8d9c80f88c7f6c44bcf28115edc647d31b95f9884`  
		Last Modified: Thu, 11 Dec 2025 21:22:06 GMT  
		Size: 9.8 MB (9822470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaafcce51f3333786fe19ee810e7107ca5c17a1a11e4b278b34d6d8989811de7`  
		Last Modified: Thu, 11 Dec 2025 21:22:06 GMT  
		Size: 5.8 MB (5790439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b70514028425c28cf39d8baef11c310457123a628d37c437bd6661fbaad6e`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f20cada75ad84d27130c93e200a873f7b2f5078d5a2049be4894b3a568aa4`  
		Last Modified: Thu, 11 Dec 2025 21:22:10 GMT  
		Size: 48.2 MB (48229359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea275cc0d43ac8b796329c90b2d0397003fdf129d2fa4b0c407b9ffb957177b`  
		Last Modified: Thu, 11 Dec 2025 21:22:11 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f18f15a6ac7b5a0a7673d362af6cd43b52cfe07914127acffa738249bb566cd`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de188f5486eb8567f178074e890509083cc993bcfb3a37457dd2300060ec14ff`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abede7ea0d56bd3a18f4443dc825494ff3d4993f87fee95b61f6d3153eb3f702`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
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
$ docker pull influxdb@sha256:e6dc6a2a5c250167a6f0d0857aec9db97fbe1f52fe7058dc2fb242372145be50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:2f8c08b8aed31b20d3358c7bd6bf2f2a7f5419672ba5055cda4ca7f78a9f6b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157222063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd90eb27c0236fcbdf5ac3724b92d04857ecc808bd4ff2dfe0c1b62ffee5732`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:55:03 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 29 Dec 2025 23:55:06 GMT
ENV GOSU_VER=1.16
# Mon, 29 Dec 2025 23:55:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:55:06 GMT
ENV INFLUXDB_VERSION=2.7.12
# Mon, 29 Dec 2025 23:55:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 29 Dec 2025 23:55:09 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 29 Dec 2025 23:55:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 29 Dec 2025 23:55:10 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 29 Dec 2025 23:55:10 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 29 Dec 2025 23:55:10 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 29 Dec 2025 23:55:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:55:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:55:10 GMT
CMD ["influxd"]
# Mon, 29 Dec 2025 23:55:10 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 29 Dec 2025 23:55:10 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 29 Dec 2025 23:55:10 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 29 Dec 2025 23:55:10 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 29 Dec 2025 23:55:10 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911ce392b3ff8f7fc7bad408739640c2df6ef585615d6f789157e54e5c90589f`  
		Last Modified: Mon, 29 Dec 2025 23:55:37 GMT  
		Size: 9.8 MB (9796344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f946e9fe797aac90f3486fb81c7960814cec74974a3a8682034defd9a12235af`  
		Last Modified: Mon, 29 Dec 2025 23:55:36 GMT  
		Size: 6.2 MB (6156977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1c9d92f8e3f07af9f4cbada6f64cc65d20e341f8a1ce0831cc948a5502377d`  
		Last Modified: Mon, 29 Dec 2025 23:55:36 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a76c1719b589adb261c347c29d83a8d64d120553159213c54bbd7832bd15c`  
		Last Modified: Mon, 29 Dec 2025 23:55:36 GMT  
		Size: 1.0 MB (1012037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3588660c9119be795a74d64f15aab36672ddd3b02517016df4bdde9618905376`  
		Last Modified: Mon, 29 Dec 2025 23:55:44 GMT  
		Size: 100.2 MB (100244542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4793382cb55bd36a1ca159cfd334ca7a744acfb2870e818e9e40cc7048a3ff99`  
		Last Modified: Mon, 29 Dec 2025 23:55:37 GMT  
		Size: 11.8 MB (11773790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdb6d5acabc51a5483c02112210726ad289bdc59a17c3b905ffe01e629b79f4`  
		Last Modified: Mon, 29 Dec 2025 23:55:36 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a872d05b6ddc879f6c1cd44ff7a309eecd713e48b3b8c79ca4ba099ab919eeb`  
		Last Modified: Mon, 29 Dec 2025 23:55:36 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5540325d51e4aeda9c6c8021fba87d440e37147d513355886c1ba5c102ae2f`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:e3eee75f94e2d61e3a66e4a69784276a80de01f8fb21315f02ea99862573713c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079e0afcecc4adfd1d9a8283efcd52e77eaf181d8dd23cd564a44e9c5b830f55`

```dockerfile
```

-	Layers:
	-	`sha256:6da9bc49dc49ea0198a92b6caa9d5f30be6865d3a87f8c9df09e937cf61df039`  
		Last Modified: Tue, 30 Dec 2025 03:21:20 GMT  
		Size: 3.0 MB (2981474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d1dc2b9a0f6a2d373e31e5c9353e9554b5af7dd939589046b876aedbb6f0752`  
		Last Modified: Tue, 30 Dec 2025 03:21:21 GMT  
		Size: 32.9 KB (32901 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:fe13b784556a920b68ad79142482b405f8dbd948c403c140de09f35b02a86f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f7e1c5eb76215a777a0f7f168b0dd1aa637c3983bf9ab361421917f5dcfe35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:55:40 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:55:42 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 29 Dec 2025 23:55:42 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 29 Dec 2025 23:55:44 GMT
ENV GOSU_VER=1.16
# Mon, 29 Dec 2025 23:55:44 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:55:44 GMT
ENV INFLUXDB_VERSION=2.7.12
# Mon, 29 Dec 2025 23:55:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 29 Dec 2025 23:55:47 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 29 Dec 2025 23:55:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 29 Dec 2025 23:55:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 29 Dec 2025 23:55:48 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 29 Dec 2025 23:55:48 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 29 Dec 2025 23:55:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:55:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:55:48 GMT
CMD ["influxd"]
# Mon, 29 Dec 2025 23:55:48 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 29 Dec 2025 23:55:48 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 29 Dec 2025 23:55:48 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 29 Dec 2025 23:55:48 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 29 Dec 2025 23:55:48 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efb8c253aea6267c9e7a235eaaf3ce7a0412b6fa39771e82b6422ca688a90c`  
		Last Modified: Mon, 29 Dec 2025 23:56:14 GMT  
		Size: 9.6 MB (9626441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ad6cd1893acd6a39d06fc230f59a2e1e98c6d1a0035a6bfc03001f97e48de`  
		Last Modified: Mon, 29 Dec 2025 23:56:13 GMT  
		Size: 5.8 MB (5790426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9e81823593bf35aad642225e250e4d5ec2be67299c5abf0cc38ce32508416a`  
		Last Modified: Mon, 29 Dec 2025 23:56:13 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807de51802d577f86e21445c18adaf1ecc6fdd75d5a7e128b8e89da3ac4612bc`  
		Last Modified: Mon, 29 Dec 2025 23:56:13 GMT  
		Size: 938.9 KB (938874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdecdb2802de3872d3361f4d9bb8a872e9a6e844e1b0e13a1308f1409ed637d6`  
		Last Modified: Mon, 29 Dec 2025 23:56:28 GMT  
		Size: 96.0 MB (96039006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8d0f19f6d7e6bb0537ad54da4d747c41ff083ed78cdc402ed4618c742fde7b`  
		Last Modified: Mon, 29 Dec 2025 23:56:14 GMT  
		Size: 11.1 MB (11099996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6249781dbd2ab556a8808c86fe7591506b1e2e7ae5b9ce389d422f7b12ba1e7`  
		Last Modified: Mon, 29 Dec 2025 23:56:13 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1ea441e70fb53e826ade62b3dd3085537f744077e1a6659b0677aa58482fa`  
		Last Modified: Mon, 29 Dec 2025 23:56:13 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e30dad2679d9c5f85ba9f7809e639a07f39ab07f31b4dbecf5b8a7f6735f40`  
		Last Modified: Mon, 29 Dec 2025 23:56:13 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:8b72ba3349c5f632a8454b43f44db5b60dfd10e3b537f788b737f28eefb84823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d997591860029fbf8b3d30ce0d1ba325a4806957b6986ea8b913f0aab71509a`

```dockerfile
```

-	Layers:
	-	`sha256:b173ef3ab60bd2e71d4fb794b3b14651280552592572f6be5c06ee5d67ecc87f`  
		Last Modified: Tue, 30 Dec 2025 03:21:25 GMT  
		Size: 3.0 MB (2980678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e310d7d84f159b5948e28e7c7e29b449206d3c669620fc2fb4fc21bb5cced1d2`  
		Last Modified: Tue, 30 Dec 2025 03:21:26 GMT  
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
		Last Modified: Mon, 08 Dec 2025 00:36:47 GMT  
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
		Last Modified: Mon, 08 Dec 2025 00:36:51 GMT  
		Size: 50.1 MB (50118379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b2ed5e22ac99676c240cb61c758189300e7929cfc6729851c369529ad53d8d`  
		Last Modified: Mon, 08 Dec 2025 00:36:49 GMT  
		Size: 11.8 MB (11773778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68db778755a7a92ab67642d92cc7aa0c820cd21e5943b496d3b32e9fd2403de7`  
		Last Modified: Mon, 08 Dec 2025 00:36:48 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d366f9033d07efa0b056a0d9362d12bf8f19cf51deec87929bb9a095810b8c21`  
		Last Modified: Mon, 08 Dec 2025 00:36:48 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a54836f3da745e3ea2b1a54e11d6a3a24d9402e2007b4610da65910613fe2`  
		Last Modified: Mon, 08 Dec 2025 00:36:49 GMT  
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
		Last Modified: Mon, 08 Dec 2025 05:34:13 GMT  
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
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
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
		Last Modified: Sun, 07 Dec 2025 22:41:09 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846ab0df2a8dd47b00f9e08910902bc9137be17fc01ecb2ab92865324a0a692`  
		Last Modified: Sun, 07 Dec 2025 22:41:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee341d51fc6d484c991e3e387ad2bab42cc99f8c5f0c144f3548538763046b7`  
		Last Modified: Sun, 07 Dec 2025 22:41:14 GMT  
		Size: 48.0 MB (48017161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467babbc25c511c880690592c05bf5c8bf7eb3718a0ffcbb6bb66881d449be0`  
		Last Modified: Sun, 07 Dec 2025 22:41:10 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73275e145aac044b3ee173c0907851a448d495a9d0f964f1d943e707c8a79108`  
		Last Modified: Sun, 07 Dec 2025 22:41:06 GMT  
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
		Last Modified: Mon, 08 Dec 2025 00:50:44 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12`

```console
$ docker pull influxdb@sha256:e6dc6a2a5c250167a6f0d0857aec9db97fbe1f52fe7058dc2fb242372145be50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:2f8c08b8aed31b20d3358c7bd6bf2f2a7f5419672ba5055cda4ca7f78a9f6b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157222063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd90eb27c0236fcbdf5ac3724b92d04857ecc808bd4ff2dfe0c1b62ffee5732`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:55:03 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 29 Dec 2025 23:55:06 GMT
ENV GOSU_VER=1.16
# Mon, 29 Dec 2025 23:55:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:55:06 GMT
ENV INFLUXDB_VERSION=2.7.12
# Mon, 29 Dec 2025 23:55:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 29 Dec 2025 23:55:09 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 29 Dec 2025 23:55:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 29 Dec 2025 23:55:10 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 29 Dec 2025 23:55:10 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 29 Dec 2025 23:55:10 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 29 Dec 2025 23:55:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:55:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:55:10 GMT
CMD ["influxd"]
# Mon, 29 Dec 2025 23:55:10 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 29 Dec 2025 23:55:10 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 29 Dec 2025 23:55:10 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 29 Dec 2025 23:55:10 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 29 Dec 2025 23:55:10 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911ce392b3ff8f7fc7bad408739640c2df6ef585615d6f789157e54e5c90589f`  
		Last Modified: Mon, 29 Dec 2025 23:55:37 GMT  
		Size: 9.8 MB (9796344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f946e9fe797aac90f3486fb81c7960814cec74974a3a8682034defd9a12235af`  
		Last Modified: Mon, 29 Dec 2025 23:55:36 GMT  
		Size: 6.2 MB (6156977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1c9d92f8e3f07af9f4cbada6f64cc65d20e341f8a1ce0831cc948a5502377d`  
		Last Modified: Mon, 29 Dec 2025 23:55:36 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a76c1719b589adb261c347c29d83a8d64d120553159213c54bbd7832bd15c`  
		Last Modified: Mon, 29 Dec 2025 23:55:36 GMT  
		Size: 1.0 MB (1012037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3588660c9119be795a74d64f15aab36672ddd3b02517016df4bdde9618905376`  
		Last Modified: Mon, 29 Dec 2025 23:55:44 GMT  
		Size: 100.2 MB (100244542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4793382cb55bd36a1ca159cfd334ca7a744acfb2870e818e9e40cc7048a3ff99`  
		Last Modified: Mon, 29 Dec 2025 23:55:37 GMT  
		Size: 11.8 MB (11773790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdb6d5acabc51a5483c02112210726ad289bdc59a17c3b905ffe01e629b79f4`  
		Last Modified: Mon, 29 Dec 2025 23:55:36 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a872d05b6ddc879f6c1cd44ff7a309eecd713e48b3b8c79ca4ba099ab919eeb`  
		Last Modified: Mon, 29 Dec 2025 23:55:36 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5540325d51e4aeda9c6c8021fba87d440e37147d513355886c1ba5c102ae2f`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:e3eee75f94e2d61e3a66e4a69784276a80de01f8fb21315f02ea99862573713c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079e0afcecc4adfd1d9a8283efcd52e77eaf181d8dd23cd564a44e9c5b830f55`

```dockerfile
```

-	Layers:
	-	`sha256:6da9bc49dc49ea0198a92b6caa9d5f30be6865d3a87f8c9df09e937cf61df039`  
		Last Modified: Tue, 30 Dec 2025 03:21:20 GMT  
		Size: 3.0 MB (2981474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d1dc2b9a0f6a2d373e31e5c9353e9554b5af7dd939589046b876aedbb6f0752`  
		Last Modified: Tue, 30 Dec 2025 03:21:21 GMT  
		Size: 32.9 KB (32901 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:fe13b784556a920b68ad79142482b405f8dbd948c403c140de09f35b02a86f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f7e1c5eb76215a777a0f7f168b0dd1aa637c3983bf9ab361421917f5dcfe35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:55:40 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:55:42 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 29 Dec 2025 23:55:42 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 29 Dec 2025 23:55:44 GMT
ENV GOSU_VER=1.16
# Mon, 29 Dec 2025 23:55:44 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:55:44 GMT
ENV INFLUXDB_VERSION=2.7.12
# Mon, 29 Dec 2025 23:55:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 29 Dec 2025 23:55:47 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 29 Dec 2025 23:55:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 29 Dec 2025 23:55:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 29 Dec 2025 23:55:48 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 29 Dec 2025 23:55:48 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 29 Dec 2025 23:55:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:55:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:55:48 GMT
CMD ["influxd"]
# Mon, 29 Dec 2025 23:55:48 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 29 Dec 2025 23:55:48 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 29 Dec 2025 23:55:48 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 29 Dec 2025 23:55:48 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 29 Dec 2025 23:55:48 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efb8c253aea6267c9e7a235eaaf3ce7a0412b6fa39771e82b6422ca688a90c`  
		Last Modified: Mon, 29 Dec 2025 23:56:14 GMT  
		Size: 9.6 MB (9626441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ad6cd1893acd6a39d06fc230f59a2e1e98c6d1a0035a6bfc03001f97e48de`  
		Last Modified: Mon, 29 Dec 2025 23:56:13 GMT  
		Size: 5.8 MB (5790426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9e81823593bf35aad642225e250e4d5ec2be67299c5abf0cc38ce32508416a`  
		Last Modified: Mon, 29 Dec 2025 23:56:13 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807de51802d577f86e21445c18adaf1ecc6fdd75d5a7e128b8e89da3ac4612bc`  
		Last Modified: Mon, 29 Dec 2025 23:56:13 GMT  
		Size: 938.9 KB (938874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdecdb2802de3872d3361f4d9bb8a872e9a6e844e1b0e13a1308f1409ed637d6`  
		Last Modified: Mon, 29 Dec 2025 23:56:28 GMT  
		Size: 96.0 MB (96039006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8d0f19f6d7e6bb0537ad54da4d747c41ff083ed78cdc402ed4618c742fde7b`  
		Last Modified: Mon, 29 Dec 2025 23:56:14 GMT  
		Size: 11.1 MB (11099996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6249781dbd2ab556a8808c86fe7591506b1e2e7ae5b9ce389d422f7b12ba1e7`  
		Last Modified: Mon, 29 Dec 2025 23:56:13 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1ea441e70fb53e826ade62b3dd3085537f744077e1a6659b0677aa58482fa`  
		Last Modified: Mon, 29 Dec 2025 23:56:13 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e30dad2679d9c5f85ba9f7809e639a07f39ab07f31b4dbecf5b8a7f6735f40`  
		Last Modified: Mon, 29 Dec 2025 23:56:13 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:8b72ba3349c5f632a8454b43f44db5b60dfd10e3b537f788b737f28eefb84823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d997591860029fbf8b3d30ce0d1ba325a4806957b6986ea8b913f0aab71509a`

```dockerfile
```

-	Layers:
	-	`sha256:b173ef3ab60bd2e71d4fb794b3b14651280552592572f6be5c06ee5d67ecc87f`  
		Last Modified: Tue, 30 Dec 2025 03:21:25 GMT  
		Size: 3.0 MB (2980678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e310d7d84f159b5948e28e7c7e29b449206d3c669620fc2fb4fc21bb5cced1d2`  
		Last Modified: Tue, 30 Dec 2025 03:21:26 GMT  
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
		Last Modified: Mon, 08 Dec 2025 00:36:47 GMT  
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
		Last Modified: Mon, 08 Dec 2025 00:36:51 GMT  
		Size: 50.1 MB (50118379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b2ed5e22ac99676c240cb61c758189300e7929cfc6729851c369529ad53d8d`  
		Last Modified: Mon, 08 Dec 2025 00:36:49 GMT  
		Size: 11.8 MB (11773778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68db778755a7a92ab67642d92cc7aa0c820cd21e5943b496d3b32e9fd2403de7`  
		Last Modified: Mon, 08 Dec 2025 00:36:48 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d366f9033d07efa0b056a0d9362d12bf8f19cf51deec87929bb9a095810b8c21`  
		Last Modified: Mon, 08 Dec 2025 00:36:48 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a54836f3da745e3ea2b1a54e11d6a3a24d9402e2007b4610da65910613fe2`  
		Last Modified: Mon, 08 Dec 2025 00:36:49 GMT  
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
		Last Modified: Mon, 08 Dec 2025 05:34:13 GMT  
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
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
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
		Last Modified: Sun, 07 Dec 2025 22:41:09 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846ab0df2a8dd47b00f9e08910902bc9137be17fc01ecb2ab92865324a0a692`  
		Last Modified: Sun, 07 Dec 2025 22:41:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee341d51fc6d484c991e3e387ad2bab42cc99f8c5f0c144f3548538763046b7`  
		Last Modified: Sun, 07 Dec 2025 22:41:14 GMT  
		Size: 48.0 MB (48017161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467babbc25c511c880690592c05bf5c8bf7eb3718a0ffcbb6bb66881d449be0`  
		Last Modified: Sun, 07 Dec 2025 22:41:10 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73275e145aac044b3ee173c0907851a448d495a9d0f964f1d943e707c8a79108`  
		Last Modified: Sun, 07 Dec 2025 22:41:06 GMT  
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
		Last Modified: Mon, 08 Dec 2025 00:50:44 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8`

```console
$ docker pull influxdb@sha256:9e967a2283f54ecd401377f1ed677c882adc23dd4090fb5f0c7ebe98a8138a8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8` - linux; amd64

```console
$ docker pull influxdb@sha256:cd9338522e3d5c507d281f031c99bf7553a28f5c0f599906518dd9851b384e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107224041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3408898af3df5a76c9a579faaf938d8a72178a7d1559302d8f85053d7a44f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:54:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:54:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 29 Dec 2025 23:54:58 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 29 Dec 2025 23:54:59 GMT
ENV GOSU_VER=1.19
# Mon, 29 Dec 2025 23:54:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:54:59 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 29 Dec 2025 23:54:59 GMT
ENV INFLUXDB_PR=-2
# Mon, 29 Dec 2025 23:54:59 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 29 Dec 2025 23:55:03 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 29 Dec 2025 23:55:03 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 29 Dec 2025 23:55:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 29 Dec 2025 23:55:04 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:55:04 GMT
CMD ["influxd"]
# Mon, 29 Dec 2025 23:55:04 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 29 Dec 2025 23:55:04 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 29 Dec 2025 23:55:04 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 29 Dec 2025 23:55:04 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 29 Dec 2025 23:55:04 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3eda513cda0dfb20cda875b352884f5f9032b1bad8cfd33b31bba3bfc4f079`  
		Last Modified: Mon, 29 Dec 2025 23:55:25 GMT  
		Size: 9.8 MB (9796291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2cc7314c76b61ace608bf8ce61fc60e2b8693ce32f76ea3695174aebdcc99e`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ced5038ff2dee1ab3a4fe7787b10f38a0f1dbe8f9719d6d98eca37538794b75`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fffb9e985775c37ccd426ddf9f40006fe74df96168e05188652d15c19bbee8`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 811.5 KB (811473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4b92236f46aac610b9dd8642f9d6c68d23ace8339918a777d8a670e4cdeba2`  
		Last Modified: Mon, 29 Dec 2025 23:55:29 GMT  
		Size: 50.4 MB (50447138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbce1186b18e56e3f22a64ec3f4a2ce82f33b46838ee5cefaeb83ffb0c4d4208`  
		Last Modified: Mon, 29 Dec 2025 23:55:25 GMT  
		Size: 11.8 MB (11773790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfc177b3dcd07b0056741edc461eaab058036e61f464b7b8d35de48a8fbae47`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6553a5f188eded8c1d292b51539522875b491fb29a92c351091de39ca27189`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5540325d51e4aeda9c6c8021fba87d440e37147d513355886c1ba5c102ae2f`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:6f946b312bf6b20a645d8cddfbb09bc81d0505515c8567b65c029a3500667f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a91951ab76298fccacefe4325b019cc6f16b12ed29038953cdc96190a784026`

```dockerfile
```

-	Layers:
	-	`sha256:65a1a3c4a54968fa4ab83e6375a19c9f31ef036bca8ca95f879606ceeb022f3a`  
		Last Modified: Tue, 30 Dec 2025 03:21:20 GMT  
		Size: 2.9 MB (2934227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b0cb0c2e3ef255c3c89ff570ddb7d8ec40e39ebcbf3b28a69c72bb0f3dd1227`  
		Last Modified: Tue, 30 Dec 2025 03:21:20 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:7d7288ba3a2827317f23ca682ee89d82c67b8886fb16b9eadd760c219542dd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103624752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14e20f215b379fe4f34b2e5c673986e33fe384442c1191723c7cc2bc44d1e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:56:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:56:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 29 Dec 2025 23:56:11 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 29 Dec 2025 23:56:12 GMT
ENV GOSU_VER=1.19
# Mon, 29 Dec 2025 23:56:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:56:12 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 29 Dec 2025 23:56:12 GMT
ENV INFLUXDB_PR=-2
# Mon, 29 Dec 2025 23:56:12 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 29 Dec 2025 23:56:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 29 Dec 2025 23:56:16 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 29 Dec 2025 23:56:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 29 Dec 2025 23:56:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:56:17 GMT
CMD ["influxd"]
# Mon, 29 Dec 2025 23:56:17 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 29 Dec 2025 23:56:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 29 Dec 2025 23:56:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 29 Dec 2025 23:56:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 29 Dec 2025 23:56:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2476917a5ea8832eb4f0ccb76bdf7f15d39e870e85c993e2824d21ebd21d80`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 9.6 MB (9626427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297409a2ba01c8ae930ab72e0cc776bd9e9b13780a1105208f20d437597ceb1d`  
		Last Modified: Mon, 29 Dec 2025 23:56:38 GMT  
		Size: 5.8 MB (5790401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a4bee7cf9792245fcffb60ef6ac8c43ac4e378e02d0b2c7fe104c044b84df9`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a67094e0b44d7b3294fc80e471c424c2f5dd2f125cf7dc63807b480448dc390`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 766.4 KB (766364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7208972ac46056e1f195f137e14374336c343a7da096d5c5e3a04e449d7d391a`  
		Last Modified: Mon, 29 Dec 2025 23:56:44 GMT  
		Size: 48.2 MB (48229404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82919091c9e4cb426deb55ae9dd4046c2e10d7106fd2c221abba170dfb6e013f`  
		Last Modified: Mon, 29 Dec 2025 23:56:38 GMT  
		Size: 11.1 MB (11099995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62de181bab838309f47cb36555a248525d527656ca1811404c29cbffaa64640`  
		Last Modified: Mon, 29 Dec 2025 23:56:40 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d852dd88b22838dc3b0f3fe973f7fca4de7e98fe5498e9b45946b99cc944390f`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813cb2d2c0591cc7bebf34b7ac9adec9eecda6617a91dbee62fa49e1fb790276`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:cd24e284afb5aebe35d7c24dcd0c94928cfc7cc5ea688c187bac54d8c7a2bf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ee92d9efbfd8a46ef5c0c9b592c00fade820b6b10c843fd163076184744be0`

```dockerfile
```

-	Layers:
	-	`sha256:76a8e1c7bf83b6ab8a38b0b4e219b6d3b8d02a2df2532aa1a40f3b516bcd029b`  
		Last Modified: Tue, 30 Dec 2025 03:21:24 GMT  
		Size: 2.9 MB (2933707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601dfd7508e497db9e6c80458304b1656f8e43f9a4591c72621f694cdb21b546`  
		Last Modified: Tue, 30 Dec 2025 03:21:25 GMT  
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
		Last Modified: Thu, 11 Dec 2025 21:22:08 GMT  
		Size: 9.9 MB (9862216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71475ef0f8f2c5f8c394cdda52333392709fc87e769397a0389fb1bb743d399b`  
		Last Modified: Thu, 11 Dec 2025 21:22:08 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315475c1c17f7a223ea2b8a1d9a1985ce438a3bae2dae153555a5d457b051c1`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc9021d0ef61725243ae72546a2a75243c5424fa7d0fc53f20c469d377cba3`  
		Last Modified: Thu, 11 Dec 2025 21:22:13 GMT  
		Size: 50.4 MB (50447116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c548f8f09a0ce506a8c2e69d75de76926e996dfe9a46448c756d6647e8a04c`  
		Last Modified: Thu, 11 Dec 2025 21:22:08 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e504a5513a054282de4e3d4006c910c7003f8804e45058cf073a0422f0212d1`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d818200c6c4e7df4884a358b6f80bca9c959914eced87214ae2c44e58fd35b`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
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
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce46991d2c4c48fd52d13891e1b5eb0777120c6d83d07fcc82f06c4340cfb6ba`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af32475cc26ad10355d0ebd8d9c80f88c7f6c44bcf28115edc647d31b95f9884`  
		Last Modified: Thu, 11 Dec 2025 21:22:06 GMT  
		Size: 9.8 MB (9822470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaafcce51f3333786fe19ee810e7107ca5c17a1a11e4b278b34d6d8989811de7`  
		Last Modified: Thu, 11 Dec 2025 21:22:06 GMT  
		Size: 5.8 MB (5790439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b70514028425c28cf39d8baef11c310457123a628d37c437bd6661fbaad6e`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f20cada75ad84d27130c93e200a873f7b2f5078d5a2049be4894b3a568aa4`  
		Last Modified: Thu, 11 Dec 2025 21:22:10 GMT  
		Size: 48.2 MB (48229359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea275cc0d43ac8b796329c90b2d0397003fdf129d2fa4b0c407b9ffb957177b`  
		Last Modified: Thu, 11 Dec 2025 21:22:11 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f18f15a6ac7b5a0a7673d362af6cd43b52cfe07914127acffa738249bb566cd`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de188f5486eb8567f178074e890509083cc993bcfb3a37457dd2300060ec14ff`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abede7ea0d56bd3a18f4443dc825494ff3d4993f87fee95b61f6d3153eb3f702`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
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
$ docker pull influxdb@sha256:9e967a2283f54ecd401377f1ed677c882adc23dd4090fb5f0c7ebe98a8138a8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0` - linux; amd64

```console
$ docker pull influxdb@sha256:cd9338522e3d5c507d281f031c99bf7553a28f5c0f599906518dd9851b384e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107224041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3408898af3df5a76c9a579faaf938d8a72178a7d1559302d8f85053d7a44f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:54:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:54:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 29 Dec 2025 23:54:58 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 29 Dec 2025 23:54:59 GMT
ENV GOSU_VER=1.19
# Mon, 29 Dec 2025 23:54:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:54:59 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 29 Dec 2025 23:54:59 GMT
ENV INFLUXDB_PR=-2
# Mon, 29 Dec 2025 23:54:59 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 29 Dec 2025 23:55:03 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 29 Dec 2025 23:55:03 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 29 Dec 2025 23:55:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 29 Dec 2025 23:55:04 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:55:04 GMT
CMD ["influxd"]
# Mon, 29 Dec 2025 23:55:04 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 29 Dec 2025 23:55:04 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 29 Dec 2025 23:55:04 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 29 Dec 2025 23:55:04 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 29 Dec 2025 23:55:04 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3eda513cda0dfb20cda875b352884f5f9032b1bad8cfd33b31bba3bfc4f079`  
		Last Modified: Mon, 29 Dec 2025 23:55:25 GMT  
		Size: 9.8 MB (9796291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2cc7314c76b61ace608bf8ce61fc60e2b8693ce32f76ea3695174aebdcc99e`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ced5038ff2dee1ab3a4fe7787b10f38a0f1dbe8f9719d6d98eca37538794b75`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fffb9e985775c37ccd426ddf9f40006fe74df96168e05188652d15c19bbee8`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 811.5 KB (811473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4b92236f46aac610b9dd8642f9d6c68d23ace8339918a777d8a670e4cdeba2`  
		Last Modified: Mon, 29 Dec 2025 23:55:29 GMT  
		Size: 50.4 MB (50447138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbce1186b18e56e3f22a64ec3f4a2ce82f33b46838ee5cefaeb83ffb0c4d4208`  
		Last Modified: Mon, 29 Dec 2025 23:55:25 GMT  
		Size: 11.8 MB (11773790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfc177b3dcd07b0056741edc461eaab058036e61f464b7b8d35de48a8fbae47`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6553a5f188eded8c1d292b51539522875b491fb29a92c351091de39ca27189`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5540325d51e4aeda9c6c8021fba87d440e37147d513355886c1ba5c102ae2f`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:6f946b312bf6b20a645d8cddfbb09bc81d0505515c8567b65c029a3500667f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a91951ab76298fccacefe4325b019cc6f16b12ed29038953cdc96190a784026`

```dockerfile
```

-	Layers:
	-	`sha256:65a1a3c4a54968fa4ab83e6375a19c9f31ef036bca8ca95f879606ceeb022f3a`  
		Last Modified: Tue, 30 Dec 2025 03:21:20 GMT  
		Size: 2.9 MB (2934227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b0cb0c2e3ef255c3c89ff570ddb7d8ec40e39ebcbf3b28a69c72bb0f3dd1227`  
		Last Modified: Tue, 30 Dec 2025 03:21:20 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:7d7288ba3a2827317f23ca682ee89d82c67b8886fb16b9eadd760c219542dd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103624752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14e20f215b379fe4f34b2e5c673986e33fe384442c1191723c7cc2bc44d1e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:56:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:56:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 29 Dec 2025 23:56:11 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 29 Dec 2025 23:56:12 GMT
ENV GOSU_VER=1.19
# Mon, 29 Dec 2025 23:56:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:56:12 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 29 Dec 2025 23:56:12 GMT
ENV INFLUXDB_PR=-2
# Mon, 29 Dec 2025 23:56:12 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 29 Dec 2025 23:56:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 29 Dec 2025 23:56:16 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 29 Dec 2025 23:56:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 29 Dec 2025 23:56:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:56:17 GMT
CMD ["influxd"]
# Mon, 29 Dec 2025 23:56:17 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 29 Dec 2025 23:56:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 29 Dec 2025 23:56:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 29 Dec 2025 23:56:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 29 Dec 2025 23:56:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2476917a5ea8832eb4f0ccb76bdf7f15d39e870e85c993e2824d21ebd21d80`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 9.6 MB (9626427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297409a2ba01c8ae930ab72e0cc776bd9e9b13780a1105208f20d437597ceb1d`  
		Last Modified: Mon, 29 Dec 2025 23:56:38 GMT  
		Size: 5.8 MB (5790401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a4bee7cf9792245fcffb60ef6ac8c43ac4e378e02d0b2c7fe104c044b84df9`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a67094e0b44d7b3294fc80e471c424c2f5dd2f125cf7dc63807b480448dc390`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 766.4 KB (766364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7208972ac46056e1f195f137e14374336c343a7da096d5c5e3a04e449d7d391a`  
		Last Modified: Mon, 29 Dec 2025 23:56:44 GMT  
		Size: 48.2 MB (48229404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82919091c9e4cb426deb55ae9dd4046c2e10d7106fd2c221abba170dfb6e013f`  
		Last Modified: Mon, 29 Dec 2025 23:56:38 GMT  
		Size: 11.1 MB (11099995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62de181bab838309f47cb36555a248525d527656ca1811404c29cbffaa64640`  
		Last Modified: Mon, 29 Dec 2025 23:56:40 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d852dd88b22838dc3b0f3fe973f7fca4de7e98fe5498e9b45946b99cc944390f`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813cb2d2c0591cc7bebf34b7ac9adec9eecda6617a91dbee62fa49e1fb790276`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:cd24e284afb5aebe35d7c24dcd0c94928cfc7cc5ea688c187bac54d8c7a2bf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ee92d9efbfd8a46ef5c0c9b592c00fade820b6b10c843fd163076184744be0`

```dockerfile
```

-	Layers:
	-	`sha256:76a8e1c7bf83b6ab8a38b0b4e219b6d3b8d02a2df2532aa1a40f3b516bcd029b`  
		Last Modified: Tue, 30 Dec 2025 03:21:24 GMT  
		Size: 2.9 MB (2933707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601dfd7508e497db9e6c80458304b1656f8e43f9a4591c72621f694cdb21b546`  
		Last Modified: Tue, 30 Dec 2025 03:21:25 GMT  
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
		Last Modified: Thu, 11 Dec 2025 21:22:08 GMT  
		Size: 9.9 MB (9862216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71475ef0f8f2c5f8c394cdda52333392709fc87e769397a0389fb1bb743d399b`  
		Last Modified: Thu, 11 Dec 2025 21:22:08 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315475c1c17f7a223ea2b8a1d9a1985ce438a3bae2dae153555a5d457b051c1`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc9021d0ef61725243ae72546a2a75243c5424fa7d0fc53f20c469d377cba3`  
		Last Modified: Thu, 11 Dec 2025 21:22:13 GMT  
		Size: 50.4 MB (50447116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c548f8f09a0ce506a8c2e69d75de76926e996dfe9a46448c756d6647e8a04c`  
		Last Modified: Thu, 11 Dec 2025 21:22:08 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e504a5513a054282de4e3d4006c910c7003f8804e45058cf073a0422f0212d1`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d818200c6c4e7df4884a358b6f80bca9c959914eced87214ae2c44e58fd35b`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
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
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce46991d2c4c48fd52d13891e1b5eb0777120c6d83d07fcc82f06c4340cfb6ba`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af32475cc26ad10355d0ebd8d9c80f88c7f6c44bcf28115edc647d31b95f9884`  
		Last Modified: Thu, 11 Dec 2025 21:22:06 GMT  
		Size: 9.8 MB (9822470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaafcce51f3333786fe19ee810e7107ca5c17a1a11e4b278b34d6d8989811de7`  
		Last Modified: Thu, 11 Dec 2025 21:22:06 GMT  
		Size: 5.8 MB (5790439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b70514028425c28cf39d8baef11c310457123a628d37c437bd6661fbaad6e`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f20cada75ad84d27130c93e200a873f7b2f5078d5a2049be4894b3a568aa4`  
		Last Modified: Thu, 11 Dec 2025 21:22:10 GMT  
		Size: 48.2 MB (48229359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea275cc0d43ac8b796329c90b2d0397003fdf129d2fa4b0c407b9ffb957177b`  
		Last Modified: Thu, 11 Dec 2025 21:22:11 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f18f15a6ac7b5a0a7673d362af6cd43b52cfe07914127acffa738249bb566cd`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de188f5486eb8567f178074e890509083cc993bcfb3a37457dd2300060ec14ff`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abede7ea0d56bd3a18f4443dc825494ff3d4993f87fee95b61f6d3153eb3f702`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
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
$ docker pull influxdb@sha256:0452079f02f4d13fe3fbb74df3df9aefc902f58242c1b423a4d2cfb57346e199
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:88655683b666037d4d999619f0bf89959411fccf709ec5acd4e730ddcd0112b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119310544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b838c638c71c34d958e76f4eb357de3a965a3f81555e378155705660629c1f`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:54:04 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:54:04 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:54:04 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:54:04 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9dea577090dac77be07b9cc74c6237c4d4a29e624c7253d32ae21d6f196ae8`  
		Last Modified: Wed, 17 Dec 2025 23:54:31 GMT  
		Size: 6.7 MB (6666136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b7260fb8b9949df8a568a2ab08ec327f75e8de23a1c7832b91a8b59a9eeac2`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394211902e5963e29110b161e250c43839f38bbd8bf032f1f5ef5f2f518c03bf`  
		Last Modified: Wed, 17 Dec 2025 23:54:37 GMT  
		Size: 82.9 MB (82915390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27765a5b9cf865533049b2b3be0a97ae30367882b22cc708748594b5230d0c1`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de81e7d91528b57cc4c9461a0bd36737cecd98c4fdf6f346abfec658c7a6f6f5`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3a6632fbd2a97ccd27b651f4454a24353669d4e980fa305fe066f4ef9e086b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9020c2dd74bccec277cd1c5f5bbab2296e81432aa76e46a9ef5db211e8af7c1`

```dockerfile
```

-	Layers:
	-	`sha256:8253ae625ade4876b9ae4480b1fff70214e61d8395a8d4453134212328c6620c`  
		Last Modified: Thu, 18 Dec 2025 00:20:37 GMT  
		Size: 2.3 MB (2310563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77fe49c85f11dbbbd310dbb808989a7dd67d8b6db212d8b5d2f9a8bd97947934`  
		Last Modified: Thu, 18 Dec 2025 00:20:37 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a30cb2b6575a0b2523585b72d3eb7ea49ba05abab0e43f2cc4e949fc23f833c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110019558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a45979608e2b37df510a125528eae572058c793c79eae7abd4ca0e7a14f3792`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:56 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:55:02 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:55:02 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:55:02 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:55:02 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191ed597af36e20c4e341347d9aae17df8f44181f0198d35ae4104b1fa8301f5`  
		Last Modified: Wed, 17 Dec 2025 23:55:32 GMT  
		Size: 6.7 MB (6676586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386868f6cc91a80987c4eb312890d52e0551569d3d9f59e90df2d87577c907e5`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525e1f297447837d6c81237bfc442d0980ecb9b40ce037ec9e8fa289c41f07ff`  
		Last Modified: Wed, 17 Dec 2025 23:55:36 GMT  
		Size: 74.5 MB (74476691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ceae49e12bfe8d10edf42dc95afcd410bb8bb9967d0c7fb621c7443dc58fd0`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdcc23b7614d8487daf0da2c16fe1a93557dbc9746db244c5aeae1943a39a5f`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:873150c7b0d9db1020675db32a25bdb111e7fcb72a9187c83ee6bdeb894a888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf92ef1265a6d4fedb6780ffe8e5099731b2a6b03a5767327e9b7b11564c5cbc`

```dockerfile
```

-	Layers:
	-	`sha256:2addf4befe7a325f7f12fe579dacba5749a6a51ffd81e4d600a3a89acbb076b7`  
		Last Modified: Thu, 18 Dec 2025 00:20:42 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd287962a95203141b8d424e36a291c7eb4855f3aef923fcb730c2a1ad6bc72`  
		Last Modified: Thu, 18 Dec 2025 00:20:43 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:3df4ecc96e2136585b25beea47e4f164469059a72714d646096cbdfb639b64b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:adc291da58fa13d386afb400a77f324b816fbed5858b3bb8d4018bfbe0fd4027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127590250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806ba4c62d2e005744a021183e0a15960a6778fcb4811f94905666a688032f23`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:54:31 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:54:31 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:54:31 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:54:31 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:54:31 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:54:31 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9dea577090dac77be07b9cc74c6237c4d4a29e624c7253d32ae21d6f196ae8`  
		Last Modified: Wed, 17 Dec 2025 23:54:31 GMT  
		Size: 6.7 MB (6666136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b7260fb8b9949df8a568a2ab08ec327f75e8de23a1c7832b91a8b59a9eeac2`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39532d39a98bcd3d51104687002cdf5339a387cc074fd54a8b168ca0d6d5861`  
		Last Modified: Wed, 17 Dec 2025 23:55:04 GMT  
		Size: 91.2 MB (91195097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02fbf1ae289239b1f1d60ce260e4d88a0380d638c1a62a8f4835e7b02d93eb`  
		Last Modified: Wed, 17 Dec 2025 23:54:53 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078288b9048f2c197b8f944e7d235c4d0125ee27e137627bc3e6157da1c49442`  
		Last Modified: Wed, 17 Dec 2025 23:54:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:473893e2630d47f20de5be30e39adabfcd784d4b5b5df63eaea74246bf43c66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ade24fa6e6c1b931e41fa20be0241b1b868b62d844911fcf64d21f423f0c84`

```dockerfile
```

-	Layers:
	-	`sha256:d1e9fd7becf5945b33fc6dd4fa3daa07bcee9a01c6a83c658e6acef29da901cb`  
		Last Modified: Thu, 18 Dec 2025 00:20:46 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73c4ebab1b452e6752cc732cf9cfd3842e8d485073df84caa952a02909134fa`  
		Last Modified: Thu, 18 Dec 2025 00:20:47 GMT  
		Size: 17.8 KB (17795 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:cfe2cc8633f9d8c03984fc9cc2250ab3e32bcc2220d355e45e35dd68b9bad774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118243665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776349d3680708857004cf0a881a87f4dea7af7e3b6905b1bd5b915a5515b425`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:56 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:55:31 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:55:31 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:55:31 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:55:31 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:55:31 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:55:31 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191ed597af36e20c4e341347d9aae17df8f44181f0198d35ae4104b1fa8301f5`  
		Last Modified: Wed, 17 Dec 2025 23:55:32 GMT  
		Size: 6.7 MB (6676586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386868f6cc91a80987c4eb312890d52e0551569d3d9f59e90df2d87577c907e5`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b26028ef8d9d1265ddfca6921c63b32b2491093546577849a7ad3a3c4cf539d`  
		Last Modified: Wed, 17 Dec 2025 23:56:01 GMT  
		Size: 82.7 MB (82700801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be273fcd50c97b84052fb6268ed901d9f30c4756840910ccaa3edb6c1b17c73c`  
		Last Modified: Wed, 17 Dec 2025 23:55:53 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e75308189e7e14eaa1e12c82d79c1a573291a6d830fd8a34e9b3547e61c659`  
		Last Modified: Wed, 17 Dec 2025 23:55:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:8c308538d22818fbc58e3c3fa13e08ba71c590e8f361eaba0eab79507139a8e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad3fd895b5744d5ce8f752dadc6efb69df22e784801d63f07d3b0e415c06f85`

```dockerfile
```

-	Layers:
	-	`sha256:6d4853809421861d33841f7ca0bf70386efe1246fe777635ccb62180c8f8a86a`  
		Last Modified: Thu, 18 Dec 2025 00:20:52 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9400f28461d88c04ce7bd0a602c7ed9ce05b1ff2f90418a7945a02b72e08d9db`  
		Last Modified: Thu, 18 Dec 2025 00:20:53 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8-core`

```console
$ docker pull influxdb@sha256:0452079f02f4d13fe3fbb74df3df9aefc902f58242c1b423a4d2cfb57346e199
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8-core` - linux; amd64

```console
$ docker pull influxdb@sha256:88655683b666037d4d999619f0bf89959411fccf709ec5acd4e730ddcd0112b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119310544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b838c638c71c34d958e76f4eb357de3a965a3f81555e378155705660629c1f`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:54:04 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:54:04 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:54:04 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:54:04 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9dea577090dac77be07b9cc74c6237c4d4a29e624c7253d32ae21d6f196ae8`  
		Last Modified: Wed, 17 Dec 2025 23:54:31 GMT  
		Size: 6.7 MB (6666136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b7260fb8b9949df8a568a2ab08ec327f75e8de23a1c7832b91a8b59a9eeac2`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394211902e5963e29110b161e250c43839f38bbd8bf032f1f5ef5f2f518c03bf`  
		Last Modified: Wed, 17 Dec 2025 23:54:37 GMT  
		Size: 82.9 MB (82915390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27765a5b9cf865533049b2b3be0a97ae30367882b22cc708748594b5230d0c1`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de81e7d91528b57cc4c9461a0bd36737cecd98c4fdf6f346abfec658c7a6f6f5`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3a6632fbd2a97ccd27b651f4454a24353669d4e980fa305fe066f4ef9e086b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9020c2dd74bccec277cd1c5f5bbab2296e81432aa76e46a9ef5db211e8af7c1`

```dockerfile
```

-	Layers:
	-	`sha256:8253ae625ade4876b9ae4480b1fff70214e61d8395a8d4453134212328c6620c`  
		Last Modified: Thu, 18 Dec 2025 00:20:37 GMT  
		Size: 2.3 MB (2310563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77fe49c85f11dbbbd310dbb808989a7dd67d8b6db212d8b5d2f9a8bd97947934`  
		Last Modified: Thu, 18 Dec 2025 00:20:37 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a30cb2b6575a0b2523585b72d3eb7ea49ba05abab0e43f2cc4e949fc23f833c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110019558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a45979608e2b37df510a125528eae572058c793c79eae7abd4ca0e7a14f3792`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:56 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:55:02 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:55:02 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:55:02 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:55:02 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191ed597af36e20c4e341347d9aae17df8f44181f0198d35ae4104b1fa8301f5`  
		Last Modified: Wed, 17 Dec 2025 23:55:32 GMT  
		Size: 6.7 MB (6676586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386868f6cc91a80987c4eb312890d52e0551569d3d9f59e90df2d87577c907e5`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525e1f297447837d6c81237bfc442d0980ecb9b40ce037ec9e8fa289c41f07ff`  
		Last Modified: Wed, 17 Dec 2025 23:55:36 GMT  
		Size: 74.5 MB (74476691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ceae49e12bfe8d10edf42dc95afcd410bb8bb9967d0c7fb621c7443dc58fd0`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdcc23b7614d8487daf0da2c16fe1a93557dbc9746db244c5aeae1943a39a5f`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:873150c7b0d9db1020675db32a25bdb111e7fcb72a9187c83ee6bdeb894a888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf92ef1265a6d4fedb6780ffe8e5099731b2a6b03a5767327e9b7b11564c5cbc`

```dockerfile
```

-	Layers:
	-	`sha256:2addf4befe7a325f7f12fe579dacba5749a6a51ffd81e4d600a3a89acbb076b7`  
		Last Modified: Thu, 18 Dec 2025 00:20:42 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd287962a95203141b8d424e36a291c7eb4855f3aef923fcb730c2a1ad6bc72`  
		Last Modified: Thu, 18 Dec 2025 00:20:43 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8-enterprise`

```console
$ docker pull influxdb@sha256:3df4ecc96e2136585b25beea47e4f164469059a72714d646096cbdfb639b64b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:adc291da58fa13d386afb400a77f324b816fbed5858b3bb8d4018bfbe0fd4027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127590250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806ba4c62d2e005744a021183e0a15960a6778fcb4811f94905666a688032f23`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:54:31 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:54:31 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:54:31 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:54:31 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:54:31 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:54:31 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9dea577090dac77be07b9cc74c6237c4d4a29e624c7253d32ae21d6f196ae8`  
		Last Modified: Wed, 17 Dec 2025 23:54:31 GMT  
		Size: 6.7 MB (6666136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b7260fb8b9949df8a568a2ab08ec327f75e8de23a1c7832b91a8b59a9eeac2`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39532d39a98bcd3d51104687002cdf5339a387cc074fd54a8b168ca0d6d5861`  
		Last Modified: Wed, 17 Dec 2025 23:55:04 GMT  
		Size: 91.2 MB (91195097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02fbf1ae289239b1f1d60ce260e4d88a0380d638c1a62a8f4835e7b02d93eb`  
		Last Modified: Wed, 17 Dec 2025 23:54:53 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078288b9048f2c197b8f944e7d235c4d0125ee27e137627bc3e6157da1c49442`  
		Last Modified: Wed, 17 Dec 2025 23:54:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:473893e2630d47f20de5be30e39adabfcd784d4b5b5df63eaea74246bf43c66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ade24fa6e6c1b931e41fa20be0241b1b868b62d844911fcf64d21f423f0c84`

```dockerfile
```

-	Layers:
	-	`sha256:d1e9fd7becf5945b33fc6dd4fa3daa07bcee9a01c6a83c658e6acef29da901cb`  
		Last Modified: Thu, 18 Dec 2025 00:20:46 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73c4ebab1b452e6752cc732cf9cfd3842e8d485073df84caa952a02909134fa`  
		Last Modified: Thu, 18 Dec 2025 00:20:47 GMT  
		Size: 17.8 KB (17795 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:cfe2cc8633f9d8c03984fc9cc2250ab3e32bcc2220d355e45e35dd68b9bad774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118243665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776349d3680708857004cf0a881a87f4dea7af7e3b6905b1bd5b915a5515b425`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:56 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:55:31 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:55:31 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:55:31 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:55:31 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:55:31 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:55:31 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191ed597af36e20c4e341347d9aae17df8f44181f0198d35ae4104b1fa8301f5`  
		Last Modified: Wed, 17 Dec 2025 23:55:32 GMT  
		Size: 6.7 MB (6676586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386868f6cc91a80987c4eb312890d52e0551569d3d9f59e90df2d87577c907e5`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b26028ef8d9d1265ddfca6921c63b32b2491093546577849a7ad3a3c4cf539d`  
		Last Modified: Wed, 17 Dec 2025 23:56:01 GMT  
		Size: 82.7 MB (82700801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be273fcd50c97b84052fb6268ed901d9f30c4756840910ccaa3edb6c1b17c73c`  
		Last Modified: Wed, 17 Dec 2025 23:55:53 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e75308189e7e14eaa1e12c82d79c1a573291a6d830fd8a34e9b3547e61c659`  
		Last Modified: Wed, 17 Dec 2025 23:55:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:8c308538d22818fbc58e3c3fa13e08ba71c590e8f361eaba0eab79507139a8e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad3fd895b5744d5ce8f752dadc6efb69df22e784801d63f07d3b0e415c06f85`

```dockerfile
```

-	Layers:
	-	`sha256:6d4853809421861d33841f7ca0bf70386efe1246fe777635ccb62180c8f8a86a`  
		Last Modified: Thu, 18 Dec 2025 00:20:52 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9400f28461d88c04ce7bd0a602c7ed9ce05b1ff2f90418a7945a02b72e08d9db`  
		Last Modified: Thu, 18 Dec 2025 00:20:53 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8.0-core`

```console
$ docker pull influxdb@sha256:0452079f02f4d13fe3fbb74df3df9aefc902f58242c1b423a4d2cfb57346e199
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8.0-core` - linux; amd64

```console
$ docker pull influxdb@sha256:88655683b666037d4d999619f0bf89959411fccf709ec5acd4e730ddcd0112b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119310544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b838c638c71c34d958e76f4eb357de3a965a3f81555e378155705660629c1f`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:54:04 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:54:04 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:54:04 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:54:04 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9dea577090dac77be07b9cc74c6237c4d4a29e624c7253d32ae21d6f196ae8`  
		Last Modified: Wed, 17 Dec 2025 23:54:31 GMT  
		Size: 6.7 MB (6666136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b7260fb8b9949df8a568a2ab08ec327f75e8de23a1c7832b91a8b59a9eeac2`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394211902e5963e29110b161e250c43839f38bbd8bf032f1f5ef5f2f518c03bf`  
		Last Modified: Wed, 17 Dec 2025 23:54:37 GMT  
		Size: 82.9 MB (82915390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27765a5b9cf865533049b2b3be0a97ae30367882b22cc708748594b5230d0c1`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de81e7d91528b57cc4c9461a0bd36737cecd98c4fdf6f346abfec658c7a6f6f5`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3a6632fbd2a97ccd27b651f4454a24353669d4e980fa305fe066f4ef9e086b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9020c2dd74bccec277cd1c5f5bbab2296e81432aa76e46a9ef5db211e8af7c1`

```dockerfile
```

-	Layers:
	-	`sha256:8253ae625ade4876b9ae4480b1fff70214e61d8395a8d4453134212328c6620c`  
		Last Modified: Thu, 18 Dec 2025 00:20:37 GMT  
		Size: 2.3 MB (2310563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77fe49c85f11dbbbd310dbb808989a7dd67d8b6db212d8b5d2f9a8bd97947934`  
		Last Modified: Thu, 18 Dec 2025 00:20:37 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8.0-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a30cb2b6575a0b2523585b72d3eb7ea49ba05abab0e43f2cc4e949fc23f833c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110019558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a45979608e2b37df510a125528eae572058c793c79eae7abd4ca0e7a14f3792`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:56 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:55:02 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:55:02 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:55:02 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:55:02 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191ed597af36e20c4e341347d9aae17df8f44181f0198d35ae4104b1fa8301f5`  
		Last Modified: Wed, 17 Dec 2025 23:55:32 GMT  
		Size: 6.7 MB (6676586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386868f6cc91a80987c4eb312890d52e0551569d3d9f59e90df2d87577c907e5`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525e1f297447837d6c81237bfc442d0980ecb9b40ce037ec9e8fa289c41f07ff`  
		Last Modified: Wed, 17 Dec 2025 23:55:36 GMT  
		Size: 74.5 MB (74476691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ceae49e12bfe8d10edf42dc95afcd410bb8bb9967d0c7fb621c7443dc58fd0`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdcc23b7614d8487daf0da2c16fe1a93557dbc9746db244c5aeae1943a39a5f`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:873150c7b0d9db1020675db32a25bdb111e7fcb72a9187c83ee6bdeb894a888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf92ef1265a6d4fedb6780ffe8e5099731b2a6b03a5767327e9b7b11564c5cbc`

```dockerfile
```

-	Layers:
	-	`sha256:2addf4befe7a325f7f12fe579dacba5749a6a51ffd81e4d600a3a89acbb076b7`  
		Last Modified: Thu, 18 Dec 2025 00:20:42 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd287962a95203141b8d424e36a291c7eb4855f3aef923fcb730c2a1ad6bc72`  
		Last Modified: Thu, 18 Dec 2025 00:20:43 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8.0-enterprise`

```console
$ docker pull influxdb@sha256:3df4ecc96e2136585b25beea47e4f164469059a72714d646096cbdfb639b64b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8.0-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:adc291da58fa13d386afb400a77f324b816fbed5858b3bb8d4018bfbe0fd4027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127590250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806ba4c62d2e005744a021183e0a15960a6778fcb4811f94905666a688032f23`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:54:31 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:54:31 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:54:31 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:54:31 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:54:31 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:54:31 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9dea577090dac77be07b9cc74c6237c4d4a29e624c7253d32ae21d6f196ae8`  
		Last Modified: Wed, 17 Dec 2025 23:54:31 GMT  
		Size: 6.7 MB (6666136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b7260fb8b9949df8a568a2ab08ec327f75e8de23a1c7832b91a8b59a9eeac2`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39532d39a98bcd3d51104687002cdf5339a387cc074fd54a8b168ca0d6d5861`  
		Last Modified: Wed, 17 Dec 2025 23:55:04 GMT  
		Size: 91.2 MB (91195097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02fbf1ae289239b1f1d60ce260e4d88a0380d638c1a62a8f4835e7b02d93eb`  
		Last Modified: Wed, 17 Dec 2025 23:54:53 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078288b9048f2c197b8f944e7d235c4d0125ee27e137627bc3e6157da1c49442`  
		Last Modified: Wed, 17 Dec 2025 23:54:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:473893e2630d47f20de5be30e39adabfcd784d4b5b5df63eaea74246bf43c66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ade24fa6e6c1b931e41fa20be0241b1b868b62d844911fcf64d21f423f0c84`

```dockerfile
```

-	Layers:
	-	`sha256:d1e9fd7becf5945b33fc6dd4fa3daa07bcee9a01c6a83c658e6acef29da901cb`  
		Last Modified: Thu, 18 Dec 2025 00:20:46 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73c4ebab1b452e6752cc732cf9cfd3842e8d485073df84caa952a02909134fa`  
		Last Modified: Thu, 18 Dec 2025 00:20:47 GMT  
		Size: 17.8 KB (17795 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:cfe2cc8633f9d8c03984fc9cc2250ab3e32bcc2220d355e45e35dd68b9bad774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118243665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776349d3680708857004cf0a881a87f4dea7af7e3b6905b1bd5b915a5515b425`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:56 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:55:31 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:55:31 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:55:31 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:55:31 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:55:31 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:55:31 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191ed597af36e20c4e341347d9aae17df8f44181f0198d35ae4104b1fa8301f5`  
		Last Modified: Wed, 17 Dec 2025 23:55:32 GMT  
		Size: 6.7 MB (6676586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386868f6cc91a80987c4eb312890d52e0551569d3d9f59e90df2d87577c907e5`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b26028ef8d9d1265ddfca6921c63b32b2491093546577849a7ad3a3c4cf539d`  
		Last Modified: Wed, 17 Dec 2025 23:56:01 GMT  
		Size: 82.7 MB (82700801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be273fcd50c97b84052fb6268ed901d9f30c4756840910ccaa3edb6c1b17c73c`  
		Last Modified: Wed, 17 Dec 2025 23:55:53 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e75308189e7e14eaa1e12c82d79c1a573291a6d830fd8a34e9b3547e61c659`  
		Last Modified: Wed, 17 Dec 2025 23:55:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:8c308538d22818fbc58e3c3fa13e08ba71c590e8f361eaba0eab79507139a8e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad3fd895b5744d5ce8f752dadc6efb69df22e784801d63f07d3b0e415c06f85`

```dockerfile
```

-	Layers:
	-	`sha256:6d4853809421861d33841f7ca0bf70386efe1246fe777635ccb62180c8f8a86a`  
		Last Modified: Thu, 18 Dec 2025 00:20:52 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9400f28461d88c04ce7bd0a602c7ed9ce05b1ff2f90418a7945a02b72e08d9db`  
		Last Modified: Thu, 18 Dec 2025 00:20:53 GMT  
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
		Last Modified: Thu, 11 Dec 2025 21:22:08 GMT  
		Size: 9.9 MB (9862216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71475ef0f8f2c5f8c394cdda52333392709fc87e769397a0389fb1bb743d399b`  
		Last Modified: Thu, 11 Dec 2025 21:22:08 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315475c1c17f7a223ea2b8a1d9a1985ce438a3bae2dae153555a5d457b051c1`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc9021d0ef61725243ae72546a2a75243c5424fa7d0fc53f20c469d377cba3`  
		Last Modified: Thu, 11 Dec 2025 21:22:13 GMT  
		Size: 50.4 MB (50447116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c548f8f09a0ce506a8c2e69d75de76926e996dfe9a46448c756d6647e8a04c`  
		Last Modified: Thu, 11 Dec 2025 21:22:08 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e504a5513a054282de4e3d4006c910c7003f8804e45058cf073a0422f0212d1`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d818200c6c4e7df4884a358b6f80bca9c959914eced87214ae2c44e58fd35b`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
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
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce46991d2c4c48fd52d13891e1b5eb0777120c6d83d07fcc82f06c4340cfb6ba`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af32475cc26ad10355d0ebd8d9c80f88c7f6c44bcf28115edc647d31b95f9884`  
		Last Modified: Thu, 11 Dec 2025 21:22:06 GMT  
		Size: 9.8 MB (9822470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaafcce51f3333786fe19ee810e7107ca5c17a1a11e4b278b34d6d8989811de7`  
		Last Modified: Thu, 11 Dec 2025 21:22:06 GMT  
		Size: 5.8 MB (5790439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b70514028425c28cf39d8baef11c310457123a628d37c437bd6661fbaad6e`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f20cada75ad84d27130c93e200a873f7b2f5078d5a2049be4894b3a568aa4`  
		Last Modified: Thu, 11 Dec 2025 21:22:10 GMT  
		Size: 48.2 MB (48229359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea275cc0d43ac8b796329c90b2d0397003fdf129d2fa4b0c407b9ffb957177b`  
		Last Modified: Thu, 11 Dec 2025 21:22:11 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f18f15a6ac7b5a0a7673d362af6cd43b52cfe07914127acffa738249bb566cd`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de188f5486eb8567f178074e890509083cc993bcfb3a37457dd2300060ec14ff`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abede7ea0d56bd3a18f4443dc825494ff3d4993f87fee95b61f6d3153eb3f702`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
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
$ docker pull influxdb@sha256:0452079f02f4d13fe3fbb74df3df9aefc902f58242c1b423a4d2cfb57346e199
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:88655683b666037d4d999619f0bf89959411fccf709ec5acd4e730ddcd0112b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119310544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b838c638c71c34d958e76f4eb357de3a965a3f81555e378155705660629c1f`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:54:04 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:54:04 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:54:04 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:54:04 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9dea577090dac77be07b9cc74c6237c4d4a29e624c7253d32ae21d6f196ae8`  
		Last Modified: Wed, 17 Dec 2025 23:54:31 GMT  
		Size: 6.7 MB (6666136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b7260fb8b9949df8a568a2ab08ec327f75e8de23a1c7832b91a8b59a9eeac2`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394211902e5963e29110b161e250c43839f38bbd8bf032f1f5ef5f2f518c03bf`  
		Last Modified: Wed, 17 Dec 2025 23:54:37 GMT  
		Size: 82.9 MB (82915390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27765a5b9cf865533049b2b3be0a97ae30367882b22cc708748594b5230d0c1`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de81e7d91528b57cc4c9461a0bd36737cecd98c4fdf6f346abfec658c7a6f6f5`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3a6632fbd2a97ccd27b651f4454a24353669d4e980fa305fe066f4ef9e086b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9020c2dd74bccec277cd1c5f5bbab2296e81432aa76e46a9ef5db211e8af7c1`

```dockerfile
```

-	Layers:
	-	`sha256:8253ae625ade4876b9ae4480b1fff70214e61d8395a8d4453134212328c6620c`  
		Last Modified: Thu, 18 Dec 2025 00:20:37 GMT  
		Size: 2.3 MB (2310563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77fe49c85f11dbbbd310dbb808989a7dd67d8b6db212d8b5d2f9a8bd97947934`  
		Last Modified: Thu, 18 Dec 2025 00:20:37 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a30cb2b6575a0b2523585b72d3eb7ea49ba05abab0e43f2cc4e949fc23f833c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110019558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a45979608e2b37df510a125528eae572058c793c79eae7abd4ca0e7a14f3792`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:56 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:55:02 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:55:02 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:55:02 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:55:02 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191ed597af36e20c4e341347d9aae17df8f44181f0198d35ae4104b1fa8301f5`  
		Last Modified: Wed, 17 Dec 2025 23:55:32 GMT  
		Size: 6.7 MB (6676586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386868f6cc91a80987c4eb312890d52e0551569d3d9f59e90df2d87577c907e5`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525e1f297447837d6c81237bfc442d0980ecb9b40ce037ec9e8fa289c41f07ff`  
		Last Modified: Wed, 17 Dec 2025 23:55:36 GMT  
		Size: 74.5 MB (74476691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ceae49e12bfe8d10edf42dc95afcd410bb8bb9967d0c7fb621c7443dc58fd0`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdcc23b7614d8487daf0da2c16fe1a93557dbc9746db244c5aeae1943a39a5f`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:873150c7b0d9db1020675db32a25bdb111e7fcb72a9187c83ee6bdeb894a888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf92ef1265a6d4fedb6780ffe8e5099731b2a6b03a5767327e9b7b11564c5cbc`

```dockerfile
```

-	Layers:
	-	`sha256:2addf4befe7a325f7f12fe579dacba5749a6a51ffd81e4d600a3a89acbb076b7`  
		Last Modified: Thu, 18 Dec 2025 00:20:42 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd287962a95203141b8d424e36a291c7eb4855f3aef923fcb730c2a1ad6bc72`  
		Last Modified: Thu, 18 Dec 2025 00:20:43 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:data`

```console
$ docker pull influxdb@sha256:48c52be245532f368ef410e1116638665b77aa2d32fc6098afa2f188a3adbf52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:59ff0c552413774b3d6b385faae73eb305a023eb4185c1b715ddd09f3a28f201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114827586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a43cbebfe667441d3f471acc3de4203c13b3e4855e1b47c2d5c1dd5ef03e2eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Dec 2025 01:31:18 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Dec 2025 01:31:18 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:31:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:31:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4703e68bd36f5bcb8b2214bab1bbb6ba374a5c20c043154da748f3361921dd`  
		Last Modified: Tue, 30 Dec 2025 01:31:43 GMT  
		Size: 42.3 MB (42315670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41017fe2f59e61beba6e4c0a2d83b618810945b92af80b28894f51be37d86051`  
		Last Modified: Tue, 30 Dec 2025 01:31:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1660405a86b92ee6b29340ec8076f9cc40e0f3ddebc4cb6f55dd2ed21de5ad0a`  
		Last Modified: Tue, 30 Dec 2025 01:31:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8b0220b4de5db27d8578d560c61c069579680553c7bd4de3421fa45cb19ffc`  
		Last Modified: Tue, 30 Dec 2025 01:31:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:b776b538cdbd99fa57093351c24de79ccc588a9473f49ef51726368cb46f5f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874ed27b2a5144ac9452ccc025be647aca0a231354bd6fef1200ccf51a9954ac`

```dockerfile
```

-	Layers:
	-	`sha256:abd6d9c653d6411a9471bb744ee4b2a895594421861c2e10bb06fa1d1db73ee9`  
		Last Modified: Tue, 30 Dec 2025 06:21:03 GMT  
		Size: 4.7 MB (4685451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27131ca66cd9a9515bd87afd32c5d0c14dc2e042ccb2120638b47804cd6aeab5`  
		Last Modified: Tue, 30 Dec 2025 06:21:04 GMT  
		Size: 13.8 KB (13779 bytes)  
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
		Last Modified: Tue, 09 Dec 2025 22:33:29 GMT  
		Size: 1.2 MB (1225329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e0170f82fea093122d3570e0d358e936d1db98ed05a0d6a48d33037501b351`  
		Last Modified: Tue, 09 Dec 2025 22:33:31 GMT  
		Size: 42.3 MB (42254311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b0661d8dbfc3b43d49ec386e18c197ae353dd5d5c77c548207da941ba2ee68`  
		Last Modified: Mon, 15 Dec 2025 19:34:03 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39225506d3b8f10fd5e6623059b8c1e0d7efadec626f71dcf9da78fee4f7e2a`  
		Last Modified: Tue, 09 Dec 2025 22:33:28 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d72d987f87daa2925154010870639046590c11fa247eb8c38fdd2ea9c6094b`  
		Last Modified: Mon, 15 Dec 2025 19:34:04 GMT  
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
		Last Modified: Mon, 15 Dec 2025 19:34:04 GMT  
		Size: 15.2 KB (15191 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:3df4ecc96e2136585b25beea47e4f164469059a72714d646096cbdfb639b64b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:adc291da58fa13d386afb400a77f324b816fbed5858b3bb8d4018bfbe0fd4027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127590250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806ba4c62d2e005744a021183e0a15960a6778fcb4811f94905666a688032f23`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:54:31 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:54:31 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:54:31 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:54:31 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:54:31 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:54:31 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:54:31 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9dea577090dac77be07b9cc74c6237c4d4a29e624c7253d32ae21d6f196ae8`  
		Last Modified: Wed, 17 Dec 2025 23:54:31 GMT  
		Size: 6.7 MB (6666136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b7260fb8b9949df8a568a2ab08ec327f75e8de23a1c7832b91a8b59a9eeac2`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39532d39a98bcd3d51104687002cdf5339a387cc074fd54a8b168ca0d6d5861`  
		Last Modified: Wed, 17 Dec 2025 23:55:04 GMT  
		Size: 91.2 MB (91195097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02fbf1ae289239b1f1d60ce260e4d88a0380d638c1a62a8f4835e7b02d93eb`  
		Last Modified: Wed, 17 Dec 2025 23:54:53 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078288b9048f2c197b8f944e7d235c4d0125ee27e137627bc3e6157da1c49442`  
		Last Modified: Wed, 17 Dec 2025 23:54:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:473893e2630d47f20de5be30e39adabfcd784d4b5b5df63eaea74246bf43c66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ade24fa6e6c1b931e41fa20be0241b1b868b62d844911fcf64d21f423f0c84`

```dockerfile
```

-	Layers:
	-	`sha256:d1e9fd7becf5945b33fc6dd4fa3daa07bcee9a01c6a83c658e6acef29da901cb`  
		Last Modified: Thu, 18 Dec 2025 00:20:46 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73c4ebab1b452e6752cc732cf9cfd3842e8d485073df84caa952a02909134fa`  
		Last Modified: Thu, 18 Dec 2025 00:20:47 GMT  
		Size: 17.8 KB (17795 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:cfe2cc8633f9d8c03984fc9cc2250ab3e32bcc2220d355e45e35dd68b9bad774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118243665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776349d3680708857004cf0a881a87f4dea7af7e3b6905b1bd5b915a5515b425`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 17 Dec 2025 23:54:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:56 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:55:31 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:55:31 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:55:31 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:55:31 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:55:31 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:55:31 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:55:31 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191ed597af36e20c4e341347d9aae17df8f44181f0198d35ae4104b1fa8301f5`  
		Last Modified: Wed, 17 Dec 2025 23:55:32 GMT  
		Size: 6.7 MB (6676586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386868f6cc91a80987c4eb312890d52e0551569d3d9f59e90df2d87577c907e5`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b26028ef8d9d1265ddfca6921c63b32b2491093546577849a7ad3a3c4cf539d`  
		Last Modified: Wed, 17 Dec 2025 23:56:01 GMT  
		Size: 82.7 MB (82700801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be273fcd50c97b84052fb6268ed901d9f30c4756840910ccaa3edb6c1b17c73c`  
		Last Modified: Wed, 17 Dec 2025 23:55:53 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e75308189e7e14eaa1e12c82d79c1a573291a6d830fd8a34e9b3547e61c659`  
		Last Modified: Wed, 17 Dec 2025 23:55:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:8c308538d22818fbc58e3c3fa13e08ba71c590e8f361eaba0eab79507139a8e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad3fd895b5744d5ce8f752dadc6efb69df22e784801d63f07d3b0e415c06f85`

```dockerfile
```

-	Layers:
	-	`sha256:6d4853809421861d33841f7ca0bf70386efe1246fe777635ccb62180c8f8a86a`  
		Last Modified: Thu, 18 Dec 2025 00:20:52 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9400f28461d88c04ce7bd0a602c7ed9ce05b1ff2f90418a7945a02b72e08d9db`  
		Last Modified: Thu, 18 Dec 2025 00:20:53 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:9e967a2283f54ecd401377f1ed677c882adc23dd4090fb5f0c7ebe98a8138a8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:cd9338522e3d5c507d281f031c99bf7553a28f5c0f599906518dd9851b384e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107224041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3408898af3df5a76c9a579faaf938d8a72178a7d1559302d8f85053d7a44f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:54:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:54:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 29 Dec 2025 23:54:58 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 29 Dec 2025 23:54:59 GMT
ENV GOSU_VER=1.19
# Mon, 29 Dec 2025 23:54:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:54:59 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 29 Dec 2025 23:54:59 GMT
ENV INFLUXDB_PR=-2
# Mon, 29 Dec 2025 23:54:59 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 29 Dec 2025 23:55:03 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 29 Dec 2025 23:55:03 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 29 Dec 2025 23:55:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 29 Dec 2025 23:55:04 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:55:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:55:04 GMT
CMD ["influxd"]
# Mon, 29 Dec 2025 23:55:04 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 29 Dec 2025 23:55:04 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 29 Dec 2025 23:55:04 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 29 Dec 2025 23:55:04 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 29 Dec 2025 23:55:04 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3eda513cda0dfb20cda875b352884f5f9032b1bad8cfd33b31bba3bfc4f079`  
		Last Modified: Mon, 29 Dec 2025 23:55:25 GMT  
		Size: 9.8 MB (9796291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2cc7314c76b61ace608bf8ce61fc60e2b8693ce32f76ea3695174aebdcc99e`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ced5038ff2dee1ab3a4fe7787b10f38a0f1dbe8f9719d6d98eca37538794b75`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fffb9e985775c37ccd426ddf9f40006fe74df96168e05188652d15c19bbee8`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 811.5 KB (811473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4b92236f46aac610b9dd8642f9d6c68d23ace8339918a777d8a670e4cdeba2`  
		Last Modified: Mon, 29 Dec 2025 23:55:29 GMT  
		Size: 50.4 MB (50447138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbce1186b18e56e3f22a64ec3f4a2ce82f33b46838ee5cefaeb83ffb0c4d4208`  
		Last Modified: Mon, 29 Dec 2025 23:55:25 GMT  
		Size: 11.8 MB (11773790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfc177b3dcd07b0056741edc461eaab058036e61f464b7b8d35de48a8fbae47`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6553a5f188eded8c1d292b51539522875b491fb29a92c351091de39ca27189`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5540325d51e4aeda9c6c8021fba87d440e37147d513355886c1ba5c102ae2f`  
		Last Modified: Mon, 29 Dec 2025 23:55:24 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:6f946b312bf6b20a645d8cddfbb09bc81d0505515c8567b65c029a3500667f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a91951ab76298fccacefe4325b019cc6f16b12ed29038953cdc96190a784026`

```dockerfile
```

-	Layers:
	-	`sha256:65a1a3c4a54968fa4ab83e6375a19c9f31ef036bca8ca95f879606ceeb022f3a`  
		Last Modified: Tue, 30 Dec 2025 03:21:20 GMT  
		Size: 2.9 MB (2934227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b0cb0c2e3ef255c3c89ff570ddb7d8ec40e39ebcbf3b28a69c72bb0f3dd1227`  
		Last Modified: Tue, 30 Dec 2025 03:21:20 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:7d7288ba3a2827317f23ca682ee89d82c67b8886fb16b9eadd760c219542dd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103624752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14e20f215b379fe4f34b2e5c673986e33fe384442c1191723c7cc2bc44d1e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:56:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:56:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 29 Dec 2025 23:56:11 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 29 Dec 2025 23:56:12 GMT
ENV GOSU_VER=1.19
# Mon, 29 Dec 2025 23:56:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:56:12 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 29 Dec 2025 23:56:12 GMT
ENV INFLUXDB_PR=-2
# Mon, 29 Dec 2025 23:56:12 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 29 Dec 2025 23:56:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 29 Dec 2025 23:56:16 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 29 Dec 2025 23:56:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 29 Dec 2025 23:56:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:56:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:56:17 GMT
CMD ["influxd"]
# Mon, 29 Dec 2025 23:56:17 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 29 Dec 2025 23:56:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 29 Dec 2025 23:56:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 29 Dec 2025 23:56:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 29 Dec 2025 23:56:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2476917a5ea8832eb4f0ccb76bdf7f15d39e870e85c993e2824d21ebd21d80`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 9.6 MB (9626427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297409a2ba01c8ae930ab72e0cc776bd9e9b13780a1105208f20d437597ceb1d`  
		Last Modified: Mon, 29 Dec 2025 23:56:38 GMT  
		Size: 5.8 MB (5790401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a4bee7cf9792245fcffb60ef6ac8c43ac4e378e02d0b2c7fe104c044b84df9`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a67094e0b44d7b3294fc80e471c424c2f5dd2f125cf7dc63807b480448dc390`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 766.4 KB (766364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7208972ac46056e1f195f137e14374336c343a7da096d5c5e3a04e449d7d391a`  
		Last Modified: Mon, 29 Dec 2025 23:56:44 GMT  
		Size: 48.2 MB (48229404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82919091c9e4cb426deb55ae9dd4046c2e10d7106fd2c221abba170dfb6e013f`  
		Last Modified: Mon, 29 Dec 2025 23:56:38 GMT  
		Size: 11.1 MB (11099995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62de181bab838309f47cb36555a248525d527656ca1811404c29cbffaa64640`  
		Last Modified: Mon, 29 Dec 2025 23:56:40 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d852dd88b22838dc3b0f3fe973f7fca4de7e98fe5498e9b45946b99cc944390f`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813cb2d2c0591cc7bebf34b7ac9adec9eecda6617a91dbee62fa49e1fb790276`  
		Last Modified: Mon, 29 Dec 2025 23:56:37 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:cd24e284afb5aebe35d7c24dcd0c94928cfc7cc5ea688c187bac54d8c7a2bf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ee92d9efbfd8a46ef5c0c9b592c00fade820b6b10c843fd163076184744be0`

```dockerfile
```

-	Layers:
	-	`sha256:76a8e1c7bf83b6ab8a38b0b4e219b6d3b8d02a2df2532aa1a40f3b516bcd029b`  
		Last Modified: Tue, 30 Dec 2025 03:21:24 GMT  
		Size: 2.9 MB (2933707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601dfd7508e497db9e6c80458304b1656f8e43f9a4591c72621f694cdb21b546`  
		Last Modified: Tue, 30 Dec 2025 03:21:25 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:a0f9c61dc18ed8aefd14d5038d3ca12a98c2761518c24728c4d03f92eae05ad5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:b8d5353f82e2bcc9fabca62cba9ba7876392cb4c0d264632ad973591fd290736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91289725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9718ab8f0c96d9df0ca5ccac148026aeffc54aa8d69a6065947040a2c6e8accd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Dec 2025 01:31:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Dec 2025 01:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:31:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fac420b8d1add9a518c8be0cadbd02cf2b0d721e683660ab29558b57a53f39e`  
		Last Modified: Tue, 30 Dec 2025 01:31:57 GMT  
		Size: 18.8 MB (18779017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e85d0585009faa68a9368aae4bc84c767729a35826873821dfbc4aa6141e2b5`  
		Last Modified: Tue, 30 Dec 2025 01:31:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefee4201d499772783be5a913f67391bb488eff5f377af4f36a20755a5932a5`  
		Last Modified: Tue, 30 Dec 2025 01:31:56 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:97fd89bcfe95081acf6933a13aba093f1c0e44b2f8d66558881dbf209b861d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4602907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd5fb5e2737dbc4eeaad475dc69ad7263fd7b4e523f9efaa0a340db32911432`

```dockerfile
```

-	Layers:
	-	`sha256:5e1e2fa8558e6841daae3568cdf28ed1410c6d2d55f39e4eae5943032a64bbe7`  
		Last Modified: Tue, 30 Dec 2025 06:21:08 GMT  
		Size: 4.6 MB (4590614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d7e461b14c9d975dd22648bf2177071baab81c1c357c7d7e280b6ea515e3d3c`  
		Last Modified: Tue, 30 Dec 2025 06:21:09 GMT  
		Size: 12.3 KB (12293 bytes)  
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
		Last Modified: Mon, 15 Dec 2025 20:39:36 GMT  
		Size: 1.2 MB (1225337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8df8f8e418a27917114426b3d245a3728772fe30be9e1b0b609e79b9ccb3b1d`  
		Last Modified: Mon, 15 Dec 2025 20:39:39 GMT  
		Size: 18.7 MB (18722501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96fdeefb85b445c179f78bb53968e8210d7aaa4a30cccb4d6452d9ac4a7b000`  
		Last Modified: Fri, 12 Dec 2025 22:35:31 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5817ad78e6b46e06d7f07b733f09a0eddd15b789d78398b86fe406d8cd2fdf7`  
		Last Modified: Tue, 09 Dec 2025 22:35:17 GMT  
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
