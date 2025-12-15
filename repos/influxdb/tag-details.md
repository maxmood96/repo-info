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
-	[`influxdb:3.7-core`](#influxdb37-core)
-	[`influxdb:3.7-enterprise`](#influxdb37-enterprise)
-	[`influxdb:3.7.0-core`](#influxdb370-core)
-	[`influxdb:3.7.0-enterprise`](#influxdb370-enterprise)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:core`](#influxdbcore)
-	[`influxdb:enterprise`](#influxdbenterprise)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.11`

```console
$ docker pull influxdb@sha256:f9b63c62cb77cdd0216ede4869784ebeed2267c96983ce12d1beba530b271533
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:d527c54a7ebbb0f2c8d55505321cc36ce16347b8ecb6a7efb02b7681d1bed15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116168191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe3678315a7f107fcb0fa51f6ab5ad9adcf7c419170b68e0e7527e746cd8d01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:46 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 09 Dec 2025 00:13:53 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 09 Dec 2025 00:13:53 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:13:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
USER influxdb
# Tue, 09 Dec 2025 00:13:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:13:53 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e0dc48fa97184d26fb2dbbf536c2608e06d3f2e5627070c933f9878dbcd22f`  
		Last Modified: Tue, 09 Dec 2025 00:14:15 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b918297aa52cc1743aa971dcfb7de253ce602baa7e2e625792f1d180f9a4a77`  
		Last Modified: Tue, 09 Dec 2025 00:14:22 GMT  
		Size: 43.7 MB (43655200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345617bdf91e26776b4da03f4c11238cb2ed195338a485f00f599f813003be0e`  
		Last Modified: Tue, 09 Dec 2025 00:14:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c219760b9292bea82b23403a0c0acc1b32e275ebefa599bc2624312620e2e046`  
		Last Modified: Tue, 09 Dec 2025 00:14:14 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714cc21560861380b272247fa06d5fa7542b9d78e91c0abfba106cbe64d07780`  
		Last Modified: Tue, 09 Dec 2025 00:14:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:58cd9a5aedf3a839659df97b86864d305c729ad8d7efd936569c796c946abd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228f723366c7221880f945247ab17d574efe342a33ee7942bf7c43a4f5a929cb`

```dockerfile
```

-	Layers:
	-	`sha256:6bd5521da43b239dcfb00e37ea12893e6958bb3bdc44400354f8dc0b9c87c4d9`  
		Last Modified: Tue, 09 Dec 2025 03:21:05 GMT  
		Size: 5.1 MB (5078620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caad7ccc330d7952677b98ae790fecbf9cbebcff61e46770020877ea446a6ad0`  
		Last Modified: Tue, 09 Dec 2025 03:21:06 GMT  
		Size: 15.5 KB (15486 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:120524bdf151ac697eba4fa7cbabfcc6781687f424d729eea9420c9dd060d4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113078954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598e6c65af502a323967627eb0789206341e2026bc5932eda153729cf89e8d58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:19:03 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 09 Dec 2025 00:19:10 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 09 Dec 2025 00:19:10 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:19:10 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 09 Dec 2025 00:19:10 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 09 Dec 2025 00:19:10 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:19:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:19:10 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 09 Dec 2025 00:19:10 GMT
USER influxdb
# Tue, 09 Dec 2025 00:19:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:19:10 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110a2896486a30cea3290077383acda67ec2618cbbd3fafa6f21a0c80e23ec14`  
		Last Modified: Tue, 09 Dec 2025 00:19:30 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20643ba39f8f2face9ed32187173792d8f8b61c5586c492bf73b4a78d2f13600`  
		Last Modified: Tue, 09 Dec 2025 00:19:33 GMT  
		Size: 41.1 MB (41118729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e65e3b5541a0af05a1aa704cf00ba6355ec2b11f15450172c9c7c14a33a96a`  
		Last Modified: Tue, 09 Dec 2025 00:19:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4687f76b162a29fb23e77ffb6e9b81f99dd2c0288b8eb281200b3039dc7779`  
		Last Modified: Tue, 09 Dec 2025 00:19:30 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d5a5499335f9471aa5684efce5773efd30a47aff43bf0b57071427db0d7318`  
		Last Modified: Tue, 09 Dec 2025 00:19:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:6f64674f65917452a4777158106334e7fef6ec68d716dc6155931021cd3560cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3820faf4fe46bf7e60f2d9d6597e239648aeeff20665261cc5a05fc15ccb43`

```dockerfile
```

-	Layers:
	-	`sha256:875c3325236e11165d73c7f15055315485b256073dc8c0c88d47ccd2ca1db328`  
		Last Modified: Tue, 09 Dec 2025 03:21:11 GMT  
		Size: 5.1 MB (5078085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6d1430d29d0d78400bb5f8a4ba5d49a0ae00a429b72ab042302347c79bac17`  
		Last Modified: Tue, 09 Dec 2025 03:21:12 GMT  
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
$ docker pull influxdb@sha256:f2d48c963c3cf469512b263969ecc210033f641846749d33f1c6075c223e2e93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:247eecc55cefe45150815faa524807787d6f9147ca52a2563b6bd6c4264c08e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114680961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2543c0e237b2f8acae5a76550725fafbcc3f58adadb8d0d91eb99a10bbc033e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:13:56 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 09 Dec 2025 00:13:56 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 09 Dec 2025 00:13:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 09 Dec 2025 00:13:57 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 09 Dec 2025 00:13:57 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:13:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:13:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 09 Dec 2025 00:13:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:13:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b361d3df1d2c4af136ad37840f9a790901a5fcf6cdb9cf5abed46ffa63be0b37`  
		Last Modified: Tue, 09 Dec 2025 00:14:14 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1d7e32e17036188ea2fe6d94bf75e47872dc1d95e3ef1a346301ae1b9e237c`  
		Last Modified: Tue, 09 Dec 2025 00:14:15 GMT  
		Size: 42.2 MB (42165665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5538fe37c8ab0ed5e30ab1ac3b7aca533de1117739b8a4cb85183c0c4ec311ea`  
		Last Modified: Tue, 09 Dec 2025 00:14:14 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6d4cb36faaf3e4a962ad402b0dc4856554484d0d9f2f536e0ef2da4be537d`  
		Last Modified: Tue, 09 Dec 2025 00:14:14 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e494b38f149db9399407d633d3d809ad3018ba57bec56e097d103814a3fd074`  
		Last Modified: Tue, 09 Dec 2025 00:14:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c1ac45237ba02267528b0afd09d3e370472d3d3a35ec1565c11afeed4505ead4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4698428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182c1e3aec60baaec85328694036e1da29aab48ce3936fce54a8e6e8319a1f1d`

```dockerfile
```

-	Layers:
	-	`sha256:294a971272e57008c417638597653458aa3831bd186e6183e5e9a62caa924f08`  
		Last Modified: Tue, 09 Dec 2025 03:21:17 GMT  
		Size: 4.7 MB (4683763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48ac9bce34d5cc309f73a335e45196fdb3a9d8ed4354e795123681e7e3e2fd59`  
		Last Modified: Tue, 09 Dec 2025 03:21:15 GMT  
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
$ docker pull influxdb@sha256:ea76c529502dee9467589d13be75b77b7cfd31227e5572df5760b04e3188ea95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:a69aa85ae66a40ba23524dfcba73f7503b8b2524e9ebabb4399efe030b0b5fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91110180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76c7ef43930a77f170b19bf2c4671966f763aaab584763326e4d2e944740022`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:14:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:14:04 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 09 Dec 2025 00:14:04 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 09 Dec 2025 00:14:04 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 09 Dec 2025 00:14:04 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 09 Dec 2025 00:14:04 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:14:04 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aee4668125d1f27140c8fe0c269dee3acb3744e231696f79a81542664b3f2ff`  
		Last Modified: Tue, 09 Dec 2025 00:14:20 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca864723b5599eff6e5a8c6796304fce66cd35fefb2c6d04d03b0b630fb55baa`  
		Last Modified: Tue, 09 Dec 2025 00:14:22 GMT  
		Size: 18.6 MB (18596103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13235bf6cf155558d6c740625f80c8ed2f7ccfcd8cf0c06e74fbac0b2033cd3`  
		Last Modified: Tue, 09 Dec 2025 00:14:21 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab360c3fff598268bc25ea969f90acd171024805111e27e8690a45219b4e091b`  
		Last Modified: Tue, 09 Dec 2025 00:14:20 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:08f543f8cbc138e0402252a647c348d0415eefce1497eb3d09a835096b5d47d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4603630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3bb750dad12ac6906815667be7bfed249702db0726a3c9126d5fc3b28eb0d8`

```dockerfile
```

-	Layers:
	-	`sha256:fab237f0420518e7c2e53a8dda37b2bf0d4f319e7b9f17dace9c7363626e30b3`  
		Last Modified: Tue, 09 Dec 2025 03:21:25 GMT  
		Size: 4.6 MB (4590606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:950e896c6f24fd88be0065191bb683adbd5fcd287f55385262fb1b2f4ad9de58`  
		Last Modified: Tue, 09 Dec 2025 03:21:26 GMT  
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
$ docker pull influxdb@sha256:f9b63c62cb77cdd0216ede4869784ebeed2267c96983ce12d1beba530b271533
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:d527c54a7ebbb0f2c8d55505321cc36ce16347b8ecb6a7efb02b7681d1bed15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116168191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe3678315a7f107fcb0fa51f6ab5ad9adcf7c419170b68e0e7527e746cd8d01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:46 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 09 Dec 2025 00:13:53 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 09 Dec 2025 00:13:53 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:13:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 09 Dec 2025 00:13:53 GMT
USER influxdb
# Tue, 09 Dec 2025 00:13:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:13:53 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e0dc48fa97184d26fb2dbbf536c2608e06d3f2e5627070c933f9878dbcd22f`  
		Last Modified: Tue, 09 Dec 2025 00:14:15 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b918297aa52cc1743aa971dcfb7de253ce602baa7e2e625792f1d180f9a4a77`  
		Last Modified: Tue, 09 Dec 2025 00:14:22 GMT  
		Size: 43.7 MB (43655200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345617bdf91e26776b4da03f4c11238cb2ed195338a485f00f599f813003be0e`  
		Last Modified: Tue, 09 Dec 2025 00:14:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c219760b9292bea82b23403a0c0acc1b32e275ebefa599bc2624312620e2e046`  
		Last Modified: Tue, 09 Dec 2025 00:14:14 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714cc21560861380b272247fa06d5fa7542b9d78e91c0abfba106cbe64d07780`  
		Last Modified: Tue, 09 Dec 2025 00:14:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:58cd9a5aedf3a839659df97b86864d305c729ad8d7efd936569c796c946abd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228f723366c7221880f945247ab17d574efe342a33ee7942bf7c43a4f5a929cb`

```dockerfile
```

-	Layers:
	-	`sha256:6bd5521da43b239dcfb00e37ea12893e6958bb3bdc44400354f8dc0b9c87c4d9`  
		Last Modified: Tue, 09 Dec 2025 03:21:05 GMT  
		Size: 5.1 MB (5078620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caad7ccc330d7952677b98ae790fecbf9cbebcff61e46770020877ea446a6ad0`  
		Last Modified: Tue, 09 Dec 2025 03:21:06 GMT  
		Size: 15.5 KB (15486 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:120524bdf151ac697eba4fa7cbabfcc6781687f424d729eea9420c9dd060d4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113078954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598e6c65af502a323967627eb0789206341e2026bc5932eda153729cf89e8d58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:19:03 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 09 Dec 2025 00:19:10 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 09 Dec 2025 00:19:10 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:19:10 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 09 Dec 2025 00:19:10 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 09 Dec 2025 00:19:10 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:19:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:19:10 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 09 Dec 2025 00:19:10 GMT
USER influxdb
# Tue, 09 Dec 2025 00:19:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:19:10 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110a2896486a30cea3290077383acda67ec2618cbbd3fafa6f21a0c80e23ec14`  
		Last Modified: Tue, 09 Dec 2025 00:19:30 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20643ba39f8f2face9ed32187173792d8f8b61c5586c492bf73b4a78d2f13600`  
		Last Modified: Tue, 09 Dec 2025 00:19:33 GMT  
		Size: 41.1 MB (41118729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e65e3b5541a0af05a1aa704cf00ba6355ec2b11f15450172c9c7c14a33a96a`  
		Last Modified: Tue, 09 Dec 2025 00:19:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4687f76b162a29fb23e77ffb6e9b81f99dd2c0288b8eb281200b3039dc7779`  
		Last Modified: Tue, 09 Dec 2025 00:19:30 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d5a5499335f9471aa5684efce5773efd30a47aff43bf0b57071427db0d7318`  
		Last Modified: Tue, 09 Dec 2025 00:19:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:6f64674f65917452a4777158106334e7fef6ec68d716dc6155931021cd3560cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3820faf4fe46bf7e60f2d9d6597e239648aeeff20665261cc5a05fc15ccb43`

```dockerfile
```

-	Layers:
	-	`sha256:875c3325236e11165d73c7f15055315485b256073dc8c0c88d47ccd2ca1db328`  
		Last Modified: Tue, 09 Dec 2025 03:21:11 GMT  
		Size: 5.1 MB (5078085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6d1430d29d0d78400bb5f8a4ba5d49a0ae00a429b72ab042302347c79bac17`  
		Last Modified: Tue, 09 Dec 2025 03:21:12 GMT  
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
$ docker pull influxdb@sha256:f2d48c963c3cf469512b263969ecc210033f641846749d33f1c6075c223e2e93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:247eecc55cefe45150815faa524807787d6f9147ca52a2563b6bd6c4264c08e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114680961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2543c0e237b2f8acae5a76550725fafbcc3f58adadb8d0d91eb99a10bbc033e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:13:56 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 09 Dec 2025 00:13:56 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 09 Dec 2025 00:13:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 09 Dec 2025 00:13:57 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 09 Dec 2025 00:13:57 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:13:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:13:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 09 Dec 2025 00:13:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:13:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b361d3df1d2c4af136ad37840f9a790901a5fcf6cdb9cf5abed46ffa63be0b37`  
		Last Modified: Tue, 09 Dec 2025 00:14:14 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1d7e32e17036188ea2fe6d94bf75e47872dc1d95e3ef1a346301ae1b9e237c`  
		Last Modified: Tue, 09 Dec 2025 00:14:15 GMT  
		Size: 42.2 MB (42165665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5538fe37c8ab0ed5e30ab1ac3b7aca533de1117739b8a4cb85183c0c4ec311ea`  
		Last Modified: Tue, 09 Dec 2025 00:14:14 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a6d4cb36faaf3e4a962ad402b0dc4856554484d0d9f2f536e0ef2da4be537d`  
		Last Modified: Tue, 09 Dec 2025 00:14:14 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e494b38f149db9399407d633d3d809ad3018ba57bec56e097d103814a3fd074`  
		Last Modified: Tue, 09 Dec 2025 00:14:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c1ac45237ba02267528b0afd09d3e370472d3d3a35ec1565c11afeed4505ead4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4698428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182c1e3aec60baaec85328694036e1da29aab48ce3936fce54a8e6e8319a1f1d`

```dockerfile
```

-	Layers:
	-	`sha256:294a971272e57008c417638597653458aa3831bd186e6183e5e9a62caa924f08`  
		Last Modified: Tue, 09 Dec 2025 03:21:17 GMT  
		Size: 4.7 MB (4683763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48ac9bce34d5cc309f73a335e45196fdb3a9d8ed4354e795123681e7e3e2fd59`  
		Last Modified: Tue, 09 Dec 2025 03:21:15 GMT  
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
$ docker pull influxdb@sha256:ea76c529502dee9467589d13be75b77b7cfd31227e5572df5760b04e3188ea95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:a69aa85ae66a40ba23524dfcba73f7503b8b2524e9ebabb4399efe030b0b5fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91110180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76c7ef43930a77f170b19bf2c4671966f763aaab584763326e4d2e944740022`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:14:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:14:04 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 09 Dec 2025 00:14:04 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 09 Dec 2025 00:14:04 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 09 Dec 2025 00:14:04 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 09 Dec 2025 00:14:04 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:14:04 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aee4668125d1f27140c8fe0c269dee3acb3744e231696f79a81542664b3f2ff`  
		Last Modified: Tue, 09 Dec 2025 00:14:20 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca864723b5599eff6e5a8c6796304fce66cd35fefb2c6d04d03b0b630fb55baa`  
		Last Modified: Tue, 09 Dec 2025 00:14:22 GMT  
		Size: 18.6 MB (18596103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13235bf6cf155558d6c740625f80c8ed2f7ccfcd8cf0c06e74fbac0b2033cd3`  
		Last Modified: Tue, 09 Dec 2025 00:14:21 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab360c3fff598268bc25ea969f90acd171024805111e27e8690a45219b4e091b`  
		Last Modified: Tue, 09 Dec 2025 00:14:20 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:08f543f8cbc138e0402252a647c348d0415eefce1497eb3d09a835096b5d47d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4603630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3bb750dad12ac6906815667be7bfed249702db0726a3c9126d5fc3b28eb0d8`

```dockerfile
```

-	Layers:
	-	`sha256:fab237f0420518e7c2e53a8dda37b2bf0d4f319e7b9f17dace9c7363626e30b3`  
		Last Modified: Tue, 09 Dec 2025 03:21:25 GMT  
		Size: 4.6 MB (4590606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:950e896c6f24fd88be0065191bb683adbd5fcd287f55385262fb1b2f4ad9de58`  
		Last Modified: Tue, 09 Dec 2025 03:21:26 GMT  
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
$ docker pull influxdb@sha256:62a9fa847313a43d3ac11c1eb7b32676dde555a58d8d9de39dcbec62abf4a00f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12` - linux; amd64

```console
$ docker pull influxdb@sha256:16b82f03c99c52cff38383eff71b63668c44ead78fa100143848734559050b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113843321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6def1d57c5b7e5219288ace57fdcce389cd8185047e653577e9c4e47b0ec255`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:20 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 09 Dec 2025 00:13:25 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 09 Dec 2025 00:13:25 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:13:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
USER influxdb
# Tue, 09 Dec 2025 00:13:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:13:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6669fb2e9f61972e6fcd1e9ac7fcf0a5aa961dc413d84622b902f85d8fea42d`  
		Last Modified: Tue, 09 Dec 2025 00:13:46 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7f6d4419f522b29083240d811449358aaefa03da13fe664e5d65fe2b6d62d`  
		Last Modified: Tue, 09 Dec 2025 00:13:55 GMT  
		Size: 41.3 MB (41330326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4720bea0f108c0cbcfad2080a807b74d9e055e2f53c6bbe93396bd755779a18`  
		Last Modified: Tue, 09 Dec 2025 00:13:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0898c1139248ed67e9c0f0684c5ddec4671cccf1ed1955be761a31ce714e4ebc`  
		Last Modified: Tue, 09 Dec 2025 00:13:47 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8387f1aa93856fa89528cd5bcee576362facb896378b6e8e52fd77e0477a67`  
		Last Modified: Tue, 09 Dec 2025 00:13:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:38c5f487deb9d5e6c66779df8301046311043dc00cd19f362b76ec746191f0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae02be10047c064bfd3cb3534bd1a5a99d87e31a98d2be358bf44f1960e784b`

```dockerfile
```

-	Layers:
	-	`sha256:322331315e89f3fdb4be3d120672d9177002226317dec69ff0ba8fdf3b1dd2cb`  
		Last Modified: Tue, 09 Dec 2025 03:21:32 GMT  
		Size: 4.7 MB (4675813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79242889e7c5ae8259f0f42e44b806b34af7e58c5f2844d34a8cd0467f77228c`  
		Last Modified: Tue, 09 Dec 2025 03:21:32 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:11fc09c440d56e948dbcf54497c854a42f277b72b34271d7a2ec4106e7d4e2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110091058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8deb5c85c854ae71ce43181dcdc7a484fb5a5e6317ef1bc0c661f0e70747e3f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:19:01 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 09 Dec 2025 00:19:05 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 09 Dec 2025 00:19:05 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:19:05 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 09 Dec 2025 00:19:05 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 09 Dec 2025 00:19:05 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:19:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:19:05 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 09 Dec 2025 00:19:05 GMT
USER influxdb
# Tue, 09 Dec 2025 00:19:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:19:05 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca4be8a5364f21221ab6e74dae63da367a4a35bb9ff94d72b497b9e8540ae2d`  
		Last Modified: Tue, 09 Dec 2025 00:19:26 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bc9fb62888315b1768a3b73182cd5c73d9560c3c280dec4a51e53d7cbb1098`  
		Last Modified: Tue, 09 Dec 2025 00:19:28 GMT  
		Size: 38.1 MB (38130833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab842a1a7e1450b7f4a77bac29510a474505210916d065982fbf4657ee3e464`  
		Last Modified: Tue, 09 Dec 2025 00:19:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712935c4849e9c78a1fb08d694556a138993722f3313820558f0adf71dc0af8a`  
		Last Modified: Tue, 09 Dec 2025 00:19:26 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ee2b4054586b69ec7c98412fcbd9fed4c0a1457d05b8c0c8a41f4e9a030ed3`  
		Last Modified: Tue, 09 Dec 2025 00:19:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:9d649d33596da37270f666dacf41353f3c8d9f27dc889daaa078b8fd8bd5f69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4691822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2c59cce2c860496c1662fd0674d9d56f9201d5c8174a3be05980c06083b6a7`

```dockerfile
```

-	Layers:
	-	`sha256:6382d8157148d926eaa42e94c0d9a87e48fc9f775616fe4965c0e03e28247c96`  
		Last Modified: Tue, 09 Dec 2025 03:21:38 GMT  
		Size: 4.7 MB (4675271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55aab66676b4a948334d90e07f603218039e54458b4fc79798e2aa66a305d07f`  
		Last Modified: Tue, 09 Dec 2025 03:21:39 GMT  
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
$ docker pull influxdb@sha256:e8a574ce503156ed8fecac8feed3f952282b65d3e20e35b5bb47bb0e60bd63d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data` - linux; amd64

```console
$ docker pull influxdb@sha256:00e3df17fba12a953e593daf7b890b8078b847bb0ac37adc6c767eada370eea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114827569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b645bc755492e0b2ccd0126e43b1fdc461ec0d6306bf059f3fac330875ae873f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 09 Dec 2025 00:13:25 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 09 Dec 2025 00:13:25 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:13:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:13:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e916812f000712a61a547dcf5a393753b5639011592379d68acf836c464eda9`  
		Last Modified: Tue, 09 Dec 2025 00:13:52 GMT  
		Size: 42.3 MB (42315721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0d6d67762a417689a0d89eb5a12366e8c4b66dd155553721070e5101f910f3`  
		Last Modified: Tue, 09 Dec 2025 00:13:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd43f4fc0a04235fb7631c2f6200cc481f2dc02ac3da80dc23868ab9b49b0beb`  
		Last Modified: Tue, 09 Dec 2025 00:55:31 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8387f1aa93856fa89528cd5bcee576362facb896378b6e8e52fd77e0477a67`  
		Last Modified: Tue, 09 Dec 2025 00:13:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:649e6433ae5c491e8d08d296d7834e465d939a0503a5f06f3560a70c55147bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df00214c73b515df69f814418ecbe8a4a7485bb92424e1701758293818304c2`

```dockerfile
```

-	Layers:
	-	`sha256:59637e5306820301584616d5d3b49c5eadaab186dd2911493496d507836be2f0`  
		Last Modified: Tue, 09 Dec 2025 03:21:38 GMT  
		Size: 4.7 MB (4685451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf46c667a193fc9afac3f4e5e5ab08796e08ab95db622dd9ae160630e6f0be0a`  
		Last Modified: Tue, 09 Dec 2025 03:21:39 GMT  
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
$ docker pull influxdb@sha256:3a104bdc74287a29834b1e74a69683d5cfa8dea8dbaf1c79e8bf0018ed4e3067
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:7df4751660b4e0734a9b724805b7d69a9473b2490211cc6c56f820560a290832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91289660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569505e86cd5ad9eac7a12768fe281a1a9eab54ba3da86ad8a220c5ded5870d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:33 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 09 Dec 2025 00:13:33 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:33 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 09 Dec 2025 00:13:33 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 09 Dec 2025 00:13:33 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:13:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:13:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:13:33 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3eafc770dfb591ed0b943cc86a60503653b87707274904ae7f357e1313aa`  
		Last Modified: Tue, 09 Dec 2025 00:13:53 GMT  
		Size: 18.8 MB (18779024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94038bb0b45460f4df068a2656b9943dd4d2ddfdf10a7ed5d40aafebd322ad02`  
		Last Modified: Tue, 09 Dec 2025 00:13:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bcaad5dbad529bb4b89320702ac9c7c208b99d5f46435edf49b8e7fa9b809f`  
		Last Modified: Tue, 09 Dec 2025 00:13:50 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:71969a907996b9e6cdc3adc664fb072ca6474a58222697ba1e23e5587b938595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4602907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb910d0b21f1466155426a195d1f5cdf0d1d61f2bd6893b21df0095052dab93`

```dockerfile
```

-	Layers:
	-	`sha256:a1cf8231346119c082e0166e97c071d38f4a50ab29279a07a16823edf57e66fd`  
		Last Modified: Tue, 09 Dec 2025 03:21:43 GMT  
		Size: 4.6 MB (4590614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cea5f55e5f523e79196c70fca6fc7ad49c2b3b39f1c26e8a42619594665b8c5`  
		Last Modified: Tue, 09 Dec 2025 03:21:44 GMT  
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
$ docker pull influxdb@sha256:62a9fa847313a43d3ac11c1eb7b32676dde555a58d8d9de39dcbec62abf4a00f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.2` - linux; amd64

```console
$ docker pull influxdb@sha256:16b82f03c99c52cff38383eff71b63668c44ead78fa100143848734559050b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113843321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6def1d57c5b7e5219288ace57fdcce389cd8185047e653577e9c4e47b0ec255`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:20 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 09 Dec 2025 00:13:25 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 09 Dec 2025 00:13:25 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:13:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
USER influxdb
# Tue, 09 Dec 2025 00:13:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:13:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6669fb2e9f61972e6fcd1e9ac7fcf0a5aa961dc413d84622b902f85d8fea42d`  
		Last Modified: Tue, 09 Dec 2025 00:13:46 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7f6d4419f522b29083240d811449358aaefa03da13fe664e5d65fe2b6d62d`  
		Last Modified: Tue, 09 Dec 2025 00:13:55 GMT  
		Size: 41.3 MB (41330326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4720bea0f108c0cbcfad2080a807b74d9e055e2f53c6bbe93396bd755779a18`  
		Last Modified: Tue, 09 Dec 2025 00:13:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0898c1139248ed67e9c0f0684c5ddec4671cccf1ed1955be761a31ce714e4ebc`  
		Last Modified: Tue, 09 Dec 2025 00:13:47 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8387f1aa93856fa89528cd5bcee576362facb896378b6e8e52fd77e0477a67`  
		Last Modified: Tue, 09 Dec 2025 00:13:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:38c5f487deb9d5e6c66779df8301046311043dc00cd19f362b76ec746191f0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae02be10047c064bfd3cb3534bd1a5a99d87e31a98d2be358bf44f1960e784b`

```dockerfile
```

-	Layers:
	-	`sha256:322331315e89f3fdb4be3d120672d9177002226317dec69ff0ba8fdf3b1dd2cb`  
		Last Modified: Tue, 09 Dec 2025 03:21:32 GMT  
		Size: 4.7 MB (4675813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79242889e7c5ae8259f0f42e44b806b34af7e58c5f2844d34a8cd0467f77228c`  
		Last Modified: Tue, 09 Dec 2025 03:21:32 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:11fc09c440d56e948dbcf54497c854a42f277b72b34271d7a2ec4106e7d4e2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110091058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8deb5c85c854ae71ce43181dcdc7a484fb5a5e6317ef1bc0c661f0e70747e3f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:19:01 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 09 Dec 2025 00:19:05 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 09 Dec 2025 00:19:05 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:19:05 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 09 Dec 2025 00:19:05 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 09 Dec 2025 00:19:05 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:19:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:19:05 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 09 Dec 2025 00:19:05 GMT
USER influxdb
# Tue, 09 Dec 2025 00:19:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:19:05 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca4be8a5364f21221ab6e74dae63da367a4a35bb9ff94d72b497b9e8540ae2d`  
		Last Modified: Tue, 09 Dec 2025 00:19:26 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bc9fb62888315b1768a3b73182cd5c73d9560c3c280dec4a51e53d7cbb1098`  
		Last Modified: Tue, 09 Dec 2025 00:19:28 GMT  
		Size: 38.1 MB (38130833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab842a1a7e1450b7f4a77bac29510a474505210916d065982fbf4657ee3e464`  
		Last Modified: Tue, 09 Dec 2025 00:19:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712935c4849e9c78a1fb08d694556a138993722f3313820558f0adf71dc0af8a`  
		Last Modified: Tue, 09 Dec 2025 00:19:26 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ee2b4054586b69ec7c98412fcbd9fed4c0a1457d05b8c0c8a41f4e9a030ed3`  
		Last Modified: Tue, 09 Dec 2025 00:19:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:9d649d33596da37270f666dacf41353f3c8d9f27dc889daaa078b8fd8bd5f69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4691822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2c59cce2c860496c1662fd0674d9d56f9201d5c8174a3be05980c06083b6a7`

```dockerfile
```

-	Layers:
	-	`sha256:6382d8157148d926eaa42e94c0d9a87e48fc9f775616fe4965c0e03e28247c96`  
		Last Modified: Tue, 09 Dec 2025 03:21:38 GMT  
		Size: 4.7 MB (4675271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55aab66676b4a948334d90e07f603218039e54458b4fc79798e2aa66a305d07f`  
		Last Modified: Tue, 09 Dec 2025 03:21:39 GMT  
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
$ docker pull influxdb@sha256:e8a574ce503156ed8fecac8feed3f952282b65d3e20e35b5bb47bb0e60bd63d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-data` - linux; amd64

```console
$ docker pull influxdb@sha256:00e3df17fba12a953e593daf7b890b8078b847bb0ac37adc6c767eada370eea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114827569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b645bc755492e0b2ccd0126e43b1fdc461ec0d6306bf059f3fac330875ae873f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 09 Dec 2025 00:13:25 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 09 Dec 2025 00:13:25 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:13:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 09 Dec 2025 00:13:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:13:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e916812f000712a61a547dcf5a393753b5639011592379d68acf836c464eda9`  
		Last Modified: Tue, 09 Dec 2025 00:13:52 GMT  
		Size: 42.3 MB (42315721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0d6d67762a417689a0d89eb5a12366e8c4b66dd155553721070e5101f910f3`  
		Last Modified: Tue, 09 Dec 2025 00:13:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd43f4fc0a04235fb7631c2f6200cc481f2dc02ac3da80dc23868ab9b49b0beb`  
		Last Modified: Tue, 09 Dec 2025 00:55:31 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8387f1aa93856fa89528cd5bcee576362facb896378b6e8e52fd77e0477a67`  
		Last Modified: Tue, 09 Dec 2025 00:13:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:649e6433ae5c491e8d08d296d7834e465d939a0503a5f06f3560a70c55147bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df00214c73b515df69f814418ecbe8a4a7485bb92424e1701758293818304c2`

```dockerfile
```

-	Layers:
	-	`sha256:59637e5306820301584616d5d3b49c5eadaab186dd2911493496d507836be2f0`  
		Last Modified: Tue, 09 Dec 2025 03:21:38 GMT  
		Size: 4.7 MB (4685451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf46c667a193fc9afac3f4e5e5ab08796e08ab95db622dd9ae160630e6f0be0a`  
		Last Modified: Tue, 09 Dec 2025 03:21:39 GMT  
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
$ docker pull influxdb@sha256:3a104bdc74287a29834b1e74a69683d5cfa8dea8dbaf1c79e8bf0018ed4e3067
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:7df4751660b4e0734a9b724805b7d69a9473b2490211cc6c56f820560a290832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91289660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569505e86cd5ad9eac7a12768fe281a1a9eab54ba3da86ad8a220c5ded5870d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:33 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 09 Dec 2025 00:13:33 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:13:33 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 09 Dec 2025 00:13:33 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 09 Dec 2025 00:13:33 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Dec 2025 00:13:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:13:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:13:33 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ced3eafc770dfb591ed0b943cc86a60503653b87707274904ae7f357e1313aa`  
		Last Modified: Tue, 09 Dec 2025 00:13:53 GMT  
		Size: 18.8 MB (18779024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94038bb0b45460f4df068a2656b9943dd4d2ddfdf10a7ed5d40aafebd322ad02`  
		Last Modified: Tue, 09 Dec 2025 00:13:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bcaad5dbad529bb4b89320702ac9c7c208b99d5f46435edf49b8e7fa9b809f`  
		Last Modified: Tue, 09 Dec 2025 00:13:50 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:71969a907996b9e6cdc3adc664fb072ca6474a58222697ba1e23e5587b938595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4602907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb910d0b21f1466155426a195d1f5cdf0d1d61f2bd6893b21df0095052dab93`

```dockerfile
```

-	Layers:
	-	`sha256:a1cf8231346119c082e0166e97c071d38f4a50ab29279a07a16823edf57e66fd`  
		Last Modified: Tue, 09 Dec 2025 03:21:43 GMT  
		Size: 4.6 MB (4590614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cea5f55e5f523e79196c70fca6fc7ad49c2b3b39f1c26e8a42619594665b8c5`  
		Last Modified: Tue, 09 Dec 2025 03:21:44 GMT  
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
$ docker pull influxdb@sha256:38829bd08b47bbfb23ee8ef98fef45ac59abb78d4d7e451870b7499840e0f365
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:3669bd66e4887f2bf178b5d8c73520eb95abc486476c8ee3a8aeaf3868ed1351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107224021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a462b10f2dcd27d7a4406f83cf3a6e98ba56475d7d3911e9a7313eab988b09bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 21:20:54 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 21:20:54 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:20:54 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Dec 2025 21:20:57 GMT
ENV GOSU_VER=1.19
# Thu, 11 Dec 2025 21:20:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Dec 2025 21:20:57 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:20:57 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:20:57 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:21:01 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:21:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:21:02 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:21:02 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:02 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:21:02 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:21:02 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:21:02 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:21:02 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:21:02 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6c5b7e5184d2694f7e00c18ccf964945fa504c6f4b0c5cc494f95442d5880d`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 9.8 MB (9796290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f105c03a426e1db3e339f90557253cd15a30f3c7e8b8fcafab517255e319c82e`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 6.2 MB (6156973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2466a9669beee52a807e7a8ad5848016cadec7327b552cc6fd681711f3f045`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1a94b5e5630da21f70d35b8e064291b9fa829afa5e577122eacb9d6497adca`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 811.5 KB (811477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e75849e6dcf40b3e9d7652d3134d01175642d3ade6cf14f87b06d5ac9c44e5`  
		Last Modified: Thu, 11 Dec 2025 21:21:54 GMT  
		Size: 50.4 MB (50447116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9e3b9c81fdc8f0fd69a83980787d18a49ef144acf052524f8692a89442e66`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 11.8 MB (11773793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49739d6301dcf53df0f9dd108470cd8c0f060f94df67b9fc80652a62b44cfebc`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ea8f055b7c0a941d89ad0a4975eb5d7a1a9cce7adf46941978325f74f4c38`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8291d544410a6d7b4d6f5d3849a015051f5627de3771759bccdaa8093061b725`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:6d5b211bf2d7c2d4a3b0e5f6baf728ecd6a51ba0a117ef3573e7f0046a29c86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32393d0d3de7f9305de7732e2191c5e2ab332767656e6f0ae5dc0aa0b0d3f75e`

```dockerfile
```

-	Layers:
	-	`sha256:6e72df097c24ad1ce1fe1e0b85621fc7357714ae8750ef5fdfb7496776db0d3a`  
		Last Modified: Fri, 12 Dec 2025 00:20:32 GMT  
		Size: 2.9 MB (2934227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530c203dd6101187fe0ffcb8d239eb488871aa417556ca7851616de9efcdc678`  
		Last Modified: Fri, 12 Dec 2025 00:20:35 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e44fc00219ab59bf3eeb01f3e25906c2e99e15bbccef85120ae793617c435918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103624828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e455c12a2559feec54f152b9b8635f288855284b60696d78bbd67b8864d53a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 21:20:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 21:20:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:20:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Dec 2025 21:20:47 GMT
ENV GOSU_VER=1.19
# Thu, 11 Dec 2025 21:20:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Dec 2025 21:20:47 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:20:47 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:20:47 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:20:51 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:20:51 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:20:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:20:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:20:53 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:20:53 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:20:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:20:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:20:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:20:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83dbb50e465add987a9b0d1e72615aea4ccec7bc9d2435b8840efc3dcf9cdfb`  
		Last Modified: Thu, 11 Dec 2025 21:21:44 GMT  
		Size: 9.6 MB (9626476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f7c93dccebef7a38bce64ad726968776236be5c93f6b1cb8ffab4bc81477fa`  
		Last Modified: Thu, 11 Dec 2025 21:21:43 GMT  
		Size: 5.8 MB (5790425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e4a7c9ef99e2ea95ad051eae00536222199b00ae7ee71f07db8b4ce070e4c7`  
		Last Modified: Thu, 11 Dec 2025 21:21:43 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1ce2fe5391f29005cd2888b88c013e28b0b9411600b90468bf03dcf44474aa`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 766.4 KB (766375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a863576f426fd1602fbc3b111ec55460504eafd10f5b131246700da6e4d40dd1`  
		Last Modified: Thu, 11 Dec 2025 21:21:46 GMT  
		Size: 48.2 MB (48229384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972cda6778a805a97bdabb7dc52cf316dcb1b53a2185a47c785ce65c544cba10`  
		Last Modified: Thu, 11 Dec 2025 21:21:43 GMT  
		Size: 11.1 MB (11099988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a77950c27edf7b42a43c0e1250aa98e3b13a62ba451c31661de6e0c73ddda1`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d0e64e366cb27aa722087d3390f64b99ba6175f188d64a1e43a82dc2557265`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd9442665675081ef3d0d7557fce092dec17dc64fdc08b6ad5fbdd3ffd10a27`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:7d180abed6483e8c69f3f5eda8c60c6758077fb68714a49d7df5bb0ea7691b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b255cad7c8b2f026cd6745eca49f754747f35565ac970f33982e01fd353a7c71`

```dockerfile
```

-	Layers:
	-	`sha256:9cc905cc79a18336d04c1386f6b444ed0b28be06a8de46597a9209cca8d12c48`  
		Last Modified: Fri, 12 Dec 2025 00:20:40 GMT  
		Size: 2.9 MB (2933707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724010682a39995361c350af48077ed7afc9bf92f4689c37eb49321d243f9898`  
		Last Modified: Fri, 12 Dec 2025 00:20:41 GMT  
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
$ docker pull influxdb@sha256:fc239ac8574c3d11f5ee03b9bce15b42a8562febb6862d8b76ed35465cd7f8ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:17d07f43a588bc9c68c575300d89d3fd7d2a3a806a7d0295d21e8c2bf0d0563f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223c19717338c6f70e54d12b95a09e7b85196eededfa5715fb519279690c7984`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:10:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 08 Dec 2025 23:10:48 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 08 Dec 2025 23:10:50 GMT
ENV GOSU_VER=1.16
# Mon, 08 Dec 2025 23:10:50 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:10:50 GMT
ENV INFLUXDB_VERSION=2.7.12
# Mon, 08 Dec 2025 23:10:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 08 Dec 2025 23:10:53 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 08 Dec 2025 23:10:54 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 08 Dec 2025 23:10:54 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 08 Dec 2025 23:10:54 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 08 Dec 2025 23:10:54 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 08 Dec 2025 23:10:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:10:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:10:54 GMT
CMD ["influxd"]
# Mon, 08 Dec 2025 23:10:54 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 08 Dec 2025 23:10:54 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 08 Dec 2025 23:10:54 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 08 Dec 2025 23:10:54 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 08 Dec 2025 23:10:54 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604851effd25328dbfe6e64335694c877236aba3650b90faeaa576df028ab2c`  
		Last Modified: Mon, 08 Dec 2025 23:11:22 GMT  
		Size: 9.8 MB (9796268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a364d1ca582d8d384f2639605845be6cd1933b7cfab23889e439b562ca635a0e`  
		Last Modified: Mon, 08 Dec 2025 23:11:19 GMT  
		Size: 6.2 MB (6156976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290754ae2d8f82fad5a9c75bcca7147fe844a1b3c30b2c2fb4cbbb70aec7fe2c`  
		Last Modified: Mon, 08 Dec 2025 23:11:18 GMT  
		Size: 3.2 KB (3222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be85d73b543b531c1ca66ca171591169061bdbd60466c4f8009c6506b2f2fc`  
		Last Modified: Mon, 08 Dec 2025 23:11:19 GMT  
		Size: 1.0 MB (1012039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f964140667d59d01540c8f77351e60f8c6b6f58ccb3d8a49c1c769aff5beb2b`  
		Last Modified: Mon, 08 Dec 2025 23:11:30 GMT  
		Size: 100.2 MB (100244549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9221d71d25e21b5b393f1287210930844f181053787ea11b1b0a50bb1b362dfc`  
		Last Modified: Mon, 08 Dec 2025 23:11:19 GMT  
		Size: 11.8 MB (11773791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9710e0fc7410459dc775d3654bc7daeaed98ba535a04ed12edb1aa7906daf811`  
		Last Modified: Mon, 08 Dec 2025 23:11:18 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ceb1bcf27d8f78c368c37fbf43476e1a17d8a04fed85a064432a3631fe519d`  
		Last Modified: Mon, 08 Dec 2025 23:11:18 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb26bb2f00dd254a3efe5d5e4f1c8e29421089ca970e693cf6eae354f56c566`  
		Last Modified: Mon, 08 Dec 2025 23:11:19 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:19e66dbdd74c58f3868f29872473e52a385c8406ffa34fd74e19932474119a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732f61d49321ec9b6d7f8a73df33f591bf6998258f9af39bd671a6b274d06159`

```dockerfile
```

-	Layers:
	-	`sha256:c24dde83600ab1332dc432b5fe2943195942e9191a6c0f8738faedf5e5a74f7e`  
		Last Modified: Tue, 09 Dec 2025 00:20:58 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae222d7860eb52590dc5d754c27b7f13aeccd0ae371307a4def21db3d94e3a4`  
		Last Modified: Tue, 09 Dec 2025 00:20:59 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:9d1b7cbd9bb6f63f639577b9186f1c849d4837935e3b80a426563c084ee41fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5e71c873d8ad9ba9fdd26ffc2ba237441a187f93559862179893c2a9e27d64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:14:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:14:07 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 08 Dec 2025 23:14:07 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 08 Dec 2025 23:14:09 GMT
ENV GOSU_VER=1.16
# Mon, 08 Dec 2025 23:14:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:14:09 GMT
ENV INFLUXDB_VERSION=2.7.12
# Mon, 08 Dec 2025 23:14:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 08 Dec 2025 23:14:12 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 08 Dec 2025 23:14:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 08 Dec 2025 23:14:13 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 08 Dec 2025 23:14:13 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 08 Dec 2025 23:14:13 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 08 Dec 2025 23:14:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:14:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:14:13 GMT
CMD ["influxd"]
# Mon, 08 Dec 2025 23:14:13 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 08 Dec 2025 23:14:13 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 08 Dec 2025 23:14:13 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 08 Dec 2025 23:14:13 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 08 Dec 2025 23:14:13 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f7db445d156280214a0f82564d7ae9ff5717f0a0f250b83a1ddfbcc3b3155`  
		Last Modified: Mon, 08 Dec 2025 23:14:37 GMT  
		Size: 9.6 MB (9626399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2157e667e520f915a6ec01a32317c08ebb439ac9e2e493be07985f14c0690be`  
		Last Modified: Mon, 08 Dec 2025 23:14:36 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59f0d19204d2f279f26b7142c450bf5c21422a13be04de84acd1fed9e0515c2`  
		Last Modified: Mon, 08 Dec 2025 23:14:36 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da81d7e5bcece4538628c845d61c6940b48c2933ac94faf54272e695100f24cb`  
		Last Modified: Mon, 08 Dec 2025 23:14:36 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9b942f724b0e83df8960c467a16d9820e8bd923626ae190277227a1a6b23d`  
		Last Modified: Mon, 08 Dec 2025 23:14:44 GMT  
		Size: 96.0 MB (96038991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383863f2b5c1cdbf0eeaca3f58d03b796758fa4d76d7a1b831330639c1f22d2f`  
		Last Modified: Mon, 08 Dec 2025 23:14:37 GMT  
		Size: 11.1 MB (11099995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a386d48b673581f7deba3b887eddd5d73cee8184870bfe1fe07d4b03307b099d`  
		Last Modified: Mon, 08 Dec 2025 23:14:36 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13321883fc6eb37adc4b7cb495600a9f61ddc6f4d404ce15fb3dc46b4369d37b`  
		Last Modified: Mon, 08 Dec 2025 23:14:36 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d13377e66a98389f6c605bf42948a7872569234c115899b22ca99d8025d9134`  
		Last Modified: Mon, 08 Dec 2025 23:14:37 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:6b5d73b277bf0a78f67fff2a7415f445dfc7f31ef19d7e40f078b58813e8f679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2e95b7af44c8c4e2fb813a19541654c9a5841774933e52c0a9922438bebc70`

```dockerfile
```

-	Layers:
	-	`sha256:c0104d30442ac431629e4871ae29fe65682c48bd93a60d4c6dbe80452b09aa49`  
		Last Modified: Tue, 09 Dec 2025 03:22:11 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457b9ba9c1dea154a1f4386421628ca42a8e6c503de5f96c1dc886c445345711`  
		Last Modified: Tue, 09 Dec 2025 03:22:11 GMT  
		Size: 33.7 KB (33678 bytes)  
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
$ docker pull influxdb@sha256:fc239ac8574c3d11f5ee03b9bce15b42a8562febb6862d8b76ed35465cd7f8ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:17d07f43a588bc9c68c575300d89d3fd7d2a3a806a7d0295d21e8c2bf0d0563f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223c19717338c6f70e54d12b95a09e7b85196eededfa5715fb519279690c7984`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:10:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 08 Dec 2025 23:10:48 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 08 Dec 2025 23:10:50 GMT
ENV GOSU_VER=1.16
# Mon, 08 Dec 2025 23:10:50 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:10:50 GMT
ENV INFLUXDB_VERSION=2.7.12
# Mon, 08 Dec 2025 23:10:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 08 Dec 2025 23:10:53 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 08 Dec 2025 23:10:54 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 08 Dec 2025 23:10:54 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 08 Dec 2025 23:10:54 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 08 Dec 2025 23:10:54 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 08 Dec 2025 23:10:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:10:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:10:54 GMT
CMD ["influxd"]
# Mon, 08 Dec 2025 23:10:54 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 08 Dec 2025 23:10:54 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 08 Dec 2025 23:10:54 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 08 Dec 2025 23:10:54 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 08 Dec 2025 23:10:54 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604851effd25328dbfe6e64335694c877236aba3650b90faeaa576df028ab2c`  
		Last Modified: Mon, 08 Dec 2025 23:11:22 GMT  
		Size: 9.8 MB (9796268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a364d1ca582d8d384f2639605845be6cd1933b7cfab23889e439b562ca635a0e`  
		Last Modified: Mon, 08 Dec 2025 23:11:19 GMT  
		Size: 6.2 MB (6156976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290754ae2d8f82fad5a9c75bcca7147fe844a1b3c30b2c2fb4cbbb70aec7fe2c`  
		Last Modified: Mon, 08 Dec 2025 23:11:18 GMT  
		Size: 3.2 KB (3222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be85d73b543b531c1ca66ca171591169061bdbd60466c4f8009c6506b2f2fc`  
		Last Modified: Mon, 08 Dec 2025 23:11:19 GMT  
		Size: 1.0 MB (1012039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f964140667d59d01540c8f77351e60f8c6b6f58ccb3d8a49c1c769aff5beb2b`  
		Last Modified: Mon, 08 Dec 2025 23:11:30 GMT  
		Size: 100.2 MB (100244549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9221d71d25e21b5b393f1287210930844f181053787ea11b1b0a50bb1b362dfc`  
		Last Modified: Mon, 08 Dec 2025 23:11:19 GMT  
		Size: 11.8 MB (11773791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9710e0fc7410459dc775d3654bc7daeaed98ba535a04ed12edb1aa7906daf811`  
		Last Modified: Mon, 08 Dec 2025 23:11:18 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ceb1bcf27d8f78c368c37fbf43476e1a17d8a04fed85a064432a3631fe519d`  
		Last Modified: Mon, 08 Dec 2025 23:11:18 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb26bb2f00dd254a3efe5d5e4f1c8e29421089ca970e693cf6eae354f56c566`  
		Last Modified: Mon, 08 Dec 2025 23:11:19 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:19e66dbdd74c58f3868f29872473e52a385c8406ffa34fd74e19932474119a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732f61d49321ec9b6d7f8a73df33f591bf6998258f9af39bd671a6b274d06159`

```dockerfile
```

-	Layers:
	-	`sha256:c24dde83600ab1332dc432b5fe2943195942e9191a6c0f8738faedf5e5a74f7e`  
		Last Modified: Tue, 09 Dec 2025 00:20:58 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae222d7860eb52590dc5d754c27b7f13aeccd0ae371307a4def21db3d94e3a4`  
		Last Modified: Tue, 09 Dec 2025 00:20:59 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:9d1b7cbd9bb6f63f639577b9186f1c849d4837935e3b80a426563c084ee41fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5e71c873d8ad9ba9fdd26ffc2ba237441a187f93559862179893c2a9e27d64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:14:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:14:07 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 08 Dec 2025 23:14:07 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 08 Dec 2025 23:14:09 GMT
ENV GOSU_VER=1.16
# Mon, 08 Dec 2025 23:14:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:14:09 GMT
ENV INFLUXDB_VERSION=2.7.12
# Mon, 08 Dec 2025 23:14:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 08 Dec 2025 23:14:12 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 08 Dec 2025 23:14:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 08 Dec 2025 23:14:13 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 08 Dec 2025 23:14:13 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 08 Dec 2025 23:14:13 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 08 Dec 2025 23:14:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:14:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:14:13 GMT
CMD ["influxd"]
# Mon, 08 Dec 2025 23:14:13 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 08 Dec 2025 23:14:13 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 08 Dec 2025 23:14:13 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 08 Dec 2025 23:14:13 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 08 Dec 2025 23:14:13 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f7db445d156280214a0f82564d7ae9ff5717f0a0f250b83a1ddfbcc3b3155`  
		Last Modified: Mon, 08 Dec 2025 23:14:37 GMT  
		Size: 9.6 MB (9626399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2157e667e520f915a6ec01a32317c08ebb439ac9e2e493be07985f14c0690be`  
		Last Modified: Mon, 08 Dec 2025 23:14:36 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59f0d19204d2f279f26b7142c450bf5c21422a13be04de84acd1fed9e0515c2`  
		Last Modified: Mon, 08 Dec 2025 23:14:36 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da81d7e5bcece4538628c845d61c6940b48c2933ac94faf54272e695100f24cb`  
		Last Modified: Mon, 08 Dec 2025 23:14:36 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9b942f724b0e83df8960c467a16d9820e8bd923626ae190277227a1a6b23d`  
		Last Modified: Mon, 08 Dec 2025 23:14:44 GMT  
		Size: 96.0 MB (96038991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383863f2b5c1cdbf0eeaca3f58d03b796758fa4d76d7a1b831330639c1f22d2f`  
		Last Modified: Mon, 08 Dec 2025 23:14:37 GMT  
		Size: 11.1 MB (11099995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a386d48b673581f7deba3b887eddd5d73cee8184870bfe1fe07d4b03307b099d`  
		Last Modified: Mon, 08 Dec 2025 23:14:36 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13321883fc6eb37adc4b7cb495600a9f61ddc6f4d404ce15fb3dc46b4369d37b`  
		Last Modified: Mon, 08 Dec 2025 23:14:36 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d13377e66a98389f6c605bf42948a7872569234c115899b22ca99d8025d9134`  
		Last Modified: Mon, 08 Dec 2025 23:14:37 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:6b5d73b277bf0a78f67fff2a7415f445dfc7f31ef19d7e40f078b58813e8f679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2e95b7af44c8c4e2fb813a19541654c9a5841774933e52c0a9922438bebc70`

```dockerfile
```

-	Layers:
	-	`sha256:c0104d30442ac431629e4871ae29fe65682c48bd93a60d4c6dbe80452b09aa49`  
		Last Modified: Tue, 09 Dec 2025 03:22:11 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457b9ba9c1dea154a1f4386421628ca42a8e6c503de5f96c1dc886c445345711`  
		Last Modified: Tue, 09 Dec 2025 03:22:11 GMT  
		Size: 33.7 KB (33678 bytes)  
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
$ docker pull influxdb@sha256:38829bd08b47bbfb23ee8ef98fef45ac59abb78d4d7e451870b7499840e0f365
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8` - linux; amd64

```console
$ docker pull influxdb@sha256:3669bd66e4887f2bf178b5d8c73520eb95abc486476c8ee3a8aeaf3868ed1351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107224021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a462b10f2dcd27d7a4406f83cf3a6e98ba56475d7d3911e9a7313eab988b09bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 21:20:54 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 21:20:54 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:20:54 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Dec 2025 21:20:57 GMT
ENV GOSU_VER=1.19
# Thu, 11 Dec 2025 21:20:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Dec 2025 21:20:57 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:20:57 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:20:57 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:21:01 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:21:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:21:02 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:21:02 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:02 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:21:02 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:21:02 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:21:02 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:21:02 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:21:02 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6c5b7e5184d2694f7e00c18ccf964945fa504c6f4b0c5cc494f95442d5880d`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 9.8 MB (9796290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f105c03a426e1db3e339f90557253cd15a30f3c7e8b8fcafab517255e319c82e`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 6.2 MB (6156973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2466a9669beee52a807e7a8ad5848016cadec7327b552cc6fd681711f3f045`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1a94b5e5630da21f70d35b8e064291b9fa829afa5e577122eacb9d6497adca`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 811.5 KB (811477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e75849e6dcf40b3e9d7652d3134d01175642d3ade6cf14f87b06d5ac9c44e5`  
		Last Modified: Thu, 11 Dec 2025 21:21:54 GMT  
		Size: 50.4 MB (50447116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9e3b9c81fdc8f0fd69a83980787d18a49ef144acf052524f8692a89442e66`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 11.8 MB (11773793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49739d6301dcf53df0f9dd108470cd8c0f060f94df67b9fc80652a62b44cfebc`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ea8f055b7c0a941d89ad0a4975eb5d7a1a9cce7adf46941978325f74f4c38`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8291d544410a6d7b4d6f5d3849a015051f5627de3771759bccdaa8093061b725`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:6d5b211bf2d7c2d4a3b0e5f6baf728ecd6a51ba0a117ef3573e7f0046a29c86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32393d0d3de7f9305de7732e2191c5e2ab332767656e6f0ae5dc0aa0b0d3f75e`

```dockerfile
```

-	Layers:
	-	`sha256:6e72df097c24ad1ce1fe1e0b85621fc7357714ae8750ef5fdfb7496776db0d3a`  
		Last Modified: Fri, 12 Dec 2025 00:20:32 GMT  
		Size: 2.9 MB (2934227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530c203dd6101187fe0ffcb8d239eb488871aa417556ca7851616de9efcdc678`  
		Last Modified: Fri, 12 Dec 2025 00:20:35 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e44fc00219ab59bf3eeb01f3e25906c2e99e15bbccef85120ae793617c435918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103624828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e455c12a2559feec54f152b9b8635f288855284b60696d78bbd67b8864d53a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 21:20:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 21:20:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:20:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Dec 2025 21:20:47 GMT
ENV GOSU_VER=1.19
# Thu, 11 Dec 2025 21:20:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Dec 2025 21:20:47 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:20:47 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:20:47 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:20:51 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:20:51 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:20:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:20:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:20:53 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:20:53 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:20:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:20:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:20:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:20:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83dbb50e465add987a9b0d1e72615aea4ccec7bc9d2435b8840efc3dcf9cdfb`  
		Last Modified: Thu, 11 Dec 2025 21:21:44 GMT  
		Size: 9.6 MB (9626476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f7c93dccebef7a38bce64ad726968776236be5c93f6b1cb8ffab4bc81477fa`  
		Last Modified: Thu, 11 Dec 2025 21:21:43 GMT  
		Size: 5.8 MB (5790425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e4a7c9ef99e2ea95ad051eae00536222199b00ae7ee71f07db8b4ce070e4c7`  
		Last Modified: Thu, 11 Dec 2025 21:21:43 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1ce2fe5391f29005cd2888b88c013e28b0b9411600b90468bf03dcf44474aa`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 766.4 KB (766375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a863576f426fd1602fbc3b111ec55460504eafd10f5b131246700da6e4d40dd1`  
		Last Modified: Thu, 11 Dec 2025 21:21:46 GMT  
		Size: 48.2 MB (48229384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972cda6778a805a97bdabb7dc52cf316dcb1b53a2185a47c785ce65c544cba10`  
		Last Modified: Thu, 11 Dec 2025 21:21:43 GMT  
		Size: 11.1 MB (11099988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a77950c27edf7b42a43c0e1250aa98e3b13a62ba451c31661de6e0c73ddda1`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d0e64e366cb27aa722087d3390f64b99ba6175f188d64a1e43a82dc2557265`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd9442665675081ef3d0d7557fce092dec17dc64fdc08b6ad5fbdd3ffd10a27`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:7d180abed6483e8c69f3f5eda8c60c6758077fb68714a49d7df5bb0ea7691b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b255cad7c8b2f026cd6745eca49f754747f35565ac970f33982e01fd353a7c71`

```dockerfile
```

-	Layers:
	-	`sha256:9cc905cc79a18336d04c1386f6b444ed0b28be06a8de46597a9209cca8d12c48`  
		Last Modified: Fri, 12 Dec 2025 00:20:40 GMT  
		Size: 2.9 MB (2933707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724010682a39995361c350af48077ed7afc9bf92f4689c37eb49321d243f9898`  
		Last Modified: Fri, 12 Dec 2025 00:20:41 GMT  
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
$ docker pull influxdb@sha256:38829bd08b47bbfb23ee8ef98fef45ac59abb78d4d7e451870b7499840e0f365
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0` - linux; amd64

```console
$ docker pull influxdb@sha256:3669bd66e4887f2bf178b5d8c73520eb95abc486476c8ee3a8aeaf3868ed1351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107224021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a462b10f2dcd27d7a4406f83cf3a6e98ba56475d7d3911e9a7313eab988b09bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 21:20:54 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 21:20:54 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:20:54 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Dec 2025 21:20:57 GMT
ENV GOSU_VER=1.19
# Thu, 11 Dec 2025 21:20:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Dec 2025 21:20:57 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:20:57 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:20:57 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:21:01 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:21:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:21:02 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:21:02 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:02 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:21:02 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:21:02 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:21:02 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:21:02 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:21:02 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6c5b7e5184d2694f7e00c18ccf964945fa504c6f4b0c5cc494f95442d5880d`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 9.8 MB (9796290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f105c03a426e1db3e339f90557253cd15a30f3c7e8b8fcafab517255e319c82e`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 6.2 MB (6156973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2466a9669beee52a807e7a8ad5848016cadec7327b552cc6fd681711f3f045`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1a94b5e5630da21f70d35b8e064291b9fa829afa5e577122eacb9d6497adca`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 811.5 KB (811477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e75849e6dcf40b3e9d7652d3134d01175642d3ade6cf14f87b06d5ac9c44e5`  
		Last Modified: Thu, 11 Dec 2025 21:21:54 GMT  
		Size: 50.4 MB (50447116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9e3b9c81fdc8f0fd69a83980787d18a49ef144acf052524f8692a89442e66`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 11.8 MB (11773793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49739d6301dcf53df0f9dd108470cd8c0f060f94df67b9fc80652a62b44cfebc`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ea8f055b7c0a941d89ad0a4975eb5d7a1a9cce7adf46941978325f74f4c38`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8291d544410a6d7b4d6f5d3849a015051f5627de3771759bccdaa8093061b725`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:6d5b211bf2d7c2d4a3b0e5f6baf728ecd6a51ba0a117ef3573e7f0046a29c86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32393d0d3de7f9305de7732e2191c5e2ab332767656e6f0ae5dc0aa0b0d3f75e`

```dockerfile
```

-	Layers:
	-	`sha256:6e72df097c24ad1ce1fe1e0b85621fc7357714ae8750ef5fdfb7496776db0d3a`  
		Last Modified: Fri, 12 Dec 2025 00:20:32 GMT  
		Size: 2.9 MB (2934227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530c203dd6101187fe0ffcb8d239eb488871aa417556ca7851616de9efcdc678`  
		Last Modified: Fri, 12 Dec 2025 00:20:35 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e44fc00219ab59bf3eeb01f3e25906c2e99e15bbccef85120ae793617c435918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103624828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e455c12a2559feec54f152b9b8635f288855284b60696d78bbd67b8864d53a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 21:20:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 21:20:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:20:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Dec 2025 21:20:47 GMT
ENV GOSU_VER=1.19
# Thu, 11 Dec 2025 21:20:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Dec 2025 21:20:47 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:20:47 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:20:47 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:20:51 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:20:51 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:20:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:20:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:20:53 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:20:53 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:20:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:20:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:20:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:20:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83dbb50e465add987a9b0d1e72615aea4ccec7bc9d2435b8840efc3dcf9cdfb`  
		Last Modified: Thu, 11 Dec 2025 21:21:44 GMT  
		Size: 9.6 MB (9626476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f7c93dccebef7a38bce64ad726968776236be5c93f6b1cb8ffab4bc81477fa`  
		Last Modified: Thu, 11 Dec 2025 21:21:43 GMT  
		Size: 5.8 MB (5790425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e4a7c9ef99e2ea95ad051eae00536222199b00ae7ee71f07db8b4ce070e4c7`  
		Last Modified: Thu, 11 Dec 2025 21:21:43 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1ce2fe5391f29005cd2888b88c013e28b0b9411600b90468bf03dcf44474aa`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 766.4 KB (766375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a863576f426fd1602fbc3b111ec55460504eafd10f5b131246700da6e4d40dd1`  
		Last Modified: Thu, 11 Dec 2025 21:21:46 GMT  
		Size: 48.2 MB (48229384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972cda6778a805a97bdabb7dc52cf316dcb1b53a2185a47c785ce65c544cba10`  
		Last Modified: Thu, 11 Dec 2025 21:21:43 GMT  
		Size: 11.1 MB (11099988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a77950c27edf7b42a43c0e1250aa98e3b13a62ba451c31661de6e0c73ddda1`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d0e64e366cb27aa722087d3390f64b99ba6175f188d64a1e43a82dc2557265`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd9442665675081ef3d0d7557fce092dec17dc64fdc08b6ad5fbdd3ffd10a27`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:7d180abed6483e8c69f3f5eda8c60c6758077fb68714a49d7df5bb0ea7691b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b255cad7c8b2f026cd6745eca49f754747f35565ac970f33982e01fd353a7c71`

```dockerfile
```

-	Layers:
	-	`sha256:9cc905cc79a18336d04c1386f6b444ed0b28be06a8de46597a9209cca8d12c48`  
		Last Modified: Fri, 12 Dec 2025 00:20:40 GMT  
		Size: 2.9 MB (2933707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724010682a39995361c350af48077ed7afc9bf92f4689c37eb49321d243f9898`  
		Last Modified: Fri, 12 Dec 2025 00:20:41 GMT  
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
$ docker pull influxdb@sha256:fb25468a7f530001a6d8e33cd762757d2a01a94bcffa548bb6720f6814c723cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:1460eaedd23b77f3e33d0d2f2416040001b9b5b8941b3faf27854809b26b2fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117798544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842428e388e55f6f2d9fe031677c407cfd2351002fee723bbca95f404d4d03f9`
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
# Thu, 11 Dec 2025 21:21:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 11 Dec 2025 21:21:37 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB_VERSION=3.7.0
# Thu, 11 Dec 2025 21:21:41 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
USER influxdb3
# Thu, 11 Dec 2025 21:21:41 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 11 Dec 2025 21:21:41 GMT
ENV LOG_FILTER=info
# Thu, 11 Dec 2025 21:21:41 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 11 Dec 2025 21:21:41 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:41 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74568c6b68d3c934c624838bcd2ed98a6e09a1b5b40c414d8d4e135560019db6`  
		Last Modified: Thu, 11 Dec 2025 21:22:09 GMT  
		Size: 6.7 MB (6666160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cda3c42a285ee841f8fe9ae40ddcb0f9d2f61364adb9cdde2ea0e8337d862fb`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63d36e84d1d75f8c55fc4e08ef4cf3d16e4709bad072ab79c20a56973667323`  
		Last Modified: Thu, 11 Dec 2025 21:22:16 GMT  
		Size: 81.4 MB (81403366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26718f5dab0402791ee2a89ac3ce99304e7e8419472882f596d6f195f0ebfd72`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 522.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5df172dc82ce1441dc402a47f3988199f7ac221cb97b9f75e284f948f19179`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5697499ad09f1d7ee9250a650de9b6625ddb259f801147e8162c71e595e8bd79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f67dc65a09282e0a0c60879470c6b04b3c8979ef5648094b84c06cb8e32284`

```dockerfile
```

-	Layers:
	-	`sha256:e3aaa038e533f5961a37565929ad4f0e2b5543c7210a2df786d0cffbf9bd5f5c`  
		Last Modified: Fri, 12 Dec 2025 00:20:59 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d10856ef1689fd366bfe41b9372b4b691a4821620ff492179a59102e6e5226ab`  
		Last Modified: Fri, 12 Dec 2025 00:21:00 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0fbb2417a8c7031186b5620e84fdb0ec0578aa0a996c919536dc25f717e1847e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108280727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2d7163cb03a89afa3b3004c6b7ecfedf5aea042793dd101225b2c1bcba90f5`
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
# Thu, 11 Dec 2025 21:21:25 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 11 Dec 2025 21:21:25 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB_VERSION=3.7.0
# Thu, 11 Dec 2025 21:21:29 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
USER influxdb3
# Thu, 11 Dec 2025 21:21:29 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 11 Dec 2025 21:21:29 GMT
ENV LOG_FILTER=info
# Thu, 11 Dec 2025 21:21:29 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 11 Dec 2025 21:21:29 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:29 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9f45ca4f6eaf2a4a96a97ee68a40c27d591b52bb7021bfff72e6ea8a1f1d34`  
		Last Modified: Thu, 11 Dec 2025 21:22:06 GMT  
		Size: 6.7 MB (6676640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4078d8127dc24b235d348ec18c160bb885a289ef1de179adfec3c0dc13582dc`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82915314d7a4b06fe2466157daa345fd2d30698f4b44b00fa218d4a967d2079`  
		Last Modified: Thu, 11 Dec 2025 21:22:15 GMT  
		Size: 72.7 MB (72737806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210c6be1560e90fbdbb25f7ffe6ad8f13527aa81d6fbc0564c3188571e60f408`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c024c1fb06638838f9b95d87d31fa616b6e9d78e6bec01941337bbefcc418c`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:197c5a19c63aa5698340d1b90e34d81b07f688dc267776c18bde33e0a2f53475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8298d3fd556dbb99fa70a3d4f000aa2b4164a9ece5f6db47203043425f4f42b5`

```dockerfile
```

-	Layers:
	-	`sha256:77eb53b16e16257066afc59798ed7f22a6d7236ecbf257a13988daf278de74e7`  
		Last Modified: Fri, 12 Dec 2025 00:21:04 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd917ae9c4105d437d77fcf6ba410bd93480390d85dcbf7c21c64c5211afa3e9`  
		Last Modified: Fri, 12 Dec 2025 00:21:05 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:d505d356938a25e2e15a8b2dadf2218b738da021d2ed7392004a817a1de52b20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:e29b41f14d7ad157cbcf017650e4f6dac627554c2d924f9e7ae57884971e1fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125281476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b2acb59bf6a3c5f51048608de0ddb03ce8b1ea1b6a3c7be429cc2228e7a8cd`
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
# Fri, 21 Nov 2025 01:09:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:09:02 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:09:36 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:09:36 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:09:36 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:09:36 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec602172e261977575f11d467ce7288f5db05528add2c6687ed88115e4566d`  
		Last Modified: Fri, 21 Nov 2025 01:09:30 GMT  
		Size: 6.7 MB (6666106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a22f257fc04204500973a158da995dc0be631c882769bc2133d99ec614904`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e633feb1122d323a9eb9cb94f723b7ad8d87cd51101808c25cd5bbb60281774`  
		Last Modified: Fri, 21 Nov 2025 01:10:10 GMT  
		Size: 88.9 MB (88886351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094d85b5cca2f3812331aaae16d49f65afb45edd2d0b9df16c424053b115082f`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77620888035321ce666dd8db02345ec637bd5a5049483f28c2de8982a5004f6`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:525301679e2494bb0c0463ecbc3f21ca1537fe80ba004d612683ea46f86f772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9303d33e2ca892f135c5953d369eb916df97424dd830393dc0467f589286511`

```dockerfile
```

-	Layers:
	-	`sha256:0e3e1236d677c014e3b16c3fd1ebf921a7360ffcdfe9cf29eec7c130ce059033`  
		Last Modified: Fri, 21 Nov 2025 03:20:40 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3683ae9634c5647b18930425cbfea200fc9c2f7cbfbbcb6f782bf146448dd451`  
		Last Modified: Fri, 21 Nov 2025 03:20:41 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ef0f1b8579a522489edca19bc7f616955496bdd5ee86066034eacbd6b21af53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115463993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0693736329ed32d1736000731a7dc106ae021eddabca28959c72e2ded72fc6bd`
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
# Fri, 21 Nov 2025 01:10:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:10:36 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:11:13 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:11:13 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:11:13 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:11:13 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b215b3151b300b2deec4daf8615f7ecb4bc96eb27db8209830dd66e00903c`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 6.7 MB (6676577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e25c4f8d48f3e4d9c23f68e350c0afbd64652ae03ebf6b59a98a95ddf691d25`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468b79c8366daaff07e38012ca6581d1aee98e31cecfe08b475184ceb20d4d34`  
		Last Modified: Fri, 21 Nov 2025 01:11:54 GMT  
		Size: 79.9 MB (79921134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b10e43e65b0618999012821ca464275048f96d3c3b0c6ef07b99bdd200161c`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cfb6bcaf92a99d2c342aa44899f9a76113610e142d349c264dd6def810c715`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd577be3b08e4279db3fffc19d22238ef18b07f075369b5ff90308c7338fc21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9e6074b38338411e63bc4d131cc4ec4f561ef77707bf0044ece1c652855c35`

```dockerfile
```

-	Layers:
	-	`sha256:0bac5d7414f7aa16b6033522b5e7e3ad2f6cc6663403d6eb92656f00d4046d09`  
		Last Modified: Fri, 21 Nov 2025 03:20:45 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fd085a2d753c505f26f533794ef16eded8d10389faa4beca71a35c4f978fae`  
		Last Modified: Fri, 21 Nov 2025 03:20:46 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.7-core`

```console
$ docker pull influxdb@sha256:fb25468a7f530001a6d8e33cd762757d2a01a94bcffa548bb6720f6814c723cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.7-core` - linux; amd64

```console
$ docker pull influxdb@sha256:1460eaedd23b77f3e33d0d2f2416040001b9b5b8941b3faf27854809b26b2fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117798544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842428e388e55f6f2d9fe031677c407cfd2351002fee723bbca95f404d4d03f9`
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
# Thu, 11 Dec 2025 21:21:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 11 Dec 2025 21:21:37 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB_VERSION=3.7.0
# Thu, 11 Dec 2025 21:21:41 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
USER influxdb3
# Thu, 11 Dec 2025 21:21:41 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 11 Dec 2025 21:21:41 GMT
ENV LOG_FILTER=info
# Thu, 11 Dec 2025 21:21:41 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 11 Dec 2025 21:21:41 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:41 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74568c6b68d3c934c624838bcd2ed98a6e09a1b5b40c414d8d4e135560019db6`  
		Last Modified: Thu, 11 Dec 2025 21:22:09 GMT  
		Size: 6.7 MB (6666160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cda3c42a285ee841f8fe9ae40ddcb0f9d2f61364adb9cdde2ea0e8337d862fb`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63d36e84d1d75f8c55fc4e08ef4cf3d16e4709bad072ab79c20a56973667323`  
		Last Modified: Thu, 11 Dec 2025 21:22:16 GMT  
		Size: 81.4 MB (81403366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26718f5dab0402791ee2a89ac3ce99304e7e8419472882f596d6f195f0ebfd72`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 522.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5df172dc82ce1441dc402a47f3988199f7ac221cb97b9f75e284f948f19179`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5697499ad09f1d7ee9250a650de9b6625ddb259f801147e8162c71e595e8bd79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f67dc65a09282e0a0c60879470c6b04b3c8979ef5648094b84c06cb8e32284`

```dockerfile
```

-	Layers:
	-	`sha256:e3aaa038e533f5961a37565929ad4f0e2b5543c7210a2df786d0cffbf9bd5f5c`  
		Last Modified: Fri, 12 Dec 2025 00:20:59 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d10856ef1689fd366bfe41b9372b4b691a4821620ff492179a59102e6e5226ab`  
		Last Modified: Fri, 12 Dec 2025 00:21:00 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.7-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0fbb2417a8c7031186b5620e84fdb0ec0578aa0a996c919536dc25f717e1847e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108280727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2d7163cb03a89afa3b3004c6b7ecfedf5aea042793dd101225b2c1bcba90f5`
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
# Thu, 11 Dec 2025 21:21:25 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 11 Dec 2025 21:21:25 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB_VERSION=3.7.0
# Thu, 11 Dec 2025 21:21:29 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
USER influxdb3
# Thu, 11 Dec 2025 21:21:29 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 11 Dec 2025 21:21:29 GMT
ENV LOG_FILTER=info
# Thu, 11 Dec 2025 21:21:29 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 11 Dec 2025 21:21:29 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:29 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9f45ca4f6eaf2a4a96a97ee68a40c27d591b52bb7021bfff72e6ea8a1f1d34`  
		Last Modified: Thu, 11 Dec 2025 21:22:06 GMT  
		Size: 6.7 MB (6676640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4078d8127dc24b235d348ec18c160bb885a289ef1de179adfec3c0dc13582dc`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82915314d7a4b06fe2466157daa345fd2d30698f4b44b00fa218d4a967d2079`  
		Last Modified: Thu, 11 Dec 2025 21:22:15 GMT  
		Size: 72.7 MB (72737806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210c6be1560e90fbdbb25f7ffe6ad8f13527aa81d6fbc0564c3188571e60f408`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c024c1fb06638838f9b95d87d31fa616b6e9d78e6bec01941337bbefcc418c`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:197c5a19c63aa5698340d1b90e34d81b07f688dc267776c18bde33e0a2f53475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8298d3fd556dbb99fa70a3d4f000aa2b4164a9ece5f6db47203043425f4f42b5`

```dockerfile
```

-	Layers:
	-	`sha256:77eb53b16e16257066afc59798ed7f22a6d7236ecbf257a13988daf278de74e7`  
		Last Modified: Fri, 12 Dec 2025 00:21:04 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd917ae9c4105d437d77fcf6ba410bd93480390d85dcbf7c21c64c5211afa3e9`  
		Last Modified: Fri, 12 Dec 2025 00:21:05 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.7-enterprise`

```console
$ docker pull influxdb@sha256:d505d356938a25e2e15a8b2dadf2218b738da021d2ed7392004a817a1de52b20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.7-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:e29b41f14d7ad157cbcf017650e4f6dac627554c2d924f9e7ae57884971e1fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125281476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b2acb59bf6a3c5f51048608de0ddb03ce8b1ea1b6a3c7be429cc2228e7a8cd`
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
# Fri, 21 Nov 2025 01:09:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:09:02 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:09:36 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:09:36 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:09:36 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:09:36 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec602172e261977575f11d467ce7288f5db05528add2c6687ed88115e4566d`  
		Last Modified: Fri, 21 Nov 2025 01:09:30 GMT  
		Size: 6.7 MB (6666106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a22f257fc04204500973a158da995dc0be631c882769bc2133d99ec614904`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e633feb1122d323a9eb9cb94f723b7ad8d87cd51101808c25cd5bbb60281774`  
		Last Modified: Fri, 21 Nov 2025 01:10:10 GMT  
		Size: 88.9 MB (88886351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094d85b5cca2f3812331aaae16d49f65afb45edd2d0b9df16c424053b115082f`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77620888035321ce666dd8db02345ec637bd5a5049483f28c2de8982a5004f6`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:525301679e2494bb0c0463ecbc3f21ca1537fe80ba004d612683ea46f86f772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9303d33e2ca892f135c5953d369eb916df97424dd830393dc0467f589286511`

```dockerfile
```

-	Layers:
	-	`sha256:0e3e1236d677c014e3b16c3fd1ebf921a7360ffcdfe9cf29eec7c130ce059033`  
		Last Modified: Fri, 21 Nov 2025 03:20:40 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3683ae9634c5647b18930425cbfea200fc9c2f7cbfbbcb6f782bf146448dd451`  
		Last Modified: Fri, 21 Nov 2025 03:20:41 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.7-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ef0f1b8579a522489edca19bc7f616955496bdd5ee86066034eacbd6b21af53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115463993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0693736329ed32d1736000731a7dc106ae021eddabca28959c72e2ded72fc6bd`
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
# Fri, 21 Nov 2025 01:10:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:10:36 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:11:13 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:11:13 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:11:13 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:11:13 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b215b3151b300b2deec4daf8615f7ecb4bc96eb27db8209830dd66e00903c`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 6.7 MB (6676577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e25c4f8d48f3e4d9c23f68e350c0afbd64652ae03ebf6b59a98a95ddf691d25`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468b79c8366daaff07e38012ca6581d1aee98e31cecfe08b475184ceb20d4d34`  
		Last Modified: Fri, 21 Nov 2025 01:11:54 GMT  
		Size: 79.9 MB (79921134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b10e43e65b0618999012821ca464275048f96d3c3b0c6ef07b99bdd200161c`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cfb6bcaf92a99d2c342aa44899f9a76113610e142d349c264dd6def810c715`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd577be3b08e4279db3fffc19d22238ef18b07f075369b5ff90308c7338fc21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9e6074b38338411e63bc4d131cc4ec4f561ef77707bf0044ece1c652855c35`

```dockerfile
```

-	Layers:
	-	`sha256:0bac5d7414f7aa16b6033522b5e7e3ad2f6cc6663403d6eb92656f00d4046d09`  
		Last Modified: Fri, 21 Nov 2025 03:20:45 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fd085a2d753c505f26f533794ef16eded8d10389faa4beca71a35c4f978fae`  
		Last Modified: Fri, 21 Nov 2025 03:20:46 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.7.0-core`

```console
$ docker pull influxdb@sha256:fb25468a7f530001a6d8e33cd762757d2a01a94bcffa548bb6720f6814c723cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.7.0-core` - linux; amd64

```console
$ docker pull influxdb@sha256:1460eaedd23b77f3e33d0d2f2416040001b9b5b8941b3faf27854809b26b2fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117798544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842428e388e55f6f2d9fe031677c407cfd2351002fee723bbca95f404d4d03f9`
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
# Thu, 11 Dec 2025 21:21:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 11 Dec 2025 21:21:37 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB_VERSION=3.7.0
# Thu, 11 Dec 2025 21:21:41 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
USER influxdb3
# Thu, 11 Dec 2025 21:21:41 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 11 Dec 2025 21:21:41 GMT
ENV LOG_FILTER=info
# Thu, 11 Dec 2025 21:21:41 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 11 Dec 2025 21:21:41 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:41 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74568c6b68d3c934c624838bcd2ed98a6e09a1b5b40c414d8d4e135560019db6`  
		Last Modified: Thu, 11 Dec 2025 21:22:09 GMT  
		Size: 6.7 MB (6666160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cda3c42a285ee841f8fe9ae40ddcb0f9d2f61364adb9cdde2ea0e8337d862fb`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63d36e84d1d75f8c55fc4e08ef4cf3d16e4709bad072ab79c20a56973667323`  
		Last Modified: Thu, 11 Dec 2025 21:22:16 GMT  
		Size: 81.4 MB (81403366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26718f5dab0402791ee2a89ac3ce99304e7e8419472882f596d6f195f0ebfd72`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 522.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5df172dc82ce1441dc402a47f3988199f7ac221cb97b9f75e284f948f19179`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5697499ad09f1d7ee9250a650de9b6625ddb259f801147e8162c71e595e8bd79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f67dc65a09282e0a0c60879470c6b04b3c8979ef5648094b84c06cb8e32284`

```dockerfile
```

-	Layers:
	-	`sha256:e3aaa038e533f5961a37565929ad4f0e2b5543c7210a2df786d0cffbf9bd5f5c`  
		Last Modified: Fri, 12 Dec 2025 00:20:59 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d10856ef1689fd366bfe41b9372b4b691a4821620ff492179a59102e6e5226ab`  
		Last Modified: Fri, 12 Dec 2025 00:21:00 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.7.0-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0fbb2417a8c7031186b5620e84fdb0ec0578aa0a996c919536dc25f717e1847e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108280727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2d7163cb03a89afa3b3004c6b7ecfedf5aea042793dd101225b2c1bcba90f5`
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
# Thu, 11 Dec 2025 21:21:25 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 11 Dec 2025 21:21:25 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB_VERSION=3.7.0
# Thu, 11 Dec 2025 21:21:29 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
USER influxdb3
# Thu, 11 Dec 2025 21:21:29 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 11 Dec 2025 21:21:29 GMT
ENV LOG_FILTER=info
# Thu, 11 Dec 2025 21:21:29 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 11 Dec 2025 21:21:29 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:29 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9f45ca4f6eaf2a4a96a97ee68a40c27d591b52bb7021bfff72e6ea8a1f1d34`  
		Last Modified: Thu, 11 Dec 2025 21:22:06 GMT  
		Size: 6.7 MB (6676640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4078d8127dc24b235d348ec18c160bb885a289ef1de179adfec3c0dc13582dc`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82915314d7a4b06fe2466157daa345fd2d30698f4b44b00fa218d4a967d2079`  
		Last Modified: Thu, 11 Dec 2025 21:22:15 GMT  
		Size: 72.7 MB (72737806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210c6be1560e90fbdbb25f7ffe6ad8f13527aa81d6fbc0564c3188571e60f408`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c024c1fb06638838f9b95d87d31fa616b6e9d78e6bec01941337bbefcc418c`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:197c5a19c63aa5698340d1b90e34d81b07f688dc267776c18bde33e0a2f53475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8298d3fd556dbb99fa70a3d4f000aa2b4164a9ece5f6db47203043425f4f42b5`

```dockerfile
```

-	Layers:
	-	`sha256:77eb53b16e16257066afc59798ed7f22a6d7236ecbf257a13988daf278de74e7`  
		Last Modified: Fri, 12 Dec 2025 00:21:04 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd917ae9c4105d437d77fcf6ba410bd93480390d85dcbf7c21c64c5211afa3e9`  
		Last Modified: Fri, 12 Dec 2025 00:21:05 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.7.0-enterprise`

```console
$ docker pull influxdb@sha256:d505d356938a25e2e15a8b2dadf2218b738da021d2ed7392004a817a1de52b20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.7.0-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:e29b41f14d7ad157cbcf017650e4f6dac627554c2d924f9e7ae57884971e1fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125281476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b2acb59bf6a3c5f51048608de0ddb03ce8b1ea1b6a3c7be429cc2228e7a8cd`
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
# Fri, 21 Nov 2025 01:09:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:09:02 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:09:36 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:09:36 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:09:36 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:09:36 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec602172e261977575f11d467ce7288f5db05528add2c6687ed88115e4566d`  
		Last Modified: Fri, 21 Nov 2025 01:09:30 GMT  
		Size: 6.7 MB (6666106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a22f257fc04204500973a158da995dc0be631c882769bc2133d99ec614904`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e633feb1122d323a9eb9cb94f723b7ad8d87cd51101808c25cd5bbb60281774`  
		Last Modified: Fri, 21 Nov 2025 01:10:10 GMT  
		Size: 88.9 MB (88886351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094d85b5cca2f3812331aaae16d49f65afb45edd2d0b9df16c424053b115082f`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77620888035321ce666dd8db02345ec637bd5a5049483f28c2de8982a5004f6`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:525301679e2494bb0c0463ecbc3f21ca1537fe80ba004d612683ea46f86f772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9303d33e2ca892f135c5953d369eb916df97424dd830393dc0467f589286511`

```dockerfile
```

-	Layers:
	-	`sha256:0e3e1236d677c014e3b16c3fd1ebf921a7360ffcdfe9cf29eec7c130ce059033`  
		Last Modified: Fri, 21 Nov 2025 03:20:40 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3683ae9634c5647b18930425cbfea200fc9c2f7cbfbbcb6f782bf146448dd451`  
		Last Modified: Fri, 21 Nov 2025 03:20:41 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.7.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ef0f1b8579a522489edca19bc7f616955496bdd5ee86066034eacbd6b21af53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115463993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0693736329ed32d1736000731a7dc106ae021eddabca28959c72e2ded72fc6bd`
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
# Fri, 21 Nov 2025 01:10:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:10:36 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:11:13 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:11:13 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:11:13 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:11:13 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b215b3151b300b2deec4daf8615f7ecb4bc96eb27db8209830dd66e00903c`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 6.7 MB (6676577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e25c4f8d48f3e4d9c23f68e350c0afbd64652ae03ebf6b59a98a95ddf691d25`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468b79c8366daaff07e38012ca6581d1aee98e31cecfe08b475184ceb20d4d34`  
		Last Modified: Fri, 21 Nov 2025 01:11:54 GMT  
		Size: 79.9 MB (79921134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b10e43e65b0618999012821ca464275048f96d3c3b0c6ef07b99bdd200161c`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cfb6bcaf92a99d2c342aa44899f9a76113610e142d349c264dd6def810c715`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.7.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd577be3b08e4279db3fffc19d22238ef18b07f075369b5ff90308c7338fc21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9e6074b38338411e63bc4d131cc4ec4f561ef77707bf0044ece1c652855c35`

```dockerfile
```

-	Layers:
	-	`sha256:0bac5d7414f7aa16b6033522b5e7e3ad2f6cc6663403d6eb92656f00d4046d09`  
		Last Modified: Fri, 21 Nov 2025 03:20:45 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fd085a2d753c505f26f533794ef16eded8d10389faa4beca71a35c4f978fae`  
		Last Modified: Fri, 21 Nov 2025 03:20:46 GMT  
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
$ docker pull influxdb@sha256:fb25468a7f530001a6d8e33cd762757d2a01a94bcffa548bb6720f6814c723cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:1460eaedd23b77f3e33d0d2f2416040001b9b5b8941b3faf27854809b26b2fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117798544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842428e388e55f6f2d9fe031677c407cfd2351002fee723bbca95f404d4d03f9`
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
# Thu, 11 Dec 2025 21:21:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 11 Dec 2025 21:21:37 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB_VERSION=3.7.0
# Thu, 11 Dec 2025 21:21:41 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
USER influxdb3
# Thu, 11 Dec 2025 21:21:41 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 11 Dec 2025 21:21:41 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 11 Dec 2025 21:21:41 GMT
ENV LOG_FILTER=info
# Thu, 11 Dec 2025 21:21:41 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 11 Dec 2025 21:21:41 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:41 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74568c6b68d3c934c624838bcd2ed98a6e09a1b5b40c414d8d4e135560019db6`  
		Last Modified: Thu, 11 Dec 2025 21:22:09 GMT  
		Size: 6.7 MB (6666160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cda3c42a285ee841f8fe9ae40ddcb0f9d2f61364adb9cdde2ea0e8337d862fb`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63d36e84d1d75f8c55fc4e08ef4cf3d16e4709bad072ab79c20a56973667323`  
		Last Modified: Thu, 11 Dec 2025 21:22:16 GMT  
		Size: 81.4 MB (81403366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26718f5dab0402791ee2a89ac3ce99304e7e8419472882f596d6f195f0ebfd72`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 522.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5df172dc82ce1441dc402a47f3988199f7ac221cb97b9f75e284f948f19179`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5697499ad09f1d7ee9250a650de9b6625ddb259f801147e8162c71e595e8bd79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f67dc65a09282e0a0c60879470c6b04b3c8979ef5648094b84c06cb8e32284`

```dockerfile
```

-	Layers:
	-	`sha256:e3aaa038e533f5961a37565929ad4f0e2b5543c7210a2df786d0cffbf9bd5f5c`  
		Last Modified: Fri, 12 Dec 2025 00:20:59 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d10856ef1689fd366bfe41b9372b4b691a4821620ff492179a59102e6e5226ab`  
		Last Modified: Fri, 12 Dec 2025 00:21:00 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0fbb2417a8c7031186b5620e84fdb0ec0578aa0a996c919536dc25f717e1847e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108280727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2d7163cb03a89afa3b3004c6b7ecfedf5aea042793dd101225b2c1bcba90f5`
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
# Thu, 11 Dec 2025 21:21:25 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 11 Dec 2025 21:21:25 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB_VERSION=3.7.0
# Thu, 11 Dec 2025 21:21:29 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
USER influxdb3
# Thu, 11 Dec 2025 21:21:29 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 11 Dec 2025 21:21:29 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 11 Dec 2025 21:21:29 GMT
ENV LOG_FILTER=info
# Thu, 11 Dec 2025 21:21:29 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 11 Dec 2025 21:21:29 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:29 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9f45ca4f6eaf2a4a96a97ee68a40c27d591b52bb7021bfff72e6ea8a1f1d34`  
		Last Modified: Thu, 11 Dec 2025 21:22:06 GMT  
		Size: 6.7 MB (6676640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4078d8127dc24b235d348ec18c160bb885a289ef1de179adfec3c0dc13582dc`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82915314d7a4b06fe2466157daa345fd2d30698f4b44b00fa218d4a967d2079`  
		Last Modified: Thu, 11 Dec 2025 21:22:15 GMT  
		Size: 72.7 MB (72737806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210c6be1560e90fbdbb25f7ffe6ad8f13527aa81d6fbc0564c3188571e60f408`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c024c1fb06638838f9b95d87d31fa616b6e9d78e6bec01941337bbefcc418c`  
		Last Modified: Thu, 11 Dec 2025 21:22:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:197c5a19c63aa5698340d1b90e34d81b07f688dc267776c18bde33e0a2f53475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8298d3fd556dbb99fa70a3d4f000aa2b4164a9ece5f6db47203043425f4f42b5`

```dockerfile
```

-	Layers:
	-	`sha256:77eb53b16e16257066afc59798ed7f22a6d7236ecbf257a13988daf278de74e7`  
		Last Modified: Fri, 12 Dec 2025 00:21:04 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd917ae9c4105d437d77fcf6ba410bd93480390d85dcbf7c21c64c5211afa3e9`  
		Last Modified: Fri, 12 Dec 2025 00:21:05 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:d505d356938a25e2e15a8b2dadf2218b738da021d2ed7392004a817a1de52b20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:e29b41f14d7ad157cbcf017650e4f6dac627554c2d924f9e7ae57884971e1fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125281476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b2acb59bf6a3c5f51048608de0ddb03ce8b1ea1b6a3c7be429cc2228e7a8cd`
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
# Fri, 21 Nov 2025 01:09:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:09:02 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:09:36 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:09:36 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:09:36 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:09:36 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:09:36 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:09:36 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec602172e261977575f11d467ce7288f5db05528add2c6687ed88115e4566d`  
		Last Modified: Fri, 21 Nov 2025 01:09:30 GMT  
		Size: 6.7 MB (6666106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a22f257fc04204500973a158da995dc0be631c882769bc2133d99ec614904`  
		Last Modified: Fri, 21 Nov 2025 01:09:29 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e633feb1122d323a9eb9cb94f723b7ad8d87cd51101808c25cd5bbb60281774`  
		Last Modified: Fri, 21 Nov 2025 01:10:10 GMT  
		Size: 88.9 MB (88886351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094d85b5cca2f3812331aaae16d49f65afb45edd2d0b9df16c424053b115082f`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77620888035321ce666dd8db02345ec637bd5a5049483f28c2de8982a5004f6`  
		Last Modified: Fri, 21 Nov 2025 01:10:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:525301679e2494bb0c0463ecbc3f21ca1537fe80ba004d612683ea46f86f772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9303d33e2ca892f135c5953d369eb916df97424dd830393dc0467f589286511`

```dockerfile
```

-	Layers:
	-	`sha256:0e3e1236d677c014e3b16c3fd1ebf921a7360ffcdfe9cf29eec7c130ce059033`  
		Last Modified: Fri, 21 Nov 2025 03:20:40 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3683ae9634c5647b18930425cbfea200fc9c2f7cbfbbcb6f782bf146448dd451`  
		Last Modified: Fri, 21 Nov 2025 03:20:41 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ef0f1b8579a522489edca19bc7f616955496bdd5ee86066034eacbd6b21af53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115463993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0693736329ed32d1736000731a7dc106ae021eddabca28959c72e2ded72fc6bd`
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
# Fri, 21 Nov 2025 01:10:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 21 Nov 2025 01:10:36 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_VERSION=3.7.0
# Fri, 21 Nov 2025 01:11:13 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
USER influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 21 Nov 2025 01:11:13 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 21 Nov 2025 01:11:13 GMT
ENV LOG_FILTER=info
# Fri, 21 Nov 2025 01:11:13 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 21 Nov 2025 01:11:13 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 21 Nov 2025 01:11:13 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b215b3151b300b2deec4daf8615f7ecb4bc96eb27db8209830dd66e00903c`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 6.7 MB (6676577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e25c4f8d48f3e4d9c23f68e350c0afbd64652ae03ebf6b59a98a95ddf691d25`  
		Last Modified: Fri, 21 Nov 2025 01:11:40 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468b79c8366daaff07e38012ca6581d1aee98e31cecfe08b475184ceb20d4d34`  
		Last Modified: Fri, 21 Nov 2025 01:11:54 GMT  
		Size: 79.9 MB (79921134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b10e43e65b0618999012821ca464275048f96d3c3b0c6ef07b99bdd200161c`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cfb6bcaf92a99d2c342aa44899f9a76113610e142d349c264dd6def810c715`  
		Last Modified: Fri, 21 Nov 2025 01:11:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd577be3b08e4279db3fffc19d22238ef18b07f075369b5ff90308c7338fc21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9e6074b38338411e63bc4d131cc4ec4f561ef77707bf0044ece1c652855c35`

```dockerfile
```

-	Layers:
	-	`sha256:0bac5d7414f7aa16b6033522b5e7e3ad2f6cc6663403d6eb92656f00d4046d09`  
		Last Modified: Fri, 21 Nov 2025 03:20:45 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3fd085a2d753c505f26f533794ef16eded8d10389faa4beca71a35c4f978fae`  
		Last Modified: Fri, 21 Nov 2025 03:20:46 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:38829bd08b47bbfb23ee8ef98fef45ac59abb78d4d7e451870b7499840e0f365
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:3669bd66e4887f2bf178b5d8c73520eb95abc486476c8ee3a8aeaf3868ed1351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107224021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a462b10f2dcd27d7a4406f83cf3a6e98ba56475d7d3911e9a7313eab988b09bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 21:20:54 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 21:20:54 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:20:54 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Dec 2025 21:20:57 GMT
ENV GOSU_VER=1.19
# Thu, 11 Dec 2025 21:20:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Dec 2025 21:20:57 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:20:57 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:20:57 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:21:01 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:21:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:21:02 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:21:02 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:02 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:21:02 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:21:02 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:21:02 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:21:02 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:21:02 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6c5b7e5184d2694f7e00c18ccf964945fa504c6f4b0c5cc494f95442d5880d`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 9.8 MB (9796290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f105c03a426e1db3e339f90557253cd15a30f3c7e8b8fcafab517255e319c82e`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 6.2 MB (6156973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2466a9669beee52a807e7a8ad5848016cadec7327b552cc6fd681711f3f045`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1a94b5e5630da21f70d35b8e064291b9fa829afa5e577122eacb9d6497adca`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 811.5 KB (811477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e75849e6dcf40b3e9d7652d3134d01175642d3ade6cf14f87b06d5ac9c44e5`  
		Last Modified: Thu, 11 Dec 2025 21:21:54 GMT  
		Size: 50.4 MB (50447116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9e3b9c81fdc8f0fd69a83980787d18a49ef144acf052524f8692a89442e66`  
		Last Modified: Thu, 11 Dec 2025 21:21:51 GMT  
		Size: 11.8 MB (11773793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49739d6301dcf53df0f9dd108470cd8c0f060f94df67b9fc80652a62b44cfebc`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ea8f055b7c0a941d89ad0a4975eb5d7a1a9cce7adf46941978325f74f4c38`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8291d544410a6d7b4d6f5d3849a015051f5627de3771759bccdaa8093061b725`  
		Last Modified: Thu, 11 Dec 2025 21:21:50 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:6d5b211bf2d7c2d4a3b0e5f6baf728ecd6a51ba0a117ef3573e7f0046a29c86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32393d0d3de7f9305de7732e2191c5e2ab332767656e6f0ae5dc0aa0b0d3f75e`

```dockerfile
```

-	Layers:
	-	`sha256:6e72df097c24ad1ce1fe1e0b85621fc7357714ae8750ef5fdfb7496776db0d3a`  
		Last Modified: Fri, 12 Dec 2025 00:20:32 GMT  
		Size: 2.9 MB (2934227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530c203dd6101187fe0ffcb8d239eb488871aa417556ca7851616de9efcdc678`  
		Last Modified: Fri, 12 Dec 2025 00:20:35 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e44fc00219ab59bf3eeb01f3e25906c2e99e15bbccef85120ae793617c435918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103624828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e455c12a2559feec54f152b9b8635f288855284b60696d78bbd67b8864d53a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 21:20:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 21:20:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:20:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Dec 2025 21:20:47 GMT
ENV GOSU_VER=1.19
# Thu, 11 Dec 2025 21:20:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Dec 2025 21:20:47 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:20:47 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:20:47 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:20:51 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:20:51 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:20:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:20:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:20:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:20:53 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:20:53 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:20:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:20:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:20:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:20:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83dbb50e465add987a9b0d1e72615aea4ccec7bc9d2435b8840efc3dcf9cdfb`  
		Last Modified: Thu, 11 Dec 2025 21:21:44 GMT  
		Size: 9.6 MB (9626476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f7c93dccebef7a38bce64ad726968776236be5c93f6b1cb8ffab4bc81477fa`  
		Last Modified: Thu, 11 Dec 2025 21:21:43 GMT  
		Size: 5.8 MB (5790425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e4a7c9ef99e2ea95ad051eae00536222199b00ae7ee71f07db8b4ce070e4c7`  
		Last Modified: Thu, 11 Dec 2025 21:21:43 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1ce2fe5391f29005cd2888b88c013e28b0b9411600b90468bf03dcf44474aa`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 766.4 KB (766375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a863576f426fd1602fbc3b111ec55460504eafd10f5b131246700da6e4d40dd1`  
		Last Modified: Thu, 11 Dec 2025 21:21:46 GMT  
		Size: 48.2 MB (48229384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972cda6778a805a97bdabb7dc52cf316dcb1b53a2185a47c785ce65c544cba10`  
		Last Modified: Thu, 11 Dec 2025 21:21:43 GMT  
		Size: 11.1 MB (11099988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a77950c27edf7b42a43c0e1250aa98e3b13a62ba451c31661de6e0c73ddda1`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d0e64e366cb27aa722087d3390f64b99ba6175f188d64a1e43a82dc2557265`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd9442665675081ef3d0d7557fce092dec17dc64fdc08b6ad5fbdd3ffd10a27`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:7d180abed6483e8c69f3f5eda8c60c6758077fb68714a49d7df5bb0ea7691b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b255cad7c8b2f026cd6745eca49f754747f35565ac970f33982e01fd353a7c71`

```dockerfile
```

-	Layers:
	-	`sha256:9cc905cc79a18336d04c1386f6b444ed0b28be06a8de46597a9209cca8d12c48`  
		Last Modified: Fri, 12 Dec 2025 00:20:40 GMT  
		Size: 2.9 MB (2933707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724010682a39995361c350af48077ed7afc9bf92f4689c37eb49321d243f9898`  
		Last Modified: Fri, 12 Dec 2025 00:20:41 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json
