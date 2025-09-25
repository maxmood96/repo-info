<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.10-data`](#influxdb110-data)
-	[`influxdb:1.10-data-alpine`](#influxdb110-data-alpine)
-	[`influxdb:1.10-meta`](#influxdb110-meta)
-	[`influxdb:1.10-meta-alpine`](#influxdb110-meta-alpine)
-	[`influxdb:1.10.9-data`](#influxdb1109-data)
-	[`influxdb:1.10.9-data-alpine`](#influxdb1109-data-alpine)
-	[`influxdb:1.10.9-meta`](#influxdb1109-meta)
-	[`influxdb:1.10.9-meta-alpine`](#influxdb1109-meta-alpine)
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
-	[`influxdb:3-core`](#influxdb3-core)
-	[`influxdb:3-enterprise`](#influxdb3-enterprise)
-	[`influxdb:3.4-core`](#influxdb34-core)
-	[`influxdb:3.4-enterprise`](#influxdb34-enterprise)
-	[`influxdb:3.4.2-core`](#influxdb342-core)
-	[`influxdb:3.4.2-enterprise`](#influxdb342-enterprise)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:core`](#influxdbcore)
-	[`influxdb:enterprise`](#influxdbenterprise)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:d571fb92c9df1ca1315dedf3725cb035ab48f5e6b7cfcc70ec68c3ae747b6a89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:63d961f83d8a609d7325ff384626f960a5e0922761668c3fa4867dfd4f5a6b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108965577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267456f334b9db0b0c936e628b15b4a9da7d3f0dd4501dc2a5bd4b7b3a2a6016`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 24 Sep 2025 16:08:46 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebbe40dd6978ce6b51e9d84d91a658eb2959635aec29cb2475587fda81e28d1`  
		Last Modified: Mon, 08 Sep 2025 21:54:22 GMT  
		Size: 15.8 MB (15765345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c0741eeae547b79db1d8f06f409ea4dd1d3988134479221650b6ddad311793`  
		Last Modified: Thu, 25 Sep 2025 18:14:53 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6409166c451017e5dd509461eb3761ee542a6ddbda926f2af06a310f06ac98b0`  
		Last Modified: Thu, 25 Sep 2025 18:14:57 GMT  
		Size: 39.4 MB (39439622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b8cea72aefdc1e24008f9840fb943fb3ae5e680bea7617881430923d3062a4`  
		Last Modified: Thu, 25 Sep 2025 18:14:53 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21f641220ba0a924a6c27f10acd0cd35f5b4a1e353ce24c29b896ca31b08ffd`  
		Last Modified: Thu, 25 Sep 2025 18:14:53 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4261cfc47cceb8e3ce01e9236df07fd1169c958e3be025f6af6d6df800c4c042`  
		Last Modified: Thu, 25 Sep 2025 18:14:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:6c5e0d8a73ccf50d16b986afc1da75058f1eafe550798383bca39f75984d34f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4799034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a83aeabfa6b0c391886d00596279b9d0219d5453624751623199c77714e5bfa`

```dockerfile
```

-	Layers:
	-	`sha256:943aab3070349142ffe76d9ba59a80934e1fc116fdcda04bde62970d3ca7c615`  
		Last Modified: Thu, 25 Sep 2025 20:20:21 GMT  
		Size: 4.8 MB (4784326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f1188554920e0fb69ae4a0dd5cf6168a8a1192b24e06f83ff4fde06c552d96`  
		Last Modified: Thu, 25 Sep 2025 20:20:22 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:39f1000e1ba45e4debc6825953ca86605d60b96424374b5b622bafb0e7e05f46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2bbb5b8a21ac0b01ddd7d137a1af05d05fdeb53c48b1c3d203ecd7d7374de86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44219748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d33787099c5e37b8ca8ad554d634a3796a78761e3f637e3a3e882d8eb9d2a4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1151c4e24803748534d8f2c424b33c628b20747fe680aa2c6cc3016313473cb8`  
		Last Modified: Thu, 25 Sep 2025 18:15:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e4bff8a635ecd0cd9cb06217ad6ab933b1343cfc952ee35956d0fc5bf4f54`  
		Last Modified: Thu, 25 Sep 2025 18:15:00 GMT  
		Size: 1.2 MB (1217676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e9ea4a60a5cb5b8bbf9be12800aac61f278096b6635daf35925daa9885b97c`  
		Last Modified: Thu, 25 Sep 2025 18:15:05 GMT  
		Size: 39.4 MB (39379543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5518908f2f34918e00266fb284e8f82f38e8febea96b6836b23880ddeb7a54f7`  
		Last Modified: Thu, 25 Sep 2025 18:15:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8580f8af550fb36ab96fd837140cf115a3aaf06fe0cfda35cf0d1affaa535618`  
		Last Modified: Thu, 25 Sep 2025 18:15:00 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e86b1507a0b6e295a3c61c45082e7449ad841fb50f88bdb65897d229df429`  
		Last Modified: Thu, 25 Sep 2025 18:15:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:908474da660f8ff2fe4c183795a2069be71d6277e4d359b09a60a5880bdaccd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.8 KB (768814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b7bb166fbe5f93bf2b923db8351921eca8db7f033812cca87ca526728da724`

```dockerfile
```

-	Layers:
	-	`sha256:281e1d5d3491d2902956019f3e5452fecca18a36e4dd865c81336d8f13fae153`  
		Last Modified: Thu, 25 Sep 2025 20:20:24 GMT  
		Size: 752.2 KB (752175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81dd4df0bdb629e8279318fcb97b6132b541c528dd42a257ff026f9599a73412`  
		Last Modified: Thu, 25 Sep 2025 20:20:25 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:5874cd3a61350fd968728e28a80d2830dc8515829cdbab561faf98ea5195ab09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:d388aec94f37c9ea42886cc722622299813d7e42c855b4ccfc6b419e97497a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88164805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb30192cade779f4f93947e042abc2bd916704c5e8645012cd3fcb04aa0d23a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 24 Sep 2025 16:08:46 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebbe40dd6978ce6b51e9d84d91a658eb2959635aec29cb2475587fda81e28d1`  
		Last Modified: Mon, 08 Sep 2025 21:54:22 GMT  
		Size: 15.8 MB (15765345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c0741eeae547b79db1d8f06f409ea4dd1d3988134479221650b6ddad311793`  
		Last Modified: Thu, 25 Sep 2025 18:14:53 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce05eb5dfaffeed8fffa3deb9bfd1525e9becd87a6fe7ec4f077d49095196f52`  
		Last Modified: Thu, 25 Sep 2025 18:15:17 GMT  
		Size: 18.6 MB (18640057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae7bb654da9567be3af685dafce11a9869eb56a0e7fe49e5538cd24d9fffc5d`  
		Last Modified: Thu, 25 Sep 2025 18:15:15 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2509b3866ffc9ee09a4741fd8fe2d3f9ecf1f659a47b71a5e160726c380c8f53`  
		Last Modified: Thu, 25 Sep 2025 18:15:15 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:54f04e1ed46354d1e4691eac997d8dd4ce99311ee95b3f75ab718e9aa5ff7e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b197aad2caf9b5def059e29d98be8882a274a775275bec3e39499968b22f82`

```dockerfile
```

-	Layers:
	-	`sha256:7dc788f56ccd2262862cef0ae459354277df2ea044fc96b26924905bab9ade03`  
		Last Modified: Thu, 25 Sep 2025 20:20:29 GMT  
		Size: 4.7 MB (4708306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef2f8835a555fb4ceba72633998d749431f3cb0d2f4ee629e9a2b69775dadb1`  
		Last Modified: Thu, 25 Sep 2025 20:20:29 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:2cf37b6b54c5717fff32b26b2d63b042b274ea6ad3fe7e638ebaecd0d4b4fa9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:93309bb57e927aa5fd716aca673be0073234af17474e772652afa884a6134185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23435281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0122af4201b209666a416d92153185c75d187c8bd838ceea8f1202048acbba9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1151c4e24803748534d8f2c424b33c628b20747fe680aa2c6cc3016313473cb8`  
		Last Modified: Thu, 25 Sep 2025 18:15:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e4bff8a635ecd0cd9cb06217ad6ab933b1343cfc952ee35956d0fc5bf4f54`  
		Last Modified: Thu, 25 Sep 2025 18:15:00 GMT  
		Size: 1.2 MB (1217676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d2f196183a4f353fd3e923f35c22fb4a6c4568d486bfb8bebbce24c68f611a`  
		Last Modified: Thu, 25 Sep 2025 18:15:54 GMT  
		Size: 18.6 MB (18596282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c8829bbacafb058fd6be1755206c8aa6b7cc5d089dff5bb773d58302eb216`  
		Last Modified: Thu, 25 Sep 2025 18:15:52 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e0441ef0c5ff2155371f823990025906ac8cfe7c79f700c4dfda0402f7573a`  
		Last Modified: Thu, 25 Sep 2025 18:15:52 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4813ce72342782ce927b5bb001cb7b5d4422cec6af82155bcf59efddc8c2134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.3 KB (691321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e98861a42b24408eaee82b269e4081fa13cd020f1495160ec3ebabb90d6d29`

```dockerfile
```

-	Layers:
	-	`sha256:f61676f57582452de890dad44869c1c217d918da30facacddcc2ed222deda2b3`  
		Last Modified: Thu, 25 Sep 2025 20:20:34 GMT  
		Size: 676.3 KB (676311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d325431b23d20effbaab1cfe9727e8f93c503eb02bd3748c5d864e911299e215`  
		Last Modified: Thu, 25 Sep 2025 20:20:35 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.9-data`

```console
$ docker pull influxdb@sha256:d571fb92c9df1ca1315dedf3725cb035ab48f5e6b7cfcc70ec68c3ae747b6a89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:63d961f83d8a609d7325ff384626f960a5e0922761668c3fa4867dfd4f5a6b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108965577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267456f334b9db0b0c936e628b15b4a9da7d3f0dd4501dc2a5bd4b7b3a2a6016`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 24 Sep 2025 16:08:46 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebbe40dd6978ce6b51e9d84d91a658eb2959635aec29cb2475587fda81e28d1`  
		Last Modified: Mon, 08 Sep 2025 21:54:22 GMT  
		Size: 15.8 MB (15765345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c0741eeae547b79db1d8f06f409ea4dd1d3988134479221650b6ddad311793`  
		Last Modified: Thu, 25 Sep 2025 18:14:53 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6409166c451017e5dd509461eb3761ee542a6ddbda926f2af06a310f06ac98b0`  
		Last Modified: Thu, 25 Sep 2025 18:14:57 GMT  
		Size: 39.4 MB (39439622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b8cea72aefdc1e24008f9840fb943fb3ae5e680bea7617881430923d3062a4`  
		Last Modified: Thu, 25 Sep 2025 18:14:53 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21f641220ba0a924a6c27f10acd0cd35f5b4a1e353ce24c29b896ca31b08ffd`  
		Last Modified: Thu, 25 Sep 2025 18:14:53 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4261cfc47cceb8e3ce01e9236df07fd1169c958e3be025f6af6d6df800c4c042`  
		Last Modified: Thu, 25 Sep 2025 18:14:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:6c5e0d8a73ccf50d16b986afc1da75058f1eafe550798383bca39f75984d34f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4799034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a83aeabfa6b0c391886d00596279b9d0219d5453624751623199c77714e5bfa`

```dockerfile
```

-	Layers:
	-	`sha256:943aab3070349142ffe76d9ba59a80934e1fc116fdcda04bde62970d3ca7c615`  
		Last Modified: Thu, 25 Sep 2025 20:20:21 GMT  
		Size: 4.8 MB (4784326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f1188554920e0fb69ae4a0dd5cf6168a8a1192b24e06f83ff4fde06c552d96`  
		Last Modified: Thu, 25 Sep 2025 20:20:22 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.9-data-alpine`

```console
$ docker pull influxdb@sha256:39f1000e1ba45e4debc6825953ca86605d60b96424374b5b622bafb0e7e05f46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2bbb5b8a21ac0b01ddd7d137a1af05d05fdeb53c48b1c3d203ecd7d7374de86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44219748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d33787099c5e37b8ca8ad554d634a3796a78761e3f637e3a3e882d8eb9d2a4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1151c4e24803748534d8f2c424b33c628b20747fe680aa2c6cc3016313473cb8`  
		Last Modified: Thu, 25 Sep 2025 18:15:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e4bff8a635ecd0cd9cb06217ad6ab933b1343cfc952ee35956d0fc5bf4f54`  
		Last Modified: Thu, 25 Sep 2025 18:15:00 GMT  
		Size: 1.2 MB (1217676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e9ea4a60a5cb5b8bbf9be12800aac61f278096b6635daf35925daa9885b97c`  
		Last Modified: Thu, 25 Sep 2025 18:15:05 GMT  
		Size: 39.4 MB (39379543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5518908f2f34918e00266fb284e8f82f38e8febea96b6836b23880ddeb7a54f7`  
		Last Modified: Thu, 25 Sep 2025 18:15:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8580f8af550fb36ab96fd837140cf115a3aaf06fe0cfda35cf0d1affaa535618`  
		Last Modified: Thu, 25 Sep 2025 18:15:00 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e86b1507a0b6e295a3c61c45082e7449ad841fb50f88bdb65897d229df429`  
		Last Modified: Thu, 25 Sep 2025 18:15:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:908474da660f8ff2fe4c183795a2069be71d6277e4d359b09a60a5880bdaccd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.8 KB (768814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b7bb166fbe5f93bf2b923db8351921eca8db7f033812cca87ca526728da724`

```dockerfile
```

-	Layers:
	-	`sha256:281e1d5d3491d2902956019f3e5452fecca18a36e4dd865c81336d8f13fae153`  
		Last Modified: Thu, 25 Sep 2025 20:20:24 GMT  
		Size: 752.2 KB (752175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81dd4df0bdb629e8279318fcb97b6132b541c528dd42a257ff026f9599a73412`  
		Last Modified: Thu, 25 Sep 2025 20:20:25 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.9-meta`

```console
$ docker pull influxdb@sha256:5874cd3a61350fd968728e28a80d2830dc8515829cdbab561faf98ea5195ab09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:d388aec94f37c9ea42886cc722622299813d7e42c855b4ccfc6b419e97497a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88164805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb30192cade779f4f93947e042abc2bd916704c5e8645012cd3fcb04aa0d23a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 24 Sep 2025 16:08:46 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebbe40dd6978ce6b51e9d84d91a658eb2959635aec29cb2475587fda81e28d1`  
		Last Modified: Mon, 08 Sep 2025 21:54:22 GMT  
		Size: 15.8 MB (15765345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c0741eeae547b79db1d8f06f409ea4dd1d3988134479221650b6ddad311793`  
		Last Modified: Thu, 25 Sep 2025 18:14:53 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce05eb5dfaffeed8fffa3deb9bfd1525e9becd87a6fe7ec4f077d49095196f52`  
		Last Modified: Thu, 25 Sep 2025 18:15:17 GMT  
		Size: 18.6 MB (18640057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae7bb654da9567be3af685dafce11a9869eb56a0e7fe49e5538cd24d9fffc5d`  
		Last Modified: Thu, 25 Sep 2025 18:15:15 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2509b3866ffc9ee09a4741fd8fe2d3f9ecf1f659a47b71a5e160726c380c8f53`  
		Last Modified: Thu, 25 Sep 2025 18:15:15 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:54f04e1ed46354d1e4691eac997d8dd4ce99311ee95b3f75ab718e9aa5ff7e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b197aad2caf9b5def059e29d98be8882a274a775275bec3e39499968b22f82`

```dockerfile
```

-	Layers:
	-	`sha256:7dc788f56ccd2262862cef0ae459354277df2ea044fc96b26924905bab9ade03`  
		Last Modified: Thu, 25 Sep 2025 20:20:29 GMT  
		Size: 4.7 MB (4708306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef2f8835a555fb4ceba72633998d749431f3cb0d2f4ee629e9a2b69775dadb1`  
		Last Modified: Thu, 25 Sep 2025 20:20:29 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.9-meta-alpine`

```console
$ docker pull influxdb@sha256:2cf37b6b54c5717fff32b26b2d63b042b274ea6ad3fe7e638ebaecd0d4b4fa9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:93309bb57e927aa5fd716aca673be0073234af17474e772652afa884a6134185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23435281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0122af4201b209666a416d92153185c75d187c8bd838ceea8f1202048acbba9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1151c4e24803748534d8f2c424b33c628b20747fe680aa2c6cc3016313473cb8`  
		Last Modified: Thu, 25 Sep 2025 18:15:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e4bff8a635ecd0cd9cb06217ad6ab933b1343cfc952ee35956d0fc5bf4f54`  
		Last Modified: Thu, 25 Sep 2025 18:15:00 GMT  
		Size: 1.2 MB (1217676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d2f196183a4f353fd3e923f35c22fb4a6c4568d486bfb8bebbce24c68f611a`  
		Last Modified: Thu, 25 Sep 2025 18:15:54 GMT  
		Size: 18.6 MB (18596282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c8829bbacafb058fd6be1755206c8aa6b7cc5d089dff5bb773d58302eb216`  
		Last Modified: Thu, 25 Sep 2025 18:15:52 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e0441ef0c5ff2155371f823990025906ac8cfe7c79f700c4dfda0402f7573a`  
		Last Modified: Thu, 25 Sep 2025 18:15:52 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4813ce72342782ce927b5bb001cb7b5d4422cec6af82155bcf59efddc8c2134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.3 KB (691321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e98861a42b24408eaee82b269e4081fa13cd020f1495160ec3ebabb90d6d29`

```dockerfile
```

-	Layers:
	-	`sha256:f61676f57582452de890dad44869c1c217d918da30facacddcc2ed222deda2b3`  
		Last Modified: Thu, 25 Sep 2025 20:20:34 GMT  
		Size: 676.3 KB (676311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d325431b23d20effbaab1cfe9727e8f93c503eb02bd3748c5d864e911299e215`  
		Last Modified: Thu, 25 Sep 2025 20:20:35 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11`

```console
$ docker pull influxdb@sha256:13a41cd673a0ef0b41dad27359fcc9103767c6bd102dce717a0b9f6ce7528695
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:34a2b542ca1cf74efce58c2c5757ed653034859ba1985aaaf564710ae12606ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116164770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc93b3381ffa9277e39f19729569938513ea9f0224fb70f4d5c6d2f9afa7bfa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c8e3e896213b6863ab0e1827fdcff92f9c092183e5d2cbbbc94c087c4f7851`  
		Last Modified: Thu, 25 Sep 2025 01:47:55 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9503cc491f8285f6f0625c2876493f09b50c834c8aaf33db0bdfa16b6780c7f3`  
		Last Modified: Thu, 25 Sep 2025 01:48:01 GMT  
		Size: 43.7 MB (43655252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014804b6a44da69257e848edf503ddcfb264bb9f87f75d95c294d275a82c7c33`  
		Last Modified: Thu, 25 Sep 2025 01:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22484e128bd92c3c4e731489e6001116438158a146fb1bcaf9dadeb7c76e653a`  
		Last Modified: Thu, 25 Sep 2025 01:47:55 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52181eb32dc8fce1248533cdfcd372dfb9bf00824482fcaf74fcfe421242819`  
		Last Modified: Thu, 25 Sep 2025 01:47:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:b2f4f21b8dce62af8028071a3cfea14bf7abc5eb6837c4f45a59e8d3d4272ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabb6259c0d83cfea62be117e8f965130e150dfdbb51aa86b30731309230cddf`

```dockerfile
```

-	Layers:
	-	`sha256:a57ed93dab39e72ef249f444eff142dfaec105735991ffc3a742974cc7c9ce5b`  
		Last Modified: Thu, 25 Sep 2025 02:20:20 GMT  
		Size: 5.1 MB (5078620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef8dee4376f620dcb988c101330565e442244c886fc19d92ebe76d735d6a5549`  
		Last Modified: Thu, 25 Sep 2025 02:20:21 GMT  
		Size: 15.5 KB (15528 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c61bd524d6ab2de143c1a3859062b4b0a4a6c1e9cc1b86af959b2e3e89ec6234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113075412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e082980ec6337884de88bb6d0522792cadd524ee2208e9e388e3a9e56b1a317e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53db565e89c013ddfd7aa8f65d740e518b38e2c3254778b80a95f36c8e9110f`  
		Last Modified: Wed, 24 Sep 2025 20:42:05 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d8f1f38ae417d1d069cb38dd1bed5b9f1e796cfe8b0938068aa347becabac`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 41.1 MB (41118692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c41cc6fff89751a0bba36e5957199e7e31f302bb5036fae248f6b1d78c81f95`  
		Last Modified: Wed, 24 Sep 2025 20:42:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072305075852e42910c84e9e649868657c293e61cf2bfec879a111bd28f7a5b3`  
		Last Modified: Wed, 24 Sep 2025 20:42:06 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f0ad996c925db03c1aa8d8f0151b4f5135db2b0bf874f32fb7b456b14a0571`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:46e0d25940c815754a09cb1c0474a51e16302276d3378f7bb012e3a6a7802f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49116a5f9b6d427174780090dff20a5cd9b1c8b380ad55f91c002978cc07f89e`

```dockerfile
```

-	Layers:
	-	`sha256:7605cb44f4d5c7c2af7b5955e0d57593c9a9c735f7cae50a107b35682cdd4940`  
		Last Modified: Thu, 25 Sep 2025 02:20:26 GMT  
		Size: 5.1 MB (5078085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7386cd3b24a27b7c81fcafec399c440d13b602a6452277ec78681a0a50c1fcf`  
		Last Modified: Thu, 25 Sep 2025 02:20:27 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-alpine`

```console
$ docker pull influxdb@sha256:1a6e3cd3c4ef4f2e93496adee573b0f41dcca3f49d114c2f798ca023b165e47f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f8e41e81325ff6810bff30223a8dafad74a5d2cc44d8b6fd43456a9d80897498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42910480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31443016c597ac7547f2e481b163ef6d8c5f1a3c1fd7258b498845812aa91376`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3c45e0960f73f468b1c3cca987dfc03c0b750169af93afeb2130cdbf9d757b`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 1.2 MB (1217687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd607992f18a72767e3fcf98637d34928ab4d49a0c8bd13e1ebb04ee17112a9`  
		Last Modified: Thu, 25 Sep 2025 01:11:56 GMT  
		Size: 38.1 MB (38069600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01393d06d8e58e859d34fc3266d2a2742dd68e8ae5c868ca968f6eb2e62c4d43`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f17e29fc370a24778a2e406b30332b621275ef1e4fc214fbd64b154cafc8e2`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7ad26c6856d0f25616d37fe4c8e7fbc5d48917c02856dd28cc167168ff70aa`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eddc754283c9c6c037f9393a8ec9f81afa62a1452c53a8665421116f58a33e4`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:d5c5c28a9535e1be2d1e69605f0d5d7b403366a12b02c6ad3d5e0d073f6f8752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.7 KB (757746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9f157a0e4f2c4f52075be0d5fc326440f5f906af7b762b3ec0101e7b8d0b45`

```dockerfile
```

-	Layers:
	-	`sha256:f4815b044ecf29fae64279ec17eb007044cc6406ab0200468d7a052f845aa5d2`  
		Last Modified: Thu, 25 Sep 2025 02:20:28 GMT  
		Size: 739.9 KB (739869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8989e87c3df574ae8677346c0d7bcd80dc5b06e9a950186f9cf742ff88ea6c97`  
		Last Modified: Thu, 25 Sep 2025 02:20:29 GMT  
		Size: 17.9 KB (17877 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6e666a97ca48b6dc1791d3ddc4612be122420b7dc5a163656790567cf3664f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40932862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20dfe53de2f31e0d7b51503c64ef154afccd341089a211bf05e4ebf67f5101af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef102850bc500b854c7a38d5283fbe0726a1f60fed78543ef6c392c1603a3cfa`  
		Last Modified: Wed, 24 Sep 2025 20:41:57 GMT  
		Size: 1.3 MB (1296559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8e3957cfa1e5b49d2d79c743009467fa2f1c1d2722fb29cd49a914dab7d8d8`  
		Last Modified: Wed, 24 Sep 2025 20:42:00 GMT  
		Size: 35.5 MB (35545219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d253d4b4b7bc324a5283fb63d8f3177a09945f487eac2ed76a54d813b412a3`  
		Last Modified: Wed, 24 Sep 2025 20:41:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb8d372908373c3370e961937e82293ba6a991b7731b3ec8bb6ec4b54b58b3b`  
		Last Modified: Wed, 24 Sep 2025 20:41:57 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab12011b6f541f0f809f8e8b45fedcc10c7057e0bfd8992fed5fc0b640fcb14`  
		Last Modified: Wed, 24 Sep 2025 20:41:57 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d2e5c4d6f06f2b6ffed5e794bb1885388e67cd7d82287a7c70165442420394`  
		Last Modified: Wed, 24 Sep 2025 20:41:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:9dc37fac81ffaf43309d01eb087d2268e911de3cb01b0697e96f8ac28ed67c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.1 KB (757083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b78fc6f046db26b86c19bbbc181f38935e2ee9bc8cabfe51ad0e5a24403501`

```dockerfile
```

-	Layers:
	-	`sha256:28bd15a686ffe30143c91e2106e4ede5c1fe34729e41fc2e730ddbd816662b1e`  
		Last Modified: Thu, 25 Sep 2025 02:20:33 GMT  
		Size: 739.1 KB (739096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fddb132dc15ab360f07f4bbf4be173c8737d6c560ec31a8b646b824216d0008e`  
		Last Modified: Thu, 25 Sep 2025 02:20:33 GMT  
		Size: 18.0 KB (17987 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:ad9aec7395ec64c108f6c4ebc8d23e2063932670296787d361e18aaac168ea6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:dd1eb599fdf93c22f242a44dcd56e474082dafe6a840342f23b3261ad3c44387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114677503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9f98cd66028eff43c09e09b2afe604a0ce464d658f05792dd8983bf9f2c503`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 24 Sep 2025 16:08:46 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd81f68f67dadc3f2720d296322206b9fb16d8980052e68e1aaa64e88fb10e2`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333a95030997cd028d80900700a1174473e0205cbddb91b68d8d886f276da288`  
		Last Modified: Thu, 25 Sep 2025 01:11:57 GMT  
		Size: 42.2 MB (42165671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03cb2e6ff1fe512410169aec9acb584d0b0a9a7aad947632d813be4759575ea`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2d7628a7c8e4f1b15da340d7cfa0dfeb0e17e2ed523cfa9f39e8c8a46511d8`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73521b81cb246f68e4d689b17ec8b20f0e5bceb1848dd93b3e69816f1a3a85a6`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:9146019135d715c25c45082368f62f7ebc486c96fae818fa83a7f937f7a99c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4698471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c85771c4cea604fb5f2c6459ef39ecc8ecde1b155f5d4fa7b17fb4d3ae9eb6`

```dockerfile
```

-	Layers:
	-	`sha256:e8beccd93404009fdb55d8ec617b530ab1c418c6a7d0906d85be2dd9019ff340`  
		Last Modified: Thu, 25 Sep 2025 02:20:34 GMT  
		Size: 4.7 MB (4683763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0decf600635ebb59fdb4865a4e63599ce4982068b950b1e2c5ed0822fb091560`  
		Last Modified: Thu, 25 Sep 2025 02:20:35 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:79a152f475ff298df71cd58706e1a14bcb5f19ddceb535325e814d75b04237ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4f85314f22a90ea3da80e052d0563021b63b9d1878cacc97dbf2ab8086be06cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46946036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ba4ab381dc10fbb06ef5fdb72d1d565d310e23dfbd2171546275268d699a41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d6a3f1ca39ef7aecc1aa054022ad806b14759ae15643a076798d5854f5aa7b`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042b4eb3c817da1b0174464d0eec4641de11cd9839ba4c369eaf3d702a601d9a`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 1.2 MB (1217669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d0ca7f1894f7b6f6ee9006850a32bb1045898d76566fb121d2703918a4c6b1`  
		Last Modified: Thu, 25 Sep 2025 01:11:25 GMT  
		Size: 42.1 MB (42105839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda602257b6c21bf51a77ca06b7ac2c712c884e50b5f5a82c37fe1faaed4f54a`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fd55f793e7a90d65824e5f00da6c010601bb1a43bf3fea8f6d78136cf5ab8f`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691072363c753e746abeb7fd61d2dc22cd76ded649696e174fa10d9fc574544f`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:d5eed4ec134e6cc48b3b24056166938ad17605a35632e79a2ced9f022509fab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.0 KB (783019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d46a8890f173290743b1a53dfddc7f06dec11c893cddf84f3fb34e3bfc1a20`

```dockerfile
```

-	Layers:
	-	`sha256:c23a1a6278a0172f9fc42704b4acd75183eae245c6b7d9b04f0036cbb8f0a40e`  
		Last Modified: Thu, 25 Sep 2025 02:20:41 GMT  
		Size: 766.4 KB (766380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84bb2c5583be579d7b91f838fdd30e3f446ac4870133773d5de119ef0b9dd0c6`  
		Last Modified: Thu, 25 Sep 2025 02:20:41 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:0064b0b09f25faa1890fb40ce350fd8fdb239fda305be65477777ad8c56fee2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:a4e4aa5117394c8b5c82384d0d1606884b90fbc3f5a589fbc342a27237bf8e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91106736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88098eb78527c6d766468b9bd89e785c0f7956c70af47026916bef6ae2f3b02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 24 Sep 2025 16:08:46 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6d7e2008b499020f78e58fc25efb15e06a7b2fe348ee6b631f319cfbdb2b3c`  
		Last Modified: Thu, 25 Sep 2025 01:11:25 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d47ffe0887f0f6f12dee87313b7d554c4566a9c52da944402fc2d1e3b677db`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 18.6 MB (18596113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4084d1c51a330d138a86637e916acf7f76a0486d6393e5fd6e1d44782a64c0`  
		Last Modified: Thu, 25 Sep 2025 01:11:25 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564bca22f7e0a208724e6f5c44f6ce1c89472ac95a8f8559bf97dad528cb7382`  
		Last Modified: Thu, 25 Sep 2025 01:11:25 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:88ae7b3b3f733f4ee086f804282c9ea1baf4f3bc6b9f69bba61fdb746e08f02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4603673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d88bc67b9eca80a3d4171660256308cc6576b58b76ac3274b92be9806dc7f69`

```dockerfile
```

-	Layers:
	-	`sha256:983a21bbf72808bbc517afde45c72081b970a9d0828e5d1daea14be6987cc0d5`  
		Last Modified: Thu, 25 Sep 2025 02:20:45 GMT  
		Size: 4.6 MB (4590606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3695cc977de812f16da7744fa280a1a20628ad2fe40dfa9f244033c714e80401`  
		Last Modified: Thu, 25 Sep 2025 02:20:46 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:9a08d01311da9282ba27751a776b405f2a1b98aab7ac04c9cf8dbf1062ca2920
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:30ff364cec9fd19b571f4271d3c53e7d670ca4993f004565a0c9e6818060766f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23388787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1e71058086d3a3f9e592065e485fddbabca3996c1feae3ea675ceb9240bf68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a7d34400c8c5dcbbbf7b7cd40818e869dcd03b967ff1fee7bb14e96e138525`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fb82d0e29221bab1f6b5d12453c4c63d74d830fbded9a1b182a41fa0d313df`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 1.2 MB (1217674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15ae145d2a72a7aea82b29f12d68053e6ed0c44ec880b222c896257fce9dc63`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 18.5 MB (18549791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d72fee249b98bda2b81595a42e765e9d9e8737d6a4191bd1c1f8ce755138364`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1607c10bcc9fd15027c82d9ab4a51faa14afcec3bc8a064fd685e7ff7c9a536`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:674f3427ed7d18b3caa08ce7e4538561ac8dfe80cf65d02d2fe144e0e76b87fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.0 KB (689019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f078f32af95ac7ce888f8d2e179f0dc3413a5cc32ba3eb74c8e7d2cea2531f3d`

```dockerfile
```

-	Layers:
	-	`sha256:9df14aceb0c253e684682fb8eaa7f1c75b4e13ff0d92e0c2dc4bf91d032c7f06`  
		Last Modified: Thu, 25 Sep 2025 02:20:48 GMT  
		Size: 674.0 KB (674009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93a2735de13f578098fc4b19a35562ce3fbad7656d513fb4017422507d78fd31`  
		Last Modified: Thu, 25 Sep 2025 02:20:49 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8`

```console
$ docker pull influxdb@sha256:13a41cd673a0ef0b41dad27359fcc9103767c6bd102dce717a0b9f6ce7528695
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:34a2b542ca1cf74efce58c2c5757ed653034859ba1985aaaf564710ae12606ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116164770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc93b3381ffa9277e39f19729569938513ea9f0224fb70f4d5c6d2f9afa7bfa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c8e3e896213b6863ab0e1827fdcff92f9c092183e5d2cbbbc94c087c4f7851`  
		Last Modified: Thu, 25 Sep 2025 01:47:55 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9503cc491f8285f6f0625c2876493f09b50c834c8aaf33db0bdfa16b6780c7f3`  
		Last Modified: Thu, 25 Sep 2025 01:48:01 GMT  
		Size: 43.7 MB (43655252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014804b6a44da69257e848edf503ddcfb264bb9f87f75d95c294d275a82c7c33`  
		Last Modified: Thu, 25 Sep 2025 01:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22484e128bd92c3c4e731489e6001116438158a146fb1bcaf9dadeb7c76e653a`  
		Last Modified: Thu, 25 Sep 2025 01:47:55 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52181eb32dc8fce1248533cdfcd372dfb9bf00824482fcaf74fcfe421242819`  
		Last Modified: Thu, 25 Sep 2025 01:47:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:b2f4f21b8dce62af8028071a3cfea14bf7abc5eb6837c4f45a59e8d3d4272ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabb6259c0d83cfea62be117e8f965130e150dfdbb51aa86b30731309230cddf`

```dockerfile
```

-	Layers:
	-	`sha256:a57ed93dab39e72ef249f444eff142dfaec105735991ffc3a742974cc7c9ce5b`  
		Last Modified: Thu, 25 Sep 2025 02:20:20 GMT  
		Size: 5.1 MB (5078620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef8dee4376f620dcb988c101330565e442244c886fc19d92ebe76d735d6a5549`  
		Last Modified: Thu, 25 Sep 2025 02:20:21 GMT  
		Size: 15.5 KB (15528 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c61bd524d6ab2de143c1a3859062b4b0a4a6c1e9cc1b86af959b2e3e89ec6234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113075412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e082980ec6337884de88bb6d0522792cadd524ee2208e9e388e3a9e56b1a317e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53db565e89c013ddfd7aa8f65d740e518b38e2c3254778b80a95f36c8e9110f`  
		Last Modified: Wed, 24 Sep 2025 20:42:05 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d8f1f38ae417d1d069cb38dd1bed5b9f1e796cfe8b0938068aa347becabac`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 41.1 MB (41118692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c41cc6fff89751a0bba36e5957199e7e31f302bb5036fae248f6b1d78c81f95`  
		Last Modified: Wed, 24 Sep 2025 20:42:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072305075852e42910c84e9e649868657c293e61cf2bfec879a111bd28f7a5b3`  
		Last Modified: Wed, 24 Sep 2025 20:42:06 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f0ad996c925db03c1aa8d8f0151b4f5135db2b0bf874f32fb7b456b14a0571`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:46e0d25940c815754a09cb1c0474a51e16302276d3378f7bb012e3a6a7802f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49116a5f9b6d427174780090dff20a5cd9b1c8b380ad55f91c002978cc07f89e`

```dockerfile
```

-	Layers:
	-	`sha256:7605cb44f4d5c7c2af7b5955e0d57593c9a9c735f7cae50a107b35682cdd4940`  
		Last Modified: Thu, 25 Sep 2025 02:20:26 GMT  
		Size: 5.1 MB (5078085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7386cd3b24a27b7c81fcafec399c440d13b602a6452277ec78681a0a50c1fcf`  
		Last Modified: Thu, 25 Sep 2025 02:20:27 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-alpine`

```console
$ docker pull influxdb@sha256:1a6e3cd3c4ef4f2e93496adee573b0f41dcca3f49d114c2f798ca023b165e47f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f8e41e81325ff6810bff30223a8dafad74a5d2cc44d8b6fd43456a9d80897498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42910480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31443016c597ac7547f2e481b163ef6d8c5f1a3c1fd7258b498845812aa91376`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3c45e0960f73f468b1c3cca987dfc03c0b750169af93afeb2130cdbf9d757b`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 1.2 MB (1217687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd607992f18a72767e3fcf98637d34928ab4d49a0c8bd13e1ebb04ee17112a9`  
		Last Modified: Thu, 25 Sep 2025 01:11:56 GMT  
		Size: 38.1 MB (38069600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01393d06d8e58e859d34fc3266d2a2742dd68e8ae5c868ca968f6eb2e62c4d43`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f17e29fc370a24778a2e406b30332b621275ef1e4fc214fbd64b154cafc8e2`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7ad26c6856d0f25616d37fe4c8e7fbc5d48917c02856dd28cc167168ff70aa`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eddc754283c9c6c037f9393a8ec9f81afa62a1452c53a8665421116f58a33e4`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:d5c5c28a9535e1be2d1e69605f0d5d7b403366a12b02c6ad3d5e0d073f6f8752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.7 KB (757746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9f157a0e4f2c4f52075be0d5fc326440f5f906af7b762b3ec0101e7b8d0b45`

```dockerfile
```

-	Layers:
	-	`sha256:f4815b044ecf29fae64279ec17eb007044cc6406ab0200468d7a052f845aa5d2`  
		Last Modified: Thu, 25 Sep 2025 02:20:28 GMT  
		Size: 739.9 KB (739869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8989e87c3df574ae8677346c0d7bcd80dc5b06e9a950186f9cf742ff88ea6c97`  
		Last Modified: Thu, 25 Sep 2025 02:20:29 GMT  
		Size: 17.9 KB (17877 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6e666a97ca48b6dc1791d3ddc4612be122420b7dc5a163656790567cf3664f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40932862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20dfe53de2f31e0d7b51503c64ef154afccd341089a211bf05e4ebf67f5101af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef102850bc500b854c7a38d5283fbe0726a1f60fed78543ef6c392c1603a3cfa`  
		Last Modified: Wed, 24 Sep 2025 20:41:57 GMT  
		Size: 1.3 MB (1296559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8e3957cfa1e5b49d2d79c743009467fa2f1c1d2722fb29cd49a914dab7d8d8`  
		Last Modified: Wed, 24 Sep 2025 20:42:00 GMT  
		Size: 35.5 MB (35545219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d253d4b4b7bc324a5283fb63d8f3177a09945f487eac2ed76a54d813b412a3`  
		Last Modified: Wed, 24 Sep 2025 20:41:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb8d372908373c3370e961937e82293ba6a991b7731b3ec8bb6ec4b54b58b3b`  
		Last Modified: Wed, 24 Sep 2025 20:41:57 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab12011b6f541f0f809f8e8b45fedcc10c7057e0bfd8992fed5fc0b640fcb14`  
		Last Modified: Wed, 24 Sep 2025 20:41:57 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d2e5c4d6f06f2b6ffed5e794bb1885388e67cd7d82287a7c70165442420394`  
		Last Modified: Wed, 24 Sep 2025 20:41:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:9dc37fac81ffaf43309d01eb087d2268e911de3cb01b0697e96f8ac28ed67c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.1 KB (757083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b78fc6f046db26b86c19bbbc181f38935e2ee9bc8cabfe51ad0e5a24403501`

```dockerfile
```

-	Layers:
	-	`sha256:28bd15a686ffe30143c91e2106e4ede5c1fe34729e41fc2e730ddbd816662b1e`  
		Last Modified: Thu, 25 Sep 2025 02:20:33 GMT  
		Size: 739.1 KB (739096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fddb132dc15ab360f07f4bbf4be173c8737d6c560ec31a8b646b824216d0008e`  
		Last Modified: Thu, 25 Sep 2025 02:20:33 GMT  
		Size: 18.0 KB (17987 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-data`

```console
$ docker pull influxdb@sha256:ad9aec7395ec64c108f6c4ebc8d23e2063932670296787d361e18aaac168ea6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:dd1eb599fdf93c22f242a44dcd56e474082dafe6a840342f23b3261ad3c44387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114677503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9f98cd66028eff43c09e09b2afe604a0ce464d658f05792dd8983bf9f2c503`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 24 Sep 2025 16:08:46 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd81f68f67dadc3f2720d296322206b9fb16d8980052e68e1aaa64e88fb10e2`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333a95030997cd028d80900700a1174473e0205cbddb91b68d8d886f276da288`  
		Last Modified: Thu, 25 Sep 2025 01:11:57 GMT  
		Size: 42.2 MB (42165671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03cb2e6ff1fe512410169aec9acb584d0b0a9a7aad947632d813be4759575ea`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2d7628a7c8e4f1b15da340d7cfa0dfeb0e17e2ed523cfa9f39e8c8a46511d8`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73521b81cb246f68e4d689b17ec8b20f0e5bceb1848dd93b3e69816f1a3a85a6`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:9146019135d715c25c45082368f62f7ebc486c96fae818fa83a7f937f7a99c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4698471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c85771c4cea604fb5f2c6459ef39ecc8ecde1b155f5d4fa7b17fb4d3ae9eb6`

```dockerfile
```

-	Layers:
	-	`sha256:e8beccd93404009fdb55d8ec617b530ab1c418c6a7d0906d85be2dd9019ff340`  
		Last Modified: Thu, 25 Sep 2025 02:20:34 GMT  
		Size: 4.7 MB (4683763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0decf600635ebb59fdb4865a4e63599ce4982068b950b1e2c5ed0822fb091560`  
		Last Modified: Thu, 25 Sep 2025 02:20:35 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-data-alpine`

```console
$ docker pull influxdb@sha256:79a152f475ff298df71cd58706e1a14bcb5f19ddceb535325e814d75b04237ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4f85314f22a90ea3da80e052d0563021b63b9d1878cacc97dbf2ab8086be06cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46946036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ba4ab381dc10fbb06ef5fdb72d1d565d310e23dfbd2171546275268d699a41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d6a3f1ca39ef7aecc1aa054022ad806b14759ae15643a076798d5854f5aa7b`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042b4eb3c817da1b0174464d0eec4641de11cd9839ba4c369eaf3d702a601d9a`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 1.2 MB (1217669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d0ca7f1894f7b6f6ee9006850a32bb1045898d76566fb121d2703918a4c6b1`  
		Last Modified: Thu, 25 Sep 2025 01:11:25 GMT  
		Size: 42.1 MB (42105839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda602257b6c21bf51a77ca06b7ac2c712c884e50b5f5a82c37fe1faaed4f54a`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fd55f793e7a90d65824e5f00da6c010601bb1a43bf3fea8f6d78136cf5ab8f`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691072363c753e746abeb7fd61d2dc22cd76ded649696e174fa10d9fc574544f`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:d5eed4ec134e6cc48b3b24056166938ad17605a35632e79a2ced9f022509fab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.0 KB (783019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d46a8890f173290743b1a53dfddc7f06dec11c893cddf84f3fb34e3bfc1a20`

```dockerfile
```

-	Layers:
	-	`sha256:c23a1a6278a0172f9fc42704b4acd75183eae245c6b7d9b04f0036cbb8f0a40e`  
		Last Modified: Thu, 25 Sep 2025 02:20:41 GMT  
		Size: 766.4 KB (766380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84bb2c5583be579d7b91f838fdd30e3f446ac4870133773d5de119ef0b9dd0c6`  
		Last Modified: Thu, 25 Sep 2025 02:20:41 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-meta`

```console
$ docker pull influxdb@sha256:0064b0b09f25faa1890fb40ce350fd8fdb239fda305be65477777ad8c56fee2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:a4e4aa5117394c8b5c82384d0d1606884b90fbc3f5a589fbc342a27237bf8e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91106736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88098eb78527c6d766468b9bd89e785c0f7956c70af47026916bef6ae2f3b02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 24 Sep 2025 16:08:46 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6d7e2008b499020f78e58fc25efb15e06a7b2fe348ee6b631f319cfbdb2b3c`  
		Last Modified: Thu, 25 Sep 2025 01:11:25 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d47ffe0887f0f6f12dee87313b7d554c4566a9c52da944402fc2d1e3b677db`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 18.6 MB (18596113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4084d1c51a330d138a86637e916acf7f76a0486d6393e5fd6e1d44782a64c0`  
		Last Modified: Thu, 25 Sep 2025 01:11:25 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564bca22f7e0a208724e6f5c44f6ce1c89472ac95a8f8559bf97dad528cb7382`  
		Last Modified: Thu, 25 Sep 2025 01:11:25 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:88ae7b3b3f733f4ee086f804282c9ea1baf4f3bc6b9f69bba61fdb746e08f02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4603673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d88bc67b9eca80a3d4171660256308cc6576b58b76ac3274b92be9806dc7f69`

```dockerfile
```

-	Layers:
	-	`sha256:983a21bbf72808bbc517afde45c72081b970a9d0828e5d1daea14be6987cc0d5`  
		Last Modified: Thu, 25 Sep 2025 02:20:45 GMT  
		Size: 4.6 MB (4590606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3695cc977de812f16da7744fa280a1a20628ad2fe40dfa9f244033c714e80401`  
		Last Modified: Thu, 25 Sep 2025 02:20:46 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-meta-alpine`

```console
$ docker pull influxdb@sha256:9a08d01311da9282ba27751a776b405f2a1b98aab7ac04c9cf8dbf1062ca2920
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:30ff364cec9fd19b571f4271d3c53e7d670ca4993f004565a0c9e6818060766f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23388787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1e71058086d3a3f9e592065e485fddbabca3996c1feae3ea675ceb9240bf68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a7d34400c8c5dcbbbf7b7cd40818e869dcd03b967ff1fee7bb14e96e138525`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fb82d0e29221bab1f6b5d12453c4c63d74d830fbded9a1b182a41fa0d313df`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 1.2 MB (1217674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15ae145d2a72a7aea82b29f12d68053e6ed0c44ec880b222c896257fce9dc63`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 18.5 MB (18549791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d72fee249b98bda2b81595a42e765e9d9e8737d6a4191bd1c1f8ce755138364`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1607c10bcc9fd15027c82d9ab4a51faa14afcec3bc8a064fd685e7ff7c9a536`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:674f3427ed7d18b3caa08ce7e4538561ac8dfe80cf65d02d2fe144e0e76b87fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.0 KB (689019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f078f32af95ac7ce888f8d2e179f0dc3413a5cc32ba3eb74c8e7d2cea2531f3d`

```dockerfile
```

-	Layers:
	-	`sha256:9df14aceb0c253e684682fb8eaa7f1c75b4e13ff0d92e0c2dc4bf91d032c7f06`  
		Last Modified: Thu, 25 Sep 2025 02:20:48 GMT  
		Size: 674.0 KB (674009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93a2735de13f578098fc4b19a35562ce3fbad7656d513fb4017422507d78fd31`  
		Last Modified: Thu, 25 Sep 2025 02:20:49 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12`

```console
$ docker pull influxdb@sha256:de34f21d0bc5aefceff2e2820de2e109b17d70539e4f5554d124add5b206adc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12` - linux; amd64

```console
$ docker pull influxdb@sha256:426ab062a68abef58ac58a7a4b23d0b37e0a3b864d4f9afe939fa0dee5dddd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113839835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a9a4f2767547c05a95f7eba88b47f8864db49d6175c347f8ac0e867328fba1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9af5d0925cec06da9d20ea0743cf4915eafbc0c00270914b75821ac256a4285`  
		Last Modified: Thu, 25 Sep 2025 01:10:59 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492d7502c6bcb2683a01642fe0653ba2584d4674a6669b02a84d7bb43987b163`  
		Last Modified: Thu, 25 Sep 2025 01:11:04 GMT  
		Size: 41.3 MB (41330316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72ce16b2f73d6deff4d01bedd5f2f8bbc25853475c63fe7de4bd7dbdc0ac5a3`  
		Last Modified: Thu, 25 Sep 2025 01:10:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc581aa0649c7b97abddce117abfb6c315bf70be7d0cd9fdab2d635531a77fa`  
		Last Modified: Thu, 25 Sep 2025 01:10:59 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93a5ae6bd9b329e5073f2f940e99118861ef9f46a63f4a617e010fb3ef7794e`  
		Last Modified: Thu, 25 Sep 2025 01:10:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:7bc254833d0d5b503087f7994a3e0309046b554c180e1d8df8c5813b34504fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6bb2b1a7cae7adfa63737e63a81b086dbe501d1be857dca03abc515980fc1d`

```dockerfile
```

-	Layers:
	-	`sha256:425d61644b2ed41c813169900705974547e01ec308dbe2efd51c29da43fff03d`  
		Last Modified: Thu, 25 Sep 2025 02:21:08 GMT  
		Size: 4.7 MB (4675813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e782921a7e16320301d3e52b72374e2eb7ddc44b849e21feb8c234d16f78fe80`  
		Last Modified: Thu, 25 Sep 2025 02:21:09 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:53fb521ae05584264606185211fc7cb420181cab87c8aadc2e63a8215efde57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110087437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0da1f3181c9cc48b9d164d0dd3d42064625c41a43324cbd05736e7224aa051`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7751095df082bb36fbdf41936eb5e7f878571a8a846feeff96b113c6217e77f0`  
		Last Modified: Wed, 24 Sep 2025 20:41:58 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbac4123333e136ece841a309f3427512ade943728e2a04b2a02859c7d66a16`  
		Last Modified: Wed, 24 Sep 2025 20:42:02 GMT  
		Size: 38.1 MB (38130718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eab60e18f77b4310dd0b49fe505f24f7728a71ade85d0ea12ee7cac4c1fcdd1`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0920398efc022a62518752fa4dc4d662c2da979c0ae307c30d3987edcafa01d`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958e4e08bfcb68da732d4e039153d749641b857652d307b714249490beda9656`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:32395c47f606c1ba73e1a6d03ebe4e30a012f693a1c72338b80ecd6b93c0d00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4691865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f20924e4593145c03937f47325f42287a592111dfbdc5e9bf262cf6d40c20c`

```dockerfile
```

-	Layers:
	-	`sha256:11903a41af016385feeb7f926cc07ea645c0e44a0ec102e2a86234a64ecd9c09`  
		Last Modified: Thu, 25 Sep 2025 02:21:13 GMT  
		Size: 4.7 MB (4675271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:595c561ed9a5f1e1adbb47d688c7602bbb57a162be04d7c8e01376cd2835f183`  
		Last Modified: Thu, 25 Sep 2025 02:21:14 GMT  
		Size: 16.6 KB (16594 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-alpine`

```console
$ docker pull influxdb@sha256:a414cd63127794632745243d4bce4eebd7735cf550f742ef3a43458815b805ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:66d2329a46d68b73f4fe44a8ecc2e1a66c470cc0bf686b41d474b82dc4819099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46109705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b598749460a540b8467edfc5d27c9176d36136f5fbf77bdf7998e8cbaaf242b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf29fd72ecc1ce907ef679e6691bffbc6e2441190fac83926e70c94cf8d3c33a`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.2 MB (1217859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7298ddb7262ac5ecf38aa23565daab66ab05f51c43a14cf5094e40b4eba6cf7e`  
		Last Modified: Thu, 25 Sep 2025 01:11:28 GMT  
		Size: 41.3 MB (41251563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6d2c35dfc301a4fc344c4cc21bf0203d7b27545d02a185d3463c8c24eeb0d1`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c194518376314b2bd83490bbd01e606f06f23d11d0650ab68d302fbaa00e1b`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 997.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9b3690d762b0518bf4a2221226cc44c7680f52ff820f551e0f5ebd8edf34b5`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc091ce4196a6f6ef52a63c0824ad8f0f9661d03cfdaff16c8aa50d57dba59d`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:199e04d8292a4a75cb8a67a517df3c22c97564ba5d49254ff4db29914ee1f964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.9 KB (777909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238053bdd74f2651b16896d6bfbae7baf7a3fae84043e53a238d989bd8d682e0`

```dockerfile
```

-	Layers:
	-	`sha256:8bd1cb6b6e76e5c1e3b5cb4aef4fa7fd296fe013ec246031ba29d39d510a2cd1`  
		Last Modified: Thu, 25 Sep 2025 02:21:17 GMT  
		Size: 759.2 KB (759246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0bc5543f212c999f8c987694aead38c4b1205df87986ae131f6bdb3890d500`  
		Last Modified: Thu, 25 Sep 2025 02:21:18 GMT  
		Size: 18.7 KB (18663 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:81c4c76971e3becd6b38181251d3f78a774f235d75eaba3aefdf9ef55da5e5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43330814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf8f03c66704fa0bfde412001f104a8b686422ccb508c0d75ed7897528f9e0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb859780c099b20f6b1c19da90718ff441cf554fbf9fea5ce8bf88b2b342b27`  
		Last Modified: Wed, 24 Sep 2025 20:41:58 GMT  
		Size: 1.3 MB (1281995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4a2ea34cebba0e887e846c07a26b4b81dff4512d981cd60d18ee25c41dc54d`  
		Last Modified: Wed, 24 Sep 2025 20:42:01 GMT  
		Size: 38.1 MB (38059175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d1b64b38d090d2af54a47b8c3f497728a03364e5f5e3b03614f750e5d7d8fe`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7cf7191a46764e43da4fd29896b77aea2cd4b4f3addb1b78aa9665aa1906d0`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 994.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ca1e114aa3f7032cc94571dbd85f0e722edf9494f8d6690c156f853c443611`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f0ad996c925db03c1aa8d8f0151b4f5135db2b0bf874f32fb7b456b14a0571`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:7ba5e12a498af66276c54313990918a6091e9a100dc86622c647bd0f9994a860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.2 KB (777248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a49d7488c6e63d06c7801ebbda6b93b0e47fb09ec8e2a3423c4ef5f03ed09e7`

```dockerfile
```

-	Layers:
	-	`sha256:673a56ea96e4b0691dbec6d531ee2405386a405eae9fad2677ca9bac97882854`  
		Last Modified: Thu, 25 Sep 2025 02:21:21 GMT  
		Size: 758.5 KB (758475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0e2ef2cb88495c0a131cac294254ab280c5d8afb5b7a9754470a20026536ab0`  
		Last Modified: Thu, 25 Sep 2025 02:21:22 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data`

```console
$ docker pull influxdb@sha256:d8c4c34372a99ce2e675ff3947e94037c1851e6cc8be5a57a575d804b35e83b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data` - linux; amd64

```console
$ docker pull influxdb@sha256:1dcacb67df100503cbf1d690e634405636bab187c3411c0d8e1fb28ff1b6b6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114824093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d205e65066024ac15edd7559c9364fb002ad4f37dc5fca14be354915c0b0eeba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525dacd1718a9a4306658abd11b9a7874983c28e8a2e30026225bca0cec2c74f`  
		Last Modified: Thu, 25 Sep 2025 01:11:25 GMT  
		Size: 42.3 MB (42315710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0f30bd18a3ef0ad3bbc7b214a79107a3a2e478b8d7bbacdb35c89346794e3b`  
		Last Modified: Thu, 25 Sep 2025 01:11:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0591c5c9402800570b5222d1b35bb55ff2b165c28d3611b96d04e40a37d3d884`  
		Last Modified: Thu, 25 Sep 2025 01:11:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc091ce4196a6f6ef52a63c0824ad8f0f9661d03cfdaff16c8aa50d57dba59d`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:a0f5adb89f60c9b4213fd2e2d8df18a519549ea804d361c2bceeb41377311f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97e28a0b904717f5628514c176a7400334f84c84444c22b87c6e7f80db485db`

```dockerfile
```

-	Layers:
	-	`sha256:3c92aa4140d1e1ef715ba9e1005c4451882845f840da63bfc1ace5836ec4c018`  
		Last Modified: Thu, 25 Sep 2025 02:21:21 GMT  
		Size: 4.7 MB (4685451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea4330030334318f7d614ce79e4edc724b2f3b75f46e8e3b08f98911e71e3123`  
		Last Modified: Thu, 25 Sep 2025 02:21:22 GMT  
		Size: 13.8 KB (13822 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data-alpine`

```console
$ docker pull influxdb@sha256:230248f4122b55660ea2f78e44d60d589b8cf6cb8ab48f5fa11355b2aa3437a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c6d9a496ea1ac3bfbb8fe7051352b68e5687cbce7cc4ade9e4dc92906d70d3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47111314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349217c040d7cb8d5ba819df95857de62d7b8c65fe537e562f9eedab6cd09781`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69f86ebefe9dfff24be9ab53cd975a2631738b7447af6789e1dff1ca3b2c27f`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.2 MB (1217842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d614cbfebd68939215609c41e791fa77b4faf9c0184838f6f2e088d147d90b`  
		Last Modified: Thu, 25 Sep 2025 01:11:20 GMT  
		Size: 42.3 MB (42254130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b27779e2d36c38b820659ca7fc3113c1733a2a5525df9062e31317c6e945791`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042f205ee4f2c54dd0fab79d5ff8ab7fc2d8b532b3b6bf65e1214a3ba864e2b6`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc48483cf9f08acfa785e7133e964bccc86be159a441243a8c2e7bf35f5c5a3`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cae64fd7f9afd9ae2714d996f632407d49177f7187e1ea8f0f0cfcc147b719ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **788.4 KB (788388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc8318dc7f4dd8e8855ad80626a177cb044360e5746e29e2d607ff65ac2aa6a`

```dockerfile
```

-	Layers:
	-	`sha256:a071aa26d75f72d4bd7f30c81a59364f35b5553a0d5e391470b451a6d0354062`  
		Last Modified: Thu, 25 Sep 2025 02:21:25 GMT  
		Size: 773.2 KB (773197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e9386bff0d6db73eee18d185455902b386dab3efc2240f66243aa380eba25a`  
		Last Modified: Thu, 25 Sep 2025 02:21:26 GMT  
		Size: 15.2 KB (15191 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta`

```console
$ docker pull influxdb@sha256:b4a18ca2506d6629ed097814309b393e33a026ac3f82cb901854fc2b8fd967bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:dc0bbc5ea6748757e54723a9b5b4ce145c57599d73bf86d3567a337d67a53250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91286168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd45c40e53c65286de17822b9851343ef1755fef293630119aa6de6148fd14a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80815c6fd7d7a52c20814c13cef8c36f4bb487b8375dd627f5dcf0ce5b9308c8`  
		Last Modified: Thu, 25 Sep 2025 01:11:11 GMT  
		Size: 18.8 MB (18778993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4f5d4f083ee73460a98f9568ab2ce0bbb89f3b0c2c246b8743471c9561fe93`  
		Last Modified: Thu, 25 Sep 2025 01:11:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e31010df7fb30794fe3614ffadd762a00456fc61ece5d2556bbbc0fa1252fc`  
		Last Modified: Thu, 25 Sep 2025 01:11:08 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:c1e318716cd76b6ddaa0a92e89b5af10892b4071a1e7a2df2e392bed3fe654a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4602950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f401843f67b2566ff0936e7fe3108a695abecb455b3aab1b8265f7cb26c3797c`

```dockerfile
```

-	Layers:
	-	`sha256:6a7c0705f078bd9566af2b64c6ec32e6b7be1705661371576bb13420c365ccac`  
		Last Modified: Thu, 25 Sep 2025 02:21:31 GMT  
		Size: 4.6 MB (4590614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b96dbac04e4531691f4d49dc6a3a95c908a88cd33ae596271f93ed53b160f7`  
		Last Modified: Thu, 25 Sep 2025 02:21:32 GMT  
		Size: 12.3 KB (12336 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta-alpine`

```console
$ docker pull influxdb@sha256:fb1c6ce882c6f76575bf00e884eb6a1cb48f015f6dced8852e0632304e0f5e18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:438d52e3d15ecb0301ecc4b86a960ee9bc6fce7f38f9d2e372347c8525563ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23578256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b60e5178733d55db673306b947c186ea7867ea6067cff2db7b2e658a86d9c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influxd-ctl'             'influxdb-*/usr/bin/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f49da720c3a823002c9dc61fb96fe6cbaef56f95b70e83f1717b0cbfe3625c2`  
		Last Modified: Thu, 25 Sep 2025 01:11:07 GMT  
		Size: 1.2 MB (1217796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b26514951c314740b0ec3a65e5c10800f94cd828599759c28c959a27cce08fc`  
		Last Modified: Thu, 25 Sep 2025 01:11:08 GMT  
		Size: 18.7 MB (18722325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a69a5b526bf15a075a5b6a8f416149db75a74b0e83960585a33600795990c9e`  
		Last Modified: Thu, 25 Sep 2025 01:11:07 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaf0d00f6e38d9ddf873ead6554c87a4c001319e00556ec54da121d35ad3db6`  
		Last Modified: Thu, 25 Sep 2025 01:11:07 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:66c0c255fb30f22da06e4e5eb91e6feab97a584430550d8c5fa3641c6e9adc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.7 KB (692723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c204ee4a35a8f1aa76d61d64fe38ae6354d2b8fc6deff8188661dddd18a645`

```dockerfile
```

-	Layers:
	-	`sha256:b6e4d83eeb239e60792a85b357d7d2758fca1759d804b3b06c1ca78d6b90f827`  
		Last Modified: Thu, 25 Sep 2025 02:21:34 GMT  
		Size: 679.1 KB (679146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d892543fbfacd30d46f77df1c4f2bad94927a6e55b406e2082cebc6a60b88c7d`  
		Last Modified: Thu, 25 Sep 2025 02:21:35 GMT  
		Size: 13.6 KB (13577 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2`

```console
$ docker pull influxdb@sha256:de34f21d0bc5aefceff2e2820de2e109b17d70539e4f5554d124add5b206adc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.2` - linux; amd64

```console
$ docker pull influxdb@sha256:426ab062a68abef58ac58a7a4b23d0b37e0a3b864d4f9afe939fa0dee5dddd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113839835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a9a4f2767547c05a95f7eba88b47f8864db49d6175c347f8ac0e867328fba1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9af5d0925cec06da9d20ea0743cf4915eafbc0c00270914b75821ac256a4285`  
		Last Modified: Thu, 25 Sep 2025 01:10:59 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492d7502c6bcb2683a01642fe0653ba2584d4674a6669b02a84d7bb43987b163`  
		Last Modified: Thu, 25 Sep 2025 01:11:04 GMT  
		Size: 41.3 MB (41330316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72ce16b2f73d6deff4d01bedd5f2f8bbc25853475c63fe7de4bd7dbdc0ac5a3`  
		Last Modified: Thu, 25 Sep 2025 01:10:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc581aa0649c7b97abddce117abfb6c315bf70be7d0cd9fdab2d635531a77fa`  
		Last Modified: Thu, 25 Sep 2025 01:10:59 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93a5ae6bd9b329e5073f2f940e99118861ef9f46a63f4a617e010fb3ef7794e`  
		Last Modified: Thu, 25 Sep 2025 01:10:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:7bc254833d0d5b503087f7994a3e0309046b554c180e1d8df8c5813b34504fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6bb2b1a7cae7adfa63737e63a81b086dbe501d1be857dca03abc515980fc1d`

```dockerfile
```

-	Layers:
	-	`sha256:425d61644b2ed41c813169900705974547e01ec308dbe2efd51c29da43fff03d`  
		Last Modified: Thu, 25 Sep 2025 02:21:08 GMT  
		Size: 4.7 MB (4675813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e782921a7e16320301d3e52b72374e2eb7ddc44b849e21feb8c234d16f78fe80`  
		Last Modified: Thu, 25 Sep 2025 02:21:09 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:53fb521ae05584264606185211fc7cb420181cab87c8aadc2e63a8215efde57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110087437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0da1f3181c9cc48b9d164d0dd3d42064625c41a43324cbd05736e7224aa051`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7751095df082bb36fbdf41936eb5e7f878571a8a846feeff96b113c6217e77f0`  
		Last Modified: Wed, 24 Sep 2025 20:41:58 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbac4123333e136ece841a309f3427512ade943728e2a04b2a02859c7d66a16`  
		Last Modified: Wed, 24 Sep 2025 20:42:02 GMT  
		Size: 38.1 MB (38130718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eab60e18f77b4310dd0b49fe505f24f7728a71ade85d0ea12ee7cac4c1fcdd1`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0920398efc022a62518752fa4dc4d662c2da979c0ae307c30d3987edcafa01d`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958e4e08bfcb68da732d4e039153d749641b857652d307b714249490beda9656`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:32395c47f606c1ba73e1a6d03ebe4e30a012f693a1c72338b80ecd6b93c0d00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4691865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f20924e4593145c03937f47325f42287a592111dfbdc5e9bf262cf6d40c20c`

```dockerfile
```

-	Layers:
	-	`sha256:11903a41af016385feeb7f926cc07ea645c0e44a0ec102e2a86234a64ecd9c09`  
		Last Modified: Thu, 25 Sep 2025 02:21:13 GMT  
		Size: 4.7 MB (4675271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:595c561ed9a5f1e1adbb47d688c7602bbb57a162be04d7c8e01376cd2835f183`  
		Last Modified: Thu, 25 Sep 2025 02:21:14 GMT  
		Size: 16.6 KB (16594 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-alpine`

```console
$ docker pull influxdb@sha256:a414cd63127794632745243d4bce4eebd7735cf550f742ef3a43458815b805ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:66d2329a46d68b73f4fe44a8ecc2e1a66c470cc0bf686b41d474b82dc4819099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46109705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b598749460a540b8467edfc5d27c9176d36136f5fbf77bdf7998e8cbaaf242b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf29fd72ecc1ce907ef679e6691bffbc6e2441190fac83926e70c94cf8d3c33a`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.2 MB (1217859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7298ddb7262ac5ecf38aa23565daab66ab05f51c43a14cf5094e40b4eba6cf7e`  
		Last Modified: Thu, 25 Sep 2025 01:11:28 GMT  
		Size: 41.3 MB (41251563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6d2c35dfc301a4fc344c4cc21bf0203d7b27545d02a185d3463c8c24eeb0d1`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c194518376314b2bd83490bbd01e606f06f23d11d0650ab68d302fbaa00e1b`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 997.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9b3690d762b0518bf4a2221226cc44c7680f52ff820f551e0f5ebd8edf34b5`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc091ce4196a6f6ef52a63c0824ad8f0f9661d03cfdaff16c8aa50d57dba59d`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:199e04d8292a4a75cb8a67a517df3c22c97564ba5d49254ff4db29914ee1f964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.9 KB (777909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238053bdd74f2651b16896d6bfbae7baf7a3fae84043e53a238d989bd8d682e0`

```dockerfile
```

-	Layers:
	-	`sha256:8bd1cb6b6e76e5c1e3b5cb4aef4fa7fd296fe013ec246031ba29d39d510a2cd1`  
		Last Modified: Thu, 25 Sep 2025 02:21:17 GMT  
		Size: 759.2 KB (759246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0bc5543f212c999f8c987694aead38c4b1205df87986ae131f6bdb3890d500`  
		Last Modified: Thu, 25 Sep 2025 02:21:18 GMT  
		Size: 18.7 KB (18663 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:81c4c76971e3becd6b38181251d3f78a774f235d75eaba3aefdf9ef55da5e5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43330814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf8f03c66704fa0bfde412001f104a8b686422ccb508c0d75ed7897528f9e0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb859780c099b20f6b1c19da90718ff441cf554fbf9fea5ce8bf88b2b342b27`  
		Last Modified: Wed, 24 Sep 2025 20:41:58 GMT  
		Size: 1.3 MB (1281995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4a2ea34cebba0e887e846c07a26b4b81dff4512d981cd60d18ee25c41dc54d`  
		Last Modified: Wed, 24 Sep 2025 20:42:01 GMT  
		Size: 38.1 MB (38059175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d1b64b38d090d2af54a47b8c3f497728a03364e5f5e3b03614f750e5d7d8fe`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7cf7191a46764e43da4fd29896b77aea2cd4b4f3addb1b78aa9665aa1906d0`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 994.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ca1e114aa3f7032cc94571dbd85f0e722edf9494f8d6690c156f853c443611`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f0ad996c925db03c1aa8d8f0151b4f5135db2b0bf874f32fb7b456b14a0571`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:7ba5e12a498af66276c54313990918a6091e9a100dc86622c647bd0f9994a860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.2 KB (777248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a49d7488c6e63d06c7801ebbda6b93b0e47fb09ec8e2a3423c4ef5f03ed09e7`

```dockerfile
```

-	Layers:
	-	`sha256:673a56ea96e4b0691dbec6d531ee2405386a405eae9fad2677ca9bac97882854`  
		Last Modified: Thu, 25 Sep 2025 02:21:21 GMT  
		Size: 758.5 KB (758475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0e2ef2cb88495c0a131cac294254ab280c5d8afb5b7a9754470a20026536ab0`  
		Last Modified: Thu, 25 Sep 2025 02:21:22 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-data`

```console
$ docker pull influxdb@sha256:d8c4c34372a99ce2e675ff3947e94037c1851e6cc8be5a57a575d804b35e83b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-data` - linux; amd64

```console
$ docker pull influxdb@sha256:1dcacb67df100503cbf1d690e634405636bab187c3411c0d8e1fb28ff1b6b6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114824093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d205e65066024ac15edd7559c9364fb002ad4f37dc5fca14be354915c0b0eeba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525dacd1718a9a4306658abd11b9a7874983c28e8a2e30026225bca0cec2c74f`  
		Last Modified: Thu, 25 Sep 2025 01:11:25 GMT  
		Size: 42.3 MB (42315710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0f30bd18a3ef0ad3bbc7b214a79107a3a2e478b8d7bbacdb35c89346794e3b`  
		Last Modified: Thu, 25 Sep 2025 01:11:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0591c5c9402800570b5222d1b35bb55ff2b165c28d3611b96d04e40a37d3d884`  
		Last Modified: Thu, 25 Sep 2025 01:11:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc091ce4196a6f6ef52a63c0824ad8f0f9661d03cfdaff16c8aa50d57dba59d`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:a0f5adb89f60c9b4213fd2e2d8df18a519549ea804d361c2bceeb41377311f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97e28a0b904717f5628514c176a7400334f84c84444c22b87c6e7f80db485db`

```dockerfile
```

-	Layers:
	-	`sha256:3c92aa4140d1e1ef715ba9e1005c4451882845f840da63bfc1ace5836ec4c018`  
		Last Modified: Thu, 25 Sep 2025 02:21:21 GMT  
		Size: 4.7 MB (4685451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea4330030334318f7d614ce79e4edc724b2f3b75f46e8e3b08f98911e71e3123`  
		Last Modified: Thu, 25 Sep 2025 02:21:22 GMT  
		Size: 13.8 KB (13822 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-data-alpine`

```console
$ docker pull influxdb@sha256:230248f4122b55660ea2f78e44d60d589b8cf6cb8ab48f5fa11355b2aa3437a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c6d9a496ea1ac3bfbb8fe7051352b68e5687cbce7cc4ade9e4dc92906d70d3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47111314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349217c040d7cb8d5ba819df95857de62d7b8c65fe537e562f9eedab6cd09781`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69f86ebefe9dfff24be9ab53cd975a2631738b7447af6789e1dff1ca3b2c27f`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.2 MB (1217842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d614cbfebd68939215609c41e791fa77b4faf9c0184838f6f2e088d147d90b`  
		Last Modified: Thu, 25 Sep 2025 01:11:20 GMT  
		Size: 42.3 MB (42254130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b27779e2d36c38b820659ca7fc3113c1733a2a5525df9062e31317c6e945791`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042f205ee4f2c54dd0fab79d5ff8ab7fc2d8b532b3b6bf65e1214a3ba864e2b6`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc48483cf9f08acfa785e7133e964bccc86be159a441243a8c2e7bf35f5c5a3`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cae64fd7f9afd9ae2714d996f632407d49177f7187e1ea8f0f0cfcc147b719ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **788.4 KB (788388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc8318dc7f4dd8e8855ad80626a177cb044360e5746e29e2d607ff65ac2aa6a`

```dockerfile
```

-	Layers:
	-	`sha256:a071aa26d75f72d4bd7f30c81a59364f35b5553a0d5e391470b451a6d0354062`  
		Last Modified: Thu, 25 Sep 2025 02:21:25 GMT  
		Size: 773.2 KB (773197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e9386bff0d6db73eee18d185455902b386dab3efc2240f66243aa380eba25a`  
		Last Modified: Thu, 25 Sep 2025 02:21:26 GMT  
		Size: 15.2 KB (15191 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-meta`

```console
$ docker pull influxdb@sha256:b4a18ca2506d6629ed097814309b393e33a026ac3f82cb901854fc2b8fd967bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:dc0bbc5ea6748757e54723a9b5b4ce145c57599d73bf86d3567a337d67a53250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91286168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd45c40e53c65286de17822b9851343ef1755fef293630119aa6de6148fd14a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80815c6fd7d7a52c20814c13cef8c36f4bb487b8375dd627f5dcf0ce5b9308c8`  
		Last Modified: Thu, 25 Sep 2025 01:11:11 GMT  
		Size: 18.8 MB (18778993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4f5d4f083ee73460a98f9568ab2ce0bbb89f3b0c2c246b8743471c9561fe93`  
		Last Modified: Thu, 25 Sep 2025 01:11:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e31010df7fb30794fe3614ffadd762a00456fc61ece5d2556bbbc0fa1252fc`  
		Last Modified: Thu, 25 Sep 2025 01:11:08 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:c1e318716cd76b6ddaa0a92e89b5af10892b4071a1e7a2df2e392bed3fe654a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4602950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f401843f67b2566ff0936e7fe3108a695abecb455b3aab1b8265f7cb26c3797c`

```dockerfile
```

-	Layers:
	-	`sha256:6a7c0705f078bd9566af2b64c6ec32e6b7be1705661371576bb13420c365ccac`  
		Last Modified: Thu, 25 Sep 2025 02:21:31 GMT  
		Size: 4.6 MB (4590614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b96dbac04e4531691f4d49dc6a3a95c908a88cd33ae596271f93ed53b160f7`  
		Last Modified: Thu, 25 Sep 2025 02:21:32 GMT  
		Size: 12.3 KB (12336 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-meta-alpine`

```console
$ docker pull influxdb@sha256:fb1c6ce882c6f76575bf00e884eb6a1cb48f015f6dced8852e0632304e0f5e18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:438d52e3d15ecb0301ecc4b86a960ee9bc6fce7f38f9d2e372347c8525563ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23578256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b60e5178733d55db673306b947c186ea7867ea6067cff2db7b2e658a86d9c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influxd-ctl'             'influxdb-*/usr/bin/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f49da720c3a823002c9dc61fb96fe6cbaef56f95b70e83f1717b0cbfe3625c2`  
		Last Modified: Thu, 25 Sep 2025 01:11:07 GMT  
		Size: 1.2 MB (1217796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b26514951c314740b0ec3a65e5c10800f94cd828599759c28c959a27cce08fc`  
		Last Modified: Thu, 25 Sep 2025 01:11:08 GMT  
		Size: 18.7 MB (18722325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a69a5b526bf15a075a5b6a8f416149db75a74b0e83960585a33600795990c9e`  
		Last Modified: Thu, 25 Sep 2025 01:11:07 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaf0d00f6e38d9ddf873ead6554c87a4c001319e00556ec54da121d35ad3db6`  
		Last Modified: Thu, 25 Sep 2025 01:11:07 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:66c0c255fb30f22da06e4e5eb91e6feab97a584430550d8c5fa3641c6e9adc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.7 KB (692723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c204ee4a35a8f1aa76d61d64fe38ae6354d2b8fc6deff8188661dddd18a645`

```dockerfile
```

-	Layers:
	-	`sha256:b6e4d83eeb239e60792a85b357d7d2758fca1759d804b3b06c1ca78d6b90f827`  
		Last Modified: Thu, 25 Sep 2025 02:21:34 GMT  
		Size: 679.1 KB (679146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d892543fbfacd30d46f77df1c4f2bad94927a6e55b406e2082cebc6a60b88c7d`  
		Last Modified: Thu, 25 Sep 2025 02:21:35 GMT  
		Size: 13.6 KB (13577 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:7cef9509aaad441529b985839e18abdf276813f0e96e53a4b588a8982ba1b22b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:99ec207e034a0030cfe9b324abd7d17c5359c30c00fe380e38bb343d32236757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf3d8c36b817ec2a3134909fa3ced93611ae30df9a9212fd88a827f6dc70cd3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV GOSU_VER=1.16
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f21742dbff9b844e8ebe7bc73fdd25b4246af656bc0a29c6b9f8d69a56d4e12`  
		Last Modified: Thu, 25 Sep 2025 01:12:23 GMT  
		Size: 9.8 MB (9796243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36fc49d49d1a27e5a8d04a999e6f56e7b499930c350fe0df2d2e7bc7802fb8e`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 6.2 MB (6156975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d232cb48b053d662eb2a0ebf0f93b556ad770c7455453ec0c7999233363ae04`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea323cfe236177f0122d70f051ffb9d262f532128b7df58448c8abab533a6fd`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 1.0 MB (1012030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eebc994e1765337ac74a0a9d063bfe6ba57130b07dfd0e6ccecb7d7ff17b683`  
		Last Modified: Thu, 25 Sep 2025 01:12:28 GMT  
		Size: 100.2 MB (100244537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489fccc0e03e220d305a6654112101c64052df1d23cd3f206f5f833d4035e2c7`  
		Last Modified: Thu, 25 Sep 2025 01:12:23 GMT  
		Size: 11.8 MB (11773804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8948b91899dae640e1f8ee6c01dfaddc356af1b0fd1d0c3b1aa5f8a49a1d7015`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04420871cdff010a378fbadfefb97c7fa29f919193a4246c646e7ae8b5da5bc2`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7058e6744694a1062c598527550938140a3a61c0a83b9628f8373f408e91d698`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:e2b41419d76750bb8d9fcbba2731a2c939acf772e283bd4cb02795d03a8785c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48557e802771f4374647ee6d591718afdd412df1e19f465f67413038f1cd1c62`

```dockerfile
```

-	Layers:
	-	`sha256:1d57937036d3daf271d4c03c34e7425d7d2d60a5261c2ff78249218a424f5ebe`  
		Last Modified: Thu, 25 Sep 2025 02:21:57 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8130e16a0cc378e5e9a85749da908ba586fac9377f75da9e5bf7d5bfd808266`  
		Last Modified: Thu, 25 Sep 2025 02:21:58 GMT  
		Size: 33.5 KB (33537 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:360dcee62c844c23a234bfafbfe5511a9eec36708ac018898417109abf442919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be31ac8b81e9cfd609c523de74012f65cb50e861e392ba63ba22aabd796f607f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV GOSU_VER=1.16
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb01127f4ecc7cec32d1038e47228414dc56b31af3bbe48fef16e87315ccbe2e`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 9.6 MB (9626297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3946c56889b4245bea086fd3932326e26ad874953fe751707350630acdae998e`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9e3f58b659a18c358e334cc15930a931b940051e6d5c5ea9c651490f58865d`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5242355409b896247ed91922f8f8eed4ff5cbf779a515539eda0d707bc28fd38`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cce3bcba21ff833984ada7e3fa4ecf3160c0b46f032bbcf082a0caa3d7fd09`  
		Last Modified: Wed, 24 Sep 2025 20:42:21 GMT  
		Size: 96.0 MB (96038999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0db4d928b52404e26b6f1c213333ab49fc4d1f2e17d01312187f82e96fb5478`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 11.1 MB (11099991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802ede4ca46ce31c894904679fe589cc47cb6a1623f99c04f2f0476135eb2fa8`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b64c4076b267fc9adfeab0eadbfabc70fd195b90720bfe6e74378fa0621d42c`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7864a9ac5c643bf554f8ba4d96a66ab30967e45048c19bbc695e08f70d2ba50e`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:740c7608085e12a989c31bb6765091b2e748e1ac2e1ad5b729683c9c7ed8445b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f4c48a7e65713d45172ae2f2cc1fe1409b4d8d33212de76f972c846d8c46bd`

```dockerfile
```

-	Layers:
	-	`sha256:6fd46fce2dd3e7092712a8481fd90a644582c32e5ba9ea39c77ecc42c7ff7511`  
		Last Modified: Thu, 25 Sep 2025 02:22:02 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b376a7e3f08be287cee166060598253dc80b41b60df84212e3b7b21d5ab60cb`  
		Last Modified: Thu, 25 Sep 2025 02:22:02 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:fa166d3bdf6beeecf57791b70e558f6ef54e1e6cea95fb7728b45314bc48543b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cff6f2ab47c82bede8226eaa115bb26a3c6b687ca6d1600c4daf951debdab495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81514718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e97594fdb74be0f41ef523f1d997467fd03327d8d08cfda4c4ac4e33bf5a76b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a8ae42cc4bbee908d14c07fc4ec8c8407af6310249f9dfeae0f8509bdc7af`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c7bfad06ee97b9a79123f8649a25c2c85621f43c09f683fc22058f5a07f5d6`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 9.8 MB (9819983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a34cab64443b962a114bd2a6beffb95756ba52160469829a5d45a76fcba800`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a8939940eb42b2ce365e0ace1c34d67dbdaf70d81621f34c5fca12f3bfd8f7`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda56c435bfb0f3172c6ba8994e754a3757983ee0517a7f6b2584a903a27e12e`  
		Last Modified: Thu, 25 Sep 2025 01:11:57 GMT  
		Size: 50.1 MB (50118442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5092574230696c38c9b6d5e80c3b0052a6775a347fc390fb3ddfbed0312b110b`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6964e799275484d75822451544c8b8aeb0525a898edf53d62dc5b2bea9ec4f23`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07acd36aa62e4aa31c3926c29dbc6d78b9952999a9f6d5a20d03ad2ac4ce55cd`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2256c74f4ebf0907ad02de26150d5f5f37dbd8fca3e5b1db457560709bcdc17`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:4cecdea6552df534fc6ff5b0baf01df080318ad872171cb76d8d681529a60c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 KB (941372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e5b13134ce9c59f59464dd153938abe2b1fb108f183574cf50f20c34593ab1`

```dockerfile
```

-	Layers:
	-	`sha256:24d2b9eb10c23f5c732a7e37c15a0f780289592f3ff141a1cf3aed71130b5200`  
		Last Modified: Thu, 25 Sep 2025 02:22:05 GMT  
		Size: 910.6 KB (910603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc19b40f79ef646496790610a3aa4aeb69ed7919b9a4f647f14c2cd431b643e`  
		Last Modified: Thu, 25 Sep 2025 02:22:06 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d76a12db18d7b6e85c3bf97b9627d2043eac00a226367a71789aa4f511b2e675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78685978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1ccd747e4a1c0cfefc72d84b8878fd0133be8c5235727262a387f7c717437b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bee215043e4b9c592d3270a4f9ca98f743ad5efe2f15d29853608a33f501e9e`  
		Last Modified: Wed, 24 Sep 2025 20:42:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd831899112efbf1818c7a1391b355b858f0978cd23d43c7301b385e94bb8fee`  
		Last Modified: Wed, 24 Sep 2025 20:42:10 GMT  
		Size: 9.8 MB (9783483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95fb2184026d4eaa8b66c5dd24e1704f9b8656617244f9830dd08887fcd1c0c`  
		Last Modified: Wed, 24 Sep 2025 20:42:10 GMT  
		Size: 5.8 MB (5790447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b6d057364a9b4e36e9823da94eaf8835e9bac3b077c62a40c181b00530cdfa`  
		Last Modified: Wed, 24 Sep 2025 20:42:09 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edba18fd6c1832982b6768f2002eb35d3cf6c674c66c3250319a5de66db7415f`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 48.0 MB (48017164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7edbd54c33d4091fc7334eb38238f440a45590e52b46baf71b46dd441a50ca`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3a4cfc59e5f76d849da88e7e676f8f42c75ea2fea9a6aa92ed3a2ea7a0b405`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7c6ec75ef0cf8c7cf00e47fc3b0650c76931084ae3b046ef3dfeb076c1f719`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92892ed38d0c82365147f5ff91c9b9018cf22b8a78c94d836c2c98259200b9e5`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:da75c82cd2a446f08e03c0f1f2436f8078f27140db4413a43c3f36b73ff7bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.8 KB (940817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82968150aefd76734cd63972f5c9bb47ad207190dc4e58e3b34ff0ce3e584987`

```dockerfile
```

-	Layers:
	-	`sha256:ac04216069aed10e6fcf7796fc4b9979609d5f75599ec854456b1cade370bf2b`  
		Last Modified: Thu, 25 Sep 2025 02:22:10 GMT  
		Size: 909.9 KB (909854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c9d7656a12cb47dd5db65e1dfe6517aa607a0480a92ae559be75c02b87fffd`  
		Last Modified: Thu, 25 Sep 2025 02:22:10 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:7cef9509aaad441529b985839e18abdf276813f0e96e53a4b588a8982ba1b22b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:99ec207e034a0030cfe9b324abd7d17c5359c30c00fe380e38bb343d32236757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf3d8c36b817ec2a3134909fa3ced93611ae30df9a9212fd88a827f6dc70cd3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV GOSU_VER=1.16
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f21742dbff9b844e8ebe7bc73fdd25b4246af656bc0a29c6b9f8d69a56d4e12`  
		Last Modified: Thu, 25 Sep 2025 01:12:23 GMT  
		Size: 9.8 MB (9796243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36fc49d49d1a27e5a8d04a999e6f56e7b499930c350fe0df2d2e7bc7802fb8e`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 6.2 MB (6156975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d232cb48b053d662eb2a0ebf0f93b556ad770c7455453ec0c7999233363ae04`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea323cfe236177f0122d70f051ffb9d262f532128b7df58448c8abab533a6fd`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 1.0 MB (1012030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eebc994e1765337ac74a0a9d063bfe6ba57130b07dfd0e6ccecb7d7ff17b683`  
		Last Modified: Thu, 25 Sep 2025 01:12:28 GMT  
		Size: 100.2 MB (100244537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489fccc0e03e220d305a6654112101c64052df1d23cd3f206f5f833d4035e2c7`  
		Last Modified: Thu, 25 Sep 2025 01:12:23 GMT  
		Size: 11.8 MB (11773804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8948b91899dae640e1f8ee6c01dfaddc356af1b0fd1d0c3b1aa5f8a49a1d7015`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04420871cdff010a378fbadfefb97c7fa29f919193a4246c646e7ae8b5da5bc2`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7058e6744694a1062c598527550938140a3a61c0a83b9628f8373f408e91d698`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:e2b41419d76750bb8d9fcbba2731a2c939acf772e283bd4cb02795d03a8785c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48557e802771f4374647ee6d591718afdd412df1e19f465f67413038f1cd1c62`

```dockerfile
```

-	Layers:
	-	`sha256:1d57937036d3daf271d4c03c34e7425d7d2d60a5261c2ff78249218a424f5ebe`  
		Last Modified: Thu, 25 Sep 2025 02:21:57 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8130e16a0cc378e5e9a85749da908ba586fac9377f75da9e5bf7d5bfd808266`  
		Last Modified: Thu, 25 Sep 2025 02:21:58 GMT  
		Size: 33.5 KB (33537 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:360dcee62c844c23a234bfafbfe5511a9eec36708ac018898417109abf442919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be31ac8b81e9cfd609c523de74012f65cb50e861e392ba63ba22aabd796f607f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV GOSU_VER=1.16
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb01127f4ecc7cec32d1038e47228414dc56b31af3bbe48fef16e87315ccbe2e`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 9.6 MB (9626297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3946c56889b4245bea086fd3932326e26ad874953fe751707350630acdae998e`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9e3f58b659a18c358e334cc15930a931b940051e6d5c5ea9c651490f58865d`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5242355409b896247ed91922f8f8eed4ff5cbf779a515539eda0d707bc28fd38`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cce3bcba21ff833984ada7e3fa4ecf3160c0b46f032bbcf082a0caa3d7fd09`  
		Last Modified: Wed, 24 Sep 2025 20:42:21 GMT  
		Size: 96.0 MB (96038999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0db4d928b52404e26b6f1c213333ab49fc4d1f2e17d01312187f82e96fb5478`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 11.1 MB (11099991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802ede4ca46ce31c894904679fe589cc47cb6a1623f99c04f2f0476135eb2fa8`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b64c4076b267fc9adfeab0eadbfabc70fd195b90720bfe6e74378fa0621d42c`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7864a9ac5c643bf554f8ba4d96a66ab30967e45048c19bbc695e08f70d2ba50e`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:740c7608085e12a989c31bb6765091b2e748e1ac2e1ad5b729683c9c7ed8445b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f4c48a7e65713d45172ae2f2cc1fe1409b4d8d33212de76f972c846d8c46bd`

```dockerfile
```

-	Layers:
	-	`sha256:6fd46fce2dd3e7092712a8481fd90a644582c32e5ba9ea39c77ecc42c7ff7511`  
		Last Modified: Thu, 25 Sep 2025 02:22:02 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b376a7e3f08be287cee166060598253dc80b41b60df84212e3b7b21d5ab60cb`  
		Last Modified: Thu, 25 Sep 2025 02:22:02 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:fa166d3bdf6beeecf57791b70e558f6ef54e1e6cea95fb7728b45314bc48543b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cff6f2ab47c82bede8226eaa115bb26a3c6b687ca6d1600c4daf951debdab495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81514718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e97594fdb74be0f41ef523f1d997467fd03327d8d08cfda4c4ac4e33bf5a76b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a8ae42cc4bbee908d14c07fc4ec8c8407af6310249f9dfeae0f8509bdc7af`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c7bfad06ee97b9a79123f8649a25c2c85621f43c09f683fc22058f5a07f5d6`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 9.8 MB (9819983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a34cab64443b962a114bd2a6beffb95756ba52160469829a5d45a76fcba800`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a8939940eb42b2ce365e0ace1c34d67dbdaf70d81621f34c5fca12f3bfd8f7`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda56c435bfb0f3172c6ba8994e754a3757983ee0517a7f6b2584a903a27e12e`  
		Last Modified: Thu, 25 Sep 2025 01:11:57 GMT  
		Size: 50.1 MB (50118442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5092574230696c38c9b6d5e80c3b0052a6775a347fc390fb3ddfbed0312b110b`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6964e799275484d75822451544c8b8aeb0525a898edf53d62dc5b2bea9ec4f23`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07acd36aa62e4aa31c3926c29dbc6d78b9952999a9f6d5a20d03ad2ac4ce55cd`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2256c74f4ebf0907ad02de26150d5f5f37dbd8fca3e5b1db457560709bcdc17`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:4cecdea6552df534fc6ff5b0baf01df080318ad872171cb76d8d681529a60c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 KB (941372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e5b13134ce9c59f59464dd153938abe2b1fb108f183574cf50f20c34593ab1`

```dockerfile
```

-	Layers:
	-	`sha256:24d2b9eb10c23f5c732a7e37c15a0f780289592f3ff141a1cf3aed71130b5200`  
		Last Modified: Thu, 25 Sep 2025 02:22:05 GMT  
		Size: 910.6 KB (910603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc19b40f79ef646496790610a3aa4aeb69ed7919b9a4f647f14c2cd431b643e`  
		Last Modified: Thu, 25 Sep 2025 02:22:06 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d76a12db18d7b6e85c3bf97b9627d2043eac00a226367a71789aa4f511b2e675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78685978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1ccd747e4a1c0cfefc72d84b8878fd0133be8c5235727262a387f7c717437b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bee215043e4b9c592d3270a4f9ca98f743ad5efe2f15d29853608a33f501e9e`  
		Last Modified: Wed, 24 Sep 2025 20:42:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd831899112efbf1818c7a1391b355b858f0978cd23d43c7301b385e94bb8fee`  
		Last Modified: Wed, 24 Sep 2025 20:42:10 GMT  
		Size: 9.8 MB (9783483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95fb2184026d4eaa8b66c5dd24e1704f9b8656617244f9830dd08887fcd1c0c`  
		Last Modified: Wed, 24 Sep 2025 20:42:10 GMT  
		Size: 5.8 MB (5790447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b6d057364a9b4e36e9823da94eaf8835e9bac3b077c62a40c181b00530cdfa`  
		Last Modified: Wed, 24 Sep 2025 20:42:09 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edba18fd6c1832982b6768f2002eb35d3cf6c674c66c3250319a5de66db7415f`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 48.0 MB (48017164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7edbd54c33d4091fc7334eb38238f440a45590e52b46baf71b46dd441a50ca`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3a4cfc59e5f76d849da88e7e676f8f42c75ea2fea9a6aa92ed3a2ea7a0b405`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7c6ec75ef0cf8c7cf00e47fc3b0650c76931084ae3b046ef3dfeb076c1f719`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92892ed38d0c82365147f5ff91c9b9018cf22b8a78c94d836c2c98259200b9e5`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:da75c82cd2a446f08e03c0f1f2436f8078f27140db4413a43c3f36b73ff7bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.8 KB (940817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82968150aefd76734cd63972f5c9bb47ad207190dc4e58e3b34ff0ce3e584987`

```dockerfile
```

-	Layers:
	-	`sha256:ac04216069aed10e6fcf7796fc4b9979609d5f75599ec854456b1cade370bf2b`  
		Last Modified: Thu, 25 Sep 2025 02:22:10 GMT  
		Size: 909.9 KB (909854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c9d7656a12cb47dd5db65e1dfe6517aa607a0480a92ae559be75c02b87fffd`  
		Last Modified: Thu, 25 Sep 2025 02:22:10 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12`

```console
$ docker pull influxdb@sha256:7cef9509aaad441529b985839e18abdf276813f0e96e53a4b588a8982ba1b22b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:99ec207e034a0030cfe9b324abd7d17c5359c30c00fe380e38bb343d32236757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf3d8c36b817ec2a3134909fa3ced93611ae30df9a9212fd88a827f6dc70cd3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV GOSU_VER=1.16
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f21742dbff9b844e8ebe7bc73fdd25b4246af656bc0a29c6b9f8d69a56d4e12`  
		Last Modified: Thu, 25 Sep 2025 01:12:23 GMT  
		Size: 9.8 MB (9796243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36fc49d49d1a27e5a8d04a999e6f56e7b499930c350fe0df2d2e7bc7802fb8e`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 6.2 MB (6156975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d232cb48b053d662eb2a0ebf0f93b556ad770c7455453ec0c7999233363ae04`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea323cfe236177f0122d70f051ffb9d262f532128b7df58448c8abab533a6fd`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 1.0 MB (1012030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eebc994e1765337ac74a0a9d063bfe6ba57130b07dfd0e6ccecb7d7ff17b683`  
		Last Modified: Thu, 25 Sep 2025 01:12:28 GMT  
		Size: 100.2 MB (100244537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489fccc0e03e220d305a6654112101c64052df1d23cd3f206f5f833d4035e2c7`  
		Last Modified: Thu, 25 Sep 2025 01:12:23 GMT  
		Size: 11.8 MB (11773804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8948b91899dae640e1f8ee6c01dfaddc356af1b0fd1d0c3b1aa5f8a49a1d7015`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04420871cdff010a378fbadfefb97c7fa29f919193a4246c646e7ae8b5da5bc2`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7058e6744694a1062c598527550938140a3a61c0a83b9628f8373f408e91d698`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:e2b41419d76750bb8d9fcbba2731a2c939acf772e283bd4cb02795d03a8785c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48557e802771f4374647ee6d591718afdd412df1e19f465f67413038f1cd1c62`

```dockerfile
```

-	Layers:
	-	`sha256:1d57937036d3daf271d4c03c34e7425d7d2d60a5261c2ff78249218a424f5ebe`  
		Last Modified: Thu, 25 Sep 2025 02:21:57 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8130e16a0cc378e5e9a85749da908ba586fac9377f75da9e5bf7d5bfd808266`  
		Last Modified: Thu, 25 Sep 2025 02:21:58 GMT  
		Size: 33.5 KB (33537 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:360dcee62c844c23a234bfafbfe5511a9eec36708ac018898417109abf442919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be31ac8b81e9cfd609c523de74012f65cb50e861e392ba63ba22aabd796f607f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV GOSU_VER=1.16
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb01127f4ecc7cec32d1038e47228414dc56b31af3bbe48fef16e87315ccbe2e`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 9.6 MB (9626297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3946c56889b4245bea086fd3932326e26ad874953fe751707350630acdae998e`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9e3f58b659a18c358e334cc15930a931b940051e6d5c5ea9c651490f58865d`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5242355409b896247ed91922f8f8eed4ff5cbf779a515539eda0d707bc28fd38`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cce3bcba21ff833984ada7e3fa4ecf3160c0b46f032bbcf082a0caa3d7fd09`  
		Last Modified: Wed, 24 Sep 2025 20:42:21 GMT  
		Size: 96.0 MB (96038999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0db4d928b52404e26b6f1c213333ab49fc4d1f2e17d01312187f82e96fb5478`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 11.1 MB (11099991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802ede4ca46ce31c894904679fe589cc47cb6a1623f99c04f2f0476135eb2fa8`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b64c4076b267fc9adfeab0eadbfabc70fd195b90720bfe6e74378fa0621d42c`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7864a9ac5c643bf554f8ba4d96a66ab30967e45048c19bbc695e08f70d2ba50e`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:740c7608085e12a989c31bb6765091b2e748e1ac2e1ad5b729683c9c7ed8445b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f4c48a7e65713d45172ae2f2cc1fe1409b4d8d33212de76f972c846d8c46bd`

```dockerfile
```

-	Layers:
	-	`sha256:6fd46fce2dd3e7092712a8481fd90a644582c32e5ba9ea39c77ecc42c7ff7511`  
		Last Modified: Thu, 25 Sep 2025 02:22:02 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b376a7e3f08be287cee166060598253dc80b41b60df84212e3b7b21d5ab60cb`  
		Last Modified: Thu, 25 Sep 2025 02:22:02 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12-alpine`

```console
$ docker pull influxdb@sha256:fa166d3bdf6beeecf57791b70e558f6ef54e1e6cea95fb7728b45314bc48543b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cff6f2ab47c82bede8226eaa115bb26a3c6b687ca6d1600c4daf951debdab495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81514718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e97594fdb74be0f41ef523f1d997467fd03327d8d08cfda4c4ac4e33bf5a76b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a8ae42cc4bbee908d14c07fc4ec8c8407af6310249f9dfeae0f8509bdc7af`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c7bfad06ee97b9a79123f8649a25c2c85621f43c09f683fc22058f5a07f5d6`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 9.8 MB (9819983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a34cab64443b962a114bd2a6beffb95756ba52160469829a5d45a76fcba800`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a8939940eb42b2ce365e0ace1c34d67dbdaf70d81621f34c5fca12f3bfd8f7`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda56c435bfb0f3172c6ba8994e754a3757983ee0517a7f6b2584a903a27e12e`  
		Last Modified: Thu, 25 Sep 2025 01:11:57 GMT  
		Size: 50.1 MB (50118442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5092574230696c38c9b6d5e80c3b0052a6775a347fc390fb3ddfbed0312b110b`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6964e799275484d75822451544c8b8aeb0525a898edf53d62dc5b2bea9ec4f23`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07acd36aa62e4aa31c3926c29dbc6d78b9952999a9f6d5a20d03ad2ac4ce55cd`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2256c74f4ebf0907ad02de26150d5f5f37dbd8fca3e5b1db457560709bcdc17`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:4cecdea6552df534fc6ff5b0baf01df080318ad872171cb76d8d681529a60c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 KB (941372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e5b13134ce9c59f59464dd153938abe2b1fb108f183574cf50f20c34593ab1`

```dockerfile
```

-	Layers:
	-	`sha256:24d2b9eb10c23f5c732a7e37c15a0f780289592f3ff141a1cf3aed71130b5200`  
		Last Modified: Thu, 25 Sep 2025 02:22:05 GMT  
		Size: 910.6 KB (910603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc19b40f79ef646496790610a3aa4aeb69ed7919b9a4f647f14c2cd431b643e`  
		Last Modified: Thu, 25 Sep 2025 02:22:06 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d76a12db18d7b6e85c3bf97b9627d2043eac00a226367a71789aa4f511b2e675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78685978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1ccd747e4a1c0cfefc72d84b8878fd0133be8c5235727262a387f7c717437b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bee215043e4b9c592d3270a4f9ca98f743ad5efe2f15d29853608a33f501e9e`  
		Last Modified: Wed, 24 Sep 2025 20:42:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd831899112efbf1818c7a1391b355b858f0978cd23d43c7301b385e94bb8fee`  
		Last Modified: Wed, 24 Sep 2025 20:42:10 GMT  
		Size: 9.8 MB (9783483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95fb2184026d4eaa8b66c5dd24e1704f9b8656617244f9830dd08887fcd1c0c`  
		Last Modified: Wed, 24 Sep 2025 20:42:10 GMT  
		Size: 5.8 MB (5790447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b6d057364a9b4e36e9823da94eaf8835e9bac3b077c62a40c181b00530cdfa`  
		Last Modified: Wed, 24 Sep 2025 20:42:09 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edba18fd6c1832982b6768f2002eb35d3cf6c674c66c3250319a5de66db7415f`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 48.0 MB (48017164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7edbd54c33d4091fc7334eb38238f440a45590e52b46baf71b46dd441a50ca`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3a4cfc59e5f76d849da88e7e676f8f42c75ea2fea9a6aa92ed3a2ea7a0b405`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7c6ec75ef0cf8c7cf00e47fc3b0650c76931084ae3b046ef3dfeb076c1f719`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92892ed38d0c82365147f5ff91c9b9018cf22b8a78c94d836c2c98259200b9e5`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:da75c82cd2a446f08e03c0f1f2436f8078f27140db4413a43c3f36b73ff7bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.8 KB (940817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82968150aefd76734cd63972f5c9bb47ad207190dc4e58e3b34ff0ce3e584987`

```dockerfile
```

-	Layers:
	-	`sha256:ac04216069aed10e6fcf7796fc4b9979609d5f75599ec854456b1cade370bf2b`  
		Last Modified: Thu, 25 Sep 2025 02:22:10 GMT  
		Size: 909.9 KB (909854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c9d7656a12cb47dd5db65e1dfe6517aa607a0480a92ae559be75c02b87fffd`  
		Last Modified: Thu, 25 Sep 2025 02:22:10 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:61f49b027eb537eca25e44e83fb375e4b34c9afeb4643085785b6045e33db3e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:86c47dff61aa11be714432ed9dd906192818ffc86fe509c040efd5233b2d0ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115829644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433e4ec2e156f21e5e4d526b8b81805e3c8c64d8f91cec051e57c9030be91c20`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17baf28e6051bd7a25fe013c9c08c6cd7f73bcaa9c734400e0f1f0d284581627`  
		Last Modified: Thu, 25 Sep 2025 01:12:01 GMT  
		Size: 6.7 MB (6665987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b81b90ea3abb8282b95fae868e842fb28507936752797da04f7121d8514f58`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e206217edc4c1be0defb1ba44d2cb562cacb37ea45ea4b6f591350c8f7d42224`  
		Last Modified: Thu, 25 Sep 2025 01:12:11 GMT  
		Size: 79.4 MB (79436081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7779b24984be148a6f6a4dd2751a96927a0ae8eaf063915fc37d68f529f6da45`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd86818b22c1efec0a5c8198f388a6305686db0ae137d779ce3ee90c35a5143`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:72406575b4d8334fa8816af7b7d5622490e873d79077160dc83500043610c83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a111a20e3b57099d9bf669d793746ddc9921c8fb00d81bdb2a02ac6606ea988`

```dockerfile
```

-	Layers:
	-	`sha256:5f9f61f4725c0fc06eda3221e7849e2f1459b46af20799713bf4274d7d5bae06`  
		Last Modified: Thu, 25 Sep 2025 02:22:21 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c72da19de4878ba2801664b77c127422b6571127a04cfb5c4675ff11516d41b`  
		Last Modified: Thu, 25 Sep 2025 02:22:22 GMT  
		Size: 17.6 KB (17591 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:758c1a038d65b404028e569cc9284e00b1c513b50a581a88f9ac16c3a858b331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106588999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452fa4782937755e004b25d81cd21387ee068907e9b99348c35664eefe66b1ae`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76772dfef93d9692ae29670bd3c35ef1b32af43be390336ce02735ca2e6ed34c`  
		Last Modified: Wed, 24 Sep 2025 20:42:13 GMT  
		Size: 6.7 MB (6676456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dd47aad406061c9bef9141140aaa9b6759d82a1c241eb78bfd0557b0bbaf3`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0ca37718bb135be92a784b085b083c56d6441e024e170147d526ce62dbeb13`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 71.0 MB (71047103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf300e1edc90912abd0f245569a70a5e38003d97ee7cc3df20da44178e19697b`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdda608d41ce88b20843112b0fccf8213f3a4cd48021557a305fe7ed9cbe3982`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:7ff5fe04ac92f2cba5c11a9d0ff4aefd16d2e155c4f6aa52979df3849d07098b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae50fbce074dd9457296eabeb258782360b24d7a45b4ccf9881dd8730f19169d`

```dockerfile
```

-	Layers:
	-	`sha256:16a8560fea8f78d8906afef5d7056ce77ddd281f67ae502ad05fe1f856f3bb5f`  
		Last Modified: Thu, 25 Sep 2025 02:22:25 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c8c699c2ee5bfb443845220e3923cb29f00e1999aaa9b529a9909d9725ca59`  
		Last Modified: Thu, 25 Sep 2025 02:22:26 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:fee1fd937f122c29450b5371ad999918de8ea60674c4ebd0b13e1e8253ce0f49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:8e8b0efaee36e18121ab7dc869fe3ee0abd1e15fbcde242c7b9f67c91e194d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121191058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc922de6f2723e8b9d5e0f6d8ac1acf23c76c9d9ca870097495dcbb248d5904`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d2b65053f412e646e84b824154bbe7dfa5e894af0253d642dd08eefcac40b0`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 6.7 MB (6665962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a974fc6c3be5853d851c4367678b3169e8bfc40e4136ec075f865ab903d2c6f`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deed8451ed99c98ccf31f9d5a56ac45437e7654f0b692b232ced6ea304183de1`  
		Last Modified: Thu, 25 Sep 2025 01:12:05 GMT  
		Size: 84.8 MB (84797518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abf28c19a8e2f63583616a1371baac7224ce0aa8039aefdbffcc14943f2ba12`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbcad217e989b316b8d5390328e498a1c7a67c7288799a96eea414060a54ea0`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:caf5e328dec6182bcb6a665df4ea084f9b6cea24fc26642b4d3d44f9225fb153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c5bb899fbf546577b5574ac6892f51c5329bf86779b69e40d94337327ad702`

```dockerfile
```

-	Layers:
	-	`sha256:53749ce6fb588cb7c4356dfb8371a918c17514d4ee9d88e47f92aec9beafdff5`  
		Last Modified: Thu, 25 Sep 2025 02:22:28 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef91f4467414786cdf25738378986deb0f9d7405fc99ff64ebc67cbf6d0455a`  
		Last Modified: Thu, 25 Sep 2025 02:22:29 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:49b06572ed51033ab384673ac640e7efb021dc7ea64244077c0eaece0ac7e4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111864713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bff344b48f080250935ce5d2295f18d545a3573179f7e245805604e9439b16`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63986cf6045810298066b4a7dd264d5d2c4422ffbf792a0414c4a3e642d30233`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 6.7 MB (6676493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d79724c215b55fae9017081e43d63d95ab2d5a85837f4314a4a92798e224e7`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fe097ce79f895e72472cdda7d81b7899b9bdc0d6456fb32b9e8642bda053f8`  
		Last Modified: Wed, 24 Sep 2025 20:42:22 GMT  
		Size: 76.3 MB (76322772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d19e7c3caecb655f5bb0efae2e98421f664d7dab14dab4a26f7944a1978869`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8ea903490ced720b738540ced6dcb212a180c4737fa8ff6b79455d3ff80e52`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:d79dee4273d7b3f5e8d2bd0c0217b54004298bfb1f00b3547b4a00be30077962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee20f57b35fecbed61eb6d90c344087dcf6df70773eae21e59ec4c1195378f6f`

```dockerfile
```

-	Layers:
	-	`sha256:38671e81d3c25beb088deb3fb376c7077da8de731cf5336e28ca1d665461228f`  
		Last Modified: Thu, 25 Sep 2025 02:22:33 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b53831b7bc512d53a7b7be3c225fa3602fcb7e1e9f344bd1e5b920d4380b1d`  
		Last Modified: Thu, 25 Sep 2025 02:22:34 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.4-core`

```console
$ docker pull influxdb@sha256:61f49b027eb537eca25e44e83fb375e4b34c9afeb4643085785b6045e33db3e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.4-core` - linux; amd64

```console
$ docker pull influxdb@sha256:86c47dff61aa11be714432ed9dd906192818ffc86fe509c040efd5233b2d0ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115829644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433e4ec2e156f21e5e4d526b8b81805e3c8c64d8f91cec051e57c9030be91c20`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17baf28e6051bd7a25fe013c9c08c6cd7f73bcaa9c734400e0f1f0d284581627`  
		Last Modified: Thu, 25 Sep 2025 01:12:01 GMT  
		Size: 6.7 MB (6665987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b81b90ea3abb8282b95fae868e842fb28507936752797da04f7121d8514f58`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e206217edc4c1be0defb1ba44d2cb562cacb37ea45ea4b6f591350c8f7d42224`  
		Last Modified: Thu, 25 Sep 2025 01:12:11 GMT  
		Size: 79.4 MB (79436081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7779b24984be148a6f6a4dd2751a96927a0ae8eaf063915fc37d68f529f6da45`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd86818b22c1efec0a5c8198f388a6305686db0ae137d779ce3ee90c35a5143`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:72406575b4d8334fa8816af7b7d5622490e873d79077160dc83500043610c83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a111a20e3b57099d9bf669d793746ddc9921c8fb00d81bdb2a02ac6606ea988`

```dockerfile
```

-	Layers:
	-	`sha256:5f9f61f4725c0fc06eda3221e7849e2f1459b46af20799713bf4274d7d5bae06`  
		Last Modified: Thu, 25 Sep 2025 02:22:21 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c72da19de4878ba2801664b77c127422b6571127a04cfb5c4675ff11516d41b`  
		Last Modified: Thu, 25 Sep 2025 02:22:22 GMT  
		Size: 17.6 KB (17591 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.4-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:758c1a038d65b404028e569cc9284e00b1c513b50a581a88f9ac16c3a858b331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106588999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452fa4782937755e004b25d81cd21387ee068907e9b99348c35664eefe66b1ae`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76772dfef93d9692ae29670bd3c35ef1b32af43be390336ce02735ca2e6ed34c`  
		Last Modified: Wed, 24 Sep 2025 20:42:13 GMT  
		Size: 6.7 MB (6676456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dd47aad406061c9bef9141140aaa9b6759d82a1c241eb78bfd0557b0bbaf3`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0ca37718bb135be92a784b085b083c56d6441e024e170147d526ce62dbeb13`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 71.0 MB (71047103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf300e1edc90912abd0f245569a70a5e38003d97ee7cc3df20da44178e19697b`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdda608d41ce88b20843112b0fccf8213f3a4cd48021557a305fe7ed9cbe3982`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:7ff5fe04ac92f2cba5c11a9d0ff4aefd16d2e155c4f6aa52979df3849d07098b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae50fbce074dd9457296eabeb258782360b24d7a45b4ccf9881dd8730f19169d`

```dockerfile
```

-	Layers:
	-	`sha256:16a8560fea8f78d8906afef5d7056ce77ddd281f67ae502ad05fe1f856f3bb5f`  
		Last Modified: Thu, 25 Sep 2025 02:22:25 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c8c699c2ee5bfb443845220e3923cb29f00e1999aaa9b529a9909d9725ca59`  
		Last Modified: Thu, 25 Sep 2025 02:22:26 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.4-enterprise`

```console
$ docker pull influxdb@sha256:fee1fd937f122c29450b5371ad999918de8ea60674c4ebd0b13e1e8253ce0f49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.4-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:8e8b0efaee36e18121ab7dc869fe3ee0abd1e15fbcde242c7b9f67c91e194d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121191058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc922de6f2723e8b9d5e0f6d8ac1acf23c76c9d9ca870097495dcbb248d5904`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d2b65053f412e646e84b824154bbe7dfa5e894af0253d642dd08eefcac40b0`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 6.7 MB (6665962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a974fc6c3be5853d851c4367678b3169e8bfc40e4136ec075f865ab903d2c6f`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deed8451ed99c98ccf31f9d5a56ac45437e7654f0b692b232ced6ea304183de1`  
		Last Modified: Thu, 25 Sep 2025 01:12:05 GMT  
		Size: 84.8 MB (84797518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abf28c19a8e2f63583616a1371baac7224ce0aa8039aefdbffcc14943f2ba12`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbcad217e989b316b8d5390328e498a1c7a67c7288799a96eea414060a54ea0`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:caf5e328dec6182bcb6a665df4ea084f9b6cea24fc26642b4d3d44f9225fb153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c5bb899fbf546577b5574ac6892f51c5329bf86779b69e40d94337327ad702`

```dockerfile
```

-	Layers:
	-	`sha256:53749ce6fb588cb7c4356dfb8371a918c17514d4ee9d88e47f92aec9beafdff5`  
		Last Modified: Thu, 25 Sep 2025 02:22:28 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef91f4467414786cdf25738378986deb0f9d7405fc99ff64ebc67cbf6d0455a`  
		Last Modified: Thu, 25 Sep 2025 02:22:29 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:49b06572ed51033ab384673ac640e7efb021dc7ea64244077c0eaece0ac7e4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111864713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bff344b48f080250935ce5d2295f18d545a3573179f7e245805604e9439b16`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63986cf6045810298066b4a7dd264d5d2c4422ffbf792a0414c4a3e642d30233`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 6.7 MB (6676493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d79724c215b55fae9017081e43d63d95ab2d5a85837f4314a4a92798e224e7`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fe097ce79f895e72472cdda7d81b7899b9bdc0d6456fb32b9e8642bda053f8`  
		Last Modified: Wed, 24 Sep 2025 20:42:22 GMT  
		Size: 76.3 MB (76322772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d19e7c3caecb655f5bb0efae2e98421f664d7dab14dab4a26f7944a1978869`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8ea903490ced720b738540ced6dcb212a180c4737fa8ff6b79455d3ff80e52`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:d79dee4273d7b3f5e8d2bd0c0217b54004298bfb1f00b3547b4a00be30077962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee20f57b35fecbed61eb6d90c344087dcf6df70773eae21e59ec4c1195378f6f`

```dockerfile
```

-	Layers:
	-	`sha256:38671e81d3c25beb088deb3fb376c7077da8de731cf5336e28ca1d665461228f`  
		Last Modified: Thu, 25 Sep 2025 02:22:33 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b53831b7bc512d53a7b7be3c225fa3602fcb7e1e9f344bd1e5b920d4380b1d`  
		Last Modified: Thu, 25 Sep 2025 02:22:34 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.4.2-core`

```console
$ docker pull influxdb@sha256:61f49b027eb537eca25e44e83fb375e4b34c9afeb4643085785b6045e33db3e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.4.2-core` - linux; amd64

```console
$ docker pull influxdb@sha256:86c47dff61aa11be714432ed9dd906192818ffc86fe509c040efd5233b2d0ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115829644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433e4ec2e156f21e5e4d526b8b81805e3c8c64d8f91cec051e57c9030be91c20`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17baf28e6051bd7a25fe013c9c08c6cd7f73bcaa9c734400e0f1f0d284581627`  
		Last Modified: Thu, 25 Sep 2025 01:12:01 GMT  
		Size: 6.7 MB (6665987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b81b90ea3abb8282b95fae868e842fb28507936752797da04f7121d8514f58`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e206217edc4c1be0defb1ba44d2cb562cacb37ea45ea4b6f591350c8f7d42224`  
		Last Modified: Thu, 25 Sep 2025 01:12:11 GMT  
		Size: 79.4 MB (79436081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7779b24984be148a6f6a4dd2751a96927a0ae8eaf063915fc37d68f529f6da45`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd86818b22c1efec0a5c8198f388a6305686db0ae137d779ce3ee90c35a5143`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4.2-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:72406575b4d8334fa8816af7b7d5622490e873d79077160dc83500043610c83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a111a20e3b57099d9bf669d793746ddc9921c8fb00d81bdb2a02ac6606ea988`

```dockerfile
```

-	Layers:
	-	`sha256:5f9f61f4725c0fc06eda3221e7849e2f1459b46af20799713bf4274d7d5bae06`  
		Last Modified: Thu, 25 Sep 2025 02:22:21 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c72da19de4878ba2801664b77c127422b6571127a04cfb5c4675ff11516d41b`  
		Last Modified: Thu, 25 Sep 2025 02:22:22 GMT  
		Size: 17.6 KB (17591 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.4.2-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:758c1a038d65b404028e569cc9284e00b1c513b50a581a88f9ac16c3a858b331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106588999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452fa4782937755e004b25d81cd21387ee068907e9b99348c35664eefe66b1ae`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76772dfef93d9692ae29670bd3c35ef1b32af43be390336ce02735ca2e6ed34c`  
		Last Modified: Wed, 24 Sep 2025 20:42:13 GMT  
		Size: 6.7 MB (6676456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dd47aad406061c9bef9141140aaa9b6759d82a1c241eb78bfd0557b0bbaf3`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0ca37718bb135be92a784b085b083c56d6441e024e170147d526ce62dbeb13`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 71.0 MB (71047103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf300e1edc90912abd0f245569a70a5e38003d97ee7cc3df20da44178e19697b`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdda608d41ce88b20843112b0fccf8213f3a4cd48021557a305fe7ed9cbe3982`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4.2-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:7ff5fe04ac92f2cba5c11a9d0ff4aefd16d2e155c4f6aa52979df3849d07098b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae50fbce074dd9457296eabeb258782360b24d7a45b4ccf9881dd8730f19169d`

```dockerfile
```

-	Layers:
	-	`sha256:16a8560fea8f78d8906afef5d7056ce77ddd281f67ae502ad05fe1f856f3bb5f`  
		Last Modified: Thu, 25 Sep 2025 02:22:25 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c8c699c2ee5bfb443845220e3923cb29f00e1999aaa9b529a9909d9725ca59`  
		Last Modified: Thu, 25 Sep 2025 02:22:26 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.4.2-enterprise`

```console
$ docker pull influxdb@sha256:fee1fd937f122c29450b5371ad999918de8ea60674c4ebd0b13e1e8253ce0f49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.4.2-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:8e8b0efaee36e18121ab7dc869fe3ee0abd1e15fbcde242c7b9f67c91e194d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121191058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc922de6f2723e8b9d5e0f6d8ac1acf23c76c9d9ca870097495dcbb248d5904`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d2b65053f412e646e84b824154bbe7dfa5e894af0253d642dd08eefcac40b0`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 6.7 MB (6665962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a974fc6c3be5853d851c4367678b3169e8bfc40e4136ec075f865ab903d2c6f`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deed8451ed99c98ccf31f9d5a56ac45437e7654f0b692b232ced6ea304183de1`  
		Last Modified: Thu, 25 Sep 2025 01:12:05 GMT  
		Size: 84.8 MB (84797518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abf28c19a8e2f63583616a1371baac7224ce0aa8039aefdbffcc14943f2ba12`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbcad217e989b316b8d5390328e498a1c7a67c7288799a96eea414060a54ea0`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4.2-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:caf5e328dec6182bcb6a665df4ea084f9b6cea24fc26642b4d3d44f9225fb153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c5bb899fbf546577b5574ac6892f51c5329bf86779b69e40d94337327ad702`

```dockerfile
```

-	Layers:
	-	`sha256:53749ce6fb588cb7c4356dfb8371a918c17514d4ee9d88e47f92aec9beafdff5`  
		Last Modified: Thu, 25 Sep 2025 02:22:28 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef91f4467414786cdf25738378986deb0f9d7405fc99ff64ebc67cbf6d0455a`  
		Last Modified: Thu, 25 Sep 2025 02:22:29 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.4.2-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:49b06572ed51033ab384673ac640e7efb021dc7ea64244077c0eaece0ac7e4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111864713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bff344b48f080250935ce5d2295f18d545a3573179f7e245805604e9439b16`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63986cf6045810298066b4a7dd264d5d2c4422ffbf792a0414c4a3e642d30233`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 6.7 MB (6676493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d79724c215b55fae9017081e43d63d95ab2d5a85837f4314a4a92798e224e7`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fe097ce79f895e72472cdda7d81b7899b9bdc0d6456fb32b9e8642bda053f8`  
		Last Modified: Wed, 24 Sep 2025 20:42:22 GMT  
		Size: 76.3 MB (76322772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d19e7c3caecb655f5bb0efae2e98421f664d7dab14dab4a26f7944a1978869`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8ea903490ced720b738540ced6dcb212a180c4737fa8ff6b79455d3ff80e52`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4.2-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:d79dee4273d7b3f5e8d2bd0c0217b54004298bfb1f00b3547b4a00be30077962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee20f57b35fecbed61eb6d90c344087dcf6df70773eae21e59ec4c1195378f6f`

```dockerfile
```

-	Layers:
	-	`sha256:38671e81d3c25beb088deb3fb376c7077da8de731cf5336e28ca1d665461228f`  
		Last Modified: Thu, 25 Sep 2025 02:22:33 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b53831b7bc512d53a7b7be3c225fa3602fcb7e1e9f344bd1e5b920d4380b1d`  
		Last Modified: Thu, 25 Sep 2025 02:22:34 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:fa166d3bdf6beeecf57791b70e558f6ef54e1e6cea95fb7728b45314bc48543b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cff6f2ab47c82bede8226eaa115bb26a3c6b687ca6d1600c4daf951debdab495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81514718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e97594fdb74be0f41ef523f1d997467fd03327d8d08cfda4c4ac4e33bf5a76b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a8ae42cc4bbee908d14c07fc4ec8c8407af6310249f9dfeae0f8509bdc7af`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c7bfad06ee97b9a79123f8649a25c2c85621f43c09f683fc22058f5a07f5d6`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 9.8 MB (9819983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a34cab64443b962a114bd2a6beffb95756ba52160469829a5d45a76fcba800`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a8939940eb42b2ce365e0ace1c34d67dbdaf70d81621f34c5fca12f3bfd8f7`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda56c435bfb0f3172c6ba8994e754a3757983ee0517a7f6b2584a903a27e12e`  
		Last Modified: Thu, 25 Sep 2025 01:11:57 GMT  
		Size: 50.1 MB (50118442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5092574230696c38c9b6d5e80c3b0052a6775a347fc390fb3ddfbed0312b110b`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6964e799275484d75822451544c8b8aeb0525a898edf53d62dc5b2bea9ec4f23`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07acd36aa62e4aa31c3926c29dbc6d78b9952999a9f6d5a20d03ad2ac4ce55cd`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2256c74f4ebf0907ad02de26150d5f5f37dbd8fca3e5b1db457560709bcdc17`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:4cecdea6552df534fc6ff5b0baf01df080318ad872171cb76d8d681529a60c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 KB (941372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e5b13134ce9c59f59464dd153938abe2b1fb108f183574cf50f20c34593ab1`

```dockerfile
```

-	Layers:
	-	`sha256:24d2b9eb10c23f5c732a7e37c15a0f780289592f3ff141a1cf3aed71130b5200`  
		Last Modified: Thu, 25 Sep 2025 02:22:05 GMT  
		Size: 910.6 KB (910603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc19b40f79ef646496790610a3aa4aeb69ed7919b9a4f647f14c2cd431b643e`  
		Last Modified: Thu, 25 Sep 2025 02:22:06 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d76a12db18d7b6e85c3bf97b9627d2043eac00a226367a71789aa4f511b2e675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78685978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1ccd747e4a1c0cfefc72d84b8878fd0133be8c5235727262a387f7c717437b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bee215043e4b9c592d3270a4f9ca98f743ad5efe2f15d29853608a33f501e9e`  
		Last Modified: Wed, 24 Sep 2025 20:42:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd831899112efbf1818c7a1391b355b858f0978cd23d43c7301b385e94bb8fee`  
		Last Modified: Wed, 24 Sep 2025 20:42:10 GMT  
		Size: 9.8 MB (9783483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95fb2184026d4eaa8b66c5dd24e1704f9b8656617244f9830dd08887fcd1c0c`  
		Last Modified: Wed, 24 Sep 2025 20:42:10 GMT  
		Size: 5.8 MB (5790447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b6d057364a9b4e36e9823da94eaf8835e9bac3b077c62a40c181b00530cdfa`  
		Last Modified: Wed, 24 Sep 2025 20:42:09 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edba18fd6c1832982b6768f2002eb35d3cf6c674c66c3250319a5de66db7415f`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 48.0 MB (48017164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7edbd54c33d4091fc7334eb38238f440a45590e52b46baf71b46dd441a50ca`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3a4cfc59e5f76d849da88e7e676f8f42c75ea2fea9a6aa92ed3a2ea7a0b405`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7c6ec75ef0cf8c7cf00e47fc3b0650c76931084ae3b046ef3dfeb076c1f719`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92892ed38d0c82365147f5ff91c9b9018cf22b8a78c94d836c2c98259200b9e5`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:da75c82cd2a446f08e03c0f1f2436f8078f27140db4413a43c3f36b73ff7bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.8 KB (940817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82968150aefd76734cd63972f5c9bb47ad207190dc4e58e3b34ff0ce3e584987`

```dockerfile
```

-	Layers:
	-	`sha256:ac04216069aed10e6fcf7796fc4b9979609d5f75599ec854456b1cade370bf2b`  
		Last Modified: Thu, 25 Sep 2025 02:22:10 GMT  
		Size: 909.9 KB (909854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c9d7656a12cb47dd5db65e1dfe6517aa607a0480a92ae559be75c02b87fffd`  
		Last Modified: Thu, 25 Sep 2025 02:22:10 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:core`

```console
$ docker pull influxdb@sha256:61f49b027eb537eca25e44e83fb375e4b34c9afeb4643085785b6045e33db3e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:86c47dff61aa11be714432ed9dd906192818ffc86fe509c040efd5233b2d0ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115829644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433e4ec2e156f21e5e4d526b8b81805e3c8c64d8f91cec051e57c9030be91c20`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17baf28e6051bd7a25fe013c9c08c6cd7f73bcaa9c734400e0f1f0d284581627`  
		Last Modified: Thu, 25 Sep 2025 01:12:01 GMT  
		Size: 6.7 MB (6665987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b81b90ea3abb8282b95fae868e842fb28507936752797da04f7121d8514f58`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e206217edc4c1be0defb1ba44d2cb562cacb37ea45ea4b6f591350c8f7d42224`  
		Last Modified: Thu, 25 Sep 2025 01:12:11 GMT  
		Size: 79.4 MB (79436081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7779b24984be148a6f6a4dd2751a96927a0ae8eaf063915fc37d68f529f6da45`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd86818b22c1efec0a5c8198f388a6305686db0ae137d779ce3ee90c35a5143`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:72406575b4d8334fa8816af7b7d5622490e873d79077160dc83500043610c83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a111a20e3b57099d9bf669d793746ddc9921c8fb00d81bdb2a02ac6606ea988`

```dockerfile
```

-	Layers:
	-	`sha256:5f9f61f4725c0fc06eda3221e7849e2f1459b46af20799713bf4274d7d5bae06`  
		Last Modified: Thu, 25 Sep 2025 02:22:21 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c72da19de4878ba2801664b77c127422b6571127a04cfb5c4675ff11516d41b`  
		Last Modified: Thu, 25 Sep 2025 02:22:22 GMT  
		Size: 17.6 KB (17591 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:758c1a038d65b404028e569cc9284e00b1c513b50a581a88f9ac16c3a858b331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106588999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452fa4782937755e004b25d81cd21387ee068907e9b99348c35664eefe66b1ae`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76772dfef93d9692ae29670bd3c35ef1b32af43be390336ce02735ca2e6ed34c`  
		Last Modified: Wed, 24 Sep 2025 20:42:13 GMT  
		Size: 6.7 MB (6676456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dd47aad406061c9bef9141140aaa9b6759d82a1c241eb78bfd0557b0bbaf3`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0ca37718bb135be92a784b085b083c56d6441e024e170147d526ce62dbeb13`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 71.0 MB (71047103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf300e1edc90912abd0f245569a70a5e38003d97ee7cc3df20da44178e19697b`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdda608d41ce88b20843112b0fccf8213f3a4cd48021557a305fe7ed9cbe3982`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:7ff5fe04ac92f2cba5c11a9d0ff4aefd16d2e155c4f6aa52979df3849d07098b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae50fbce074dd9457296eabeb258782360b24d7a45b4ccf9881dd8730f19169d`

```dockerfile
```

-	Layers:
	-	`sha256:16a8560fea8f78d8906afef5d7056ce77ddd281f67ae502ad05fe1f856f3bb5f`  
		Last Modified: Thu, 25 Sep 2025 02:22:25 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c8c699c2ee5bfb443845220e3923cb29f00e1999aaa9b529a9909d9725ca59`  
		Last Modified: Thu, 25 Sep 2025 02:22:26 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:fee1fd937f122c29450b5371ad999918de8ea60674c4ebd0b13e1e8253ce0f49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:8e8b0efaee36e18121ab7dc869fe3ee0abd1e15fbcde242c7b9f67c91e194d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121191058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc922de6f2723e8b9d5e0f6d8ac1acf23c76c9d9ca870097495dcbb248d5904`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d2b65053f412e646e84b824154bbe7dfa5e894af0253d642dd08eefcac40b0`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 6.7 MB (6665962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a974fc6c3be5853d851c4367678b3169e8bfc40e4136ec075f865ab903d2c6f`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deed8451ed99c98ccf31f9d5a56ac45437e7654f0b692b232ced6ea304183de1`  
		Last Modified: Thu, 25 Sep 2025 01:12:05 GMT  
		Size: 84.8 MB (84797518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abf28c19a8e2f63583616a1371baac7224ce0aa8039aefdbffcc14943f2ba12`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbcad217e989b316b8d5390328e498a1c7a67c7288799a96eea414060a54ea0`  
		Last Modified: Thu, 25 Sep 2025 01:12:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:caf5e328dec6182bcb6a665df4ea084f9b6cea24fc26642b4d3d44f9225fb153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c5bb899fbf546577b5574ac6892f51c5329bf86779b69e40d94337327ad702`

```dockerfile
```

-	Layers:
	-	`sha256:53749ce6fb588cb7c4356dfb8371a918c17514d4ee9d88e47f92aec9beafdff5`  
		Last Modified: Thu, 25 Sep 2025 02:22:28 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef91f4467414786cdf25738378986deb0f9d7405fc99ff64ebc67cbf6d0455a`  
		Last Modified: Thu, 25 Sep 2025 02:22:29 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:49b06572ed51033ab384673ac640e7efb021dc7ea64244077c0eaece0ac7e4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111864713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bff344b48f080250935ce5d2295f18d545a3573179f7e245805604e9439b16`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63986cf6045810298066b4a7dd264d5d2c4422ffbf792a0414c4a3e642d30233`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 6.7 MB (6676493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d79724c215b55fae9017081e43d63d95ab2d5a85837f4314a4a92798e224e7`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fe097ce79f895e72472cdda7d81b7899b9bdc0d6456fb32b9e8642bda053f8`  
		Last Modified: Wed, 24 Sep 2025 20:42:22 GMT  
		Size: 76.3 MB (76322772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d19e7c3caecb655f5bb0efae2e98421f664d7dab14dab4a26f7944a1978869`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8ea903490ced720b738540ced6dcb212a180c4737fa8ff6b79455d3ff80e52`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:d79dee4273d7b3f5e8d2bd0c0217b54004298bfb1f00b3547b4a00be30077962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee20f57b35fecbed61eb6d90c344087dcf6df70773eae21e59ec4c1195378f6f`

```dockerfile
```

-	Layers:
	-	`sha256:38671e81d3c25beb088deb3fb376c7077da8de731cf5336e28ca1d665461228f`  
		Last Modified: Thu, 25 Sep 2025 02:22:33 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b53831b7bc512d53a7b7be3c225fa3602fcb7e1e9f344bd1e5b920d4380b1d`  
		Last Modified: Thu, 25 Sep 2025 02:22:34 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:7cef9509aaad441529b985839e18abdf276813f0e96e53a4b588a8982ba1b22b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:99ec207e034a0030cfe9b324abd7d17c5359c30c00fe380e38bb343d32236757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf3d8c36b817ec2a3134909fa3ced93611ae30df9a9212fd88a827f6dc70cd3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV GOSU_VER=1.16
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f21742dbff9b844e8ebe7bc73fdd25b4246af656bc0a29c6b9f8d69a56d4e12`  
		Last Modified: Thu, 25 Sep 2025 01:12:23 GMT  
		Size: 9.8 MB (9796243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36fc49d49d1a27e5a8d04a999e6f56e7b499930c350fe0df2d2e7bc7802fb8e`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 6.2 MB (6156975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d232cb48b053d662eb2a0ebf0f93b556ad770c7455453ec0c7999233363ae04`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea323cfe236177f0122d70f051ffb9d262f532128b7df58448c8abab533a6fd`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 1.0 MB (1012030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eebc994e1765337ac74a0a9d063bfe6ba57130b07dfd0e6ccecb7d7ff17b683`  
		Last Modified: Thu, 25 Sep 2025 01:12:28 GMT  
		Size: 100.2 MB (100244537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489fccc0e03e220d305a6654112101c64052df1d23cd3f206f5f833d4035e2c7`  
		Last Modified: Thu, 25 Sep 2025 01:12:23 GMT  
		Size: 11.8 MB (11773804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8948b91899dae640e1f8ee6c01dfaddc356af1b0fd1d0c3b1aa5f8a49a1d7015`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04420871cdff010a378fbadfefb97c7fa29f919193a4246c646e7ae8b5da5bc2`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7058e6744694a1062c598527550938140a3a61c0a83b9628f8373f408e91d698`  
		Last Modified: Thu, 25 Sep 2025 01:12:22 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:e2b41419d76750bb8d9fcbba2731a2c939acf772e283bd4cb02795d03a8785c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48557e802771f4374647ee6d591718afdd412df1e19f465f67413038f1cd1c62`

```dockerfile
```

-	Layers:
	-	`sha256:1d57937036d3daf271d4c03c34e7425d7d2d60a5261c2ff78249218a424f5ebe`  
		Last Modified: Thu, 25 Sep 2025 02:21:57 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8130e16a0cc378e5e9a85749da908ba586fac9377f75da9e5bf7d5bfd808266`  
		Last Modified: Thu, 25 Sep 2025 02:21:58 GMT  
		Size: 33.5 KB (33537 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:360dcee62c844c23a234bfafbfe5511a9eec36708ac018898417109abf442919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be31ac8b81e9cfd609c523de74012f65cb50e861e392ba63ba22aabd796f607f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV GOSU_VER=1.16
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb01127f4ecc7cec32d1038e47228414dc56b31af3bbe48fef16e87315ccbe2e`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 9.6 MB (9626297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3946c56889b4245bea086fd3932326e26ad874953fe751707350630acdae998e`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9e3f58b659a18c358e334cc15930a931b940051e6d5c5ea9c651490f58865d`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5242355409b896247ed91922f8f8eed4ff5cbf779a515539eda0d707bc28fd38`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cce3bcba21ff833984ada7e3fa4ecf3160c0b46f032bbcf082a0caa3d7fd09`  
		Last Modified: Wed, 24 Sep 2025 20:42:21 GMT  
		Size: 96.0 MB (96038999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0db4d928b52404e26b6f1c213333ab49fc4d1f2e17d01312187f82e96fb5478`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 11.1 MB (11099991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802ede4ca46ce31c894904679fe589cc47cb6a1623f99c04f2f0476135eb2fa8`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b64c4076b267fc9adfeab0eadbfabc70fd195b90720bfe6e74378fa0621d42c`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7864a9ac5c643bf554f8ba4d96a66ab30967e45048c19bbc695e08f70d2ba50e`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:740c7608085e12a989c31bb6765091b2e748e1ac2e1ad5b729683c9c7ed8445b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f4c48a7e65713d45172ae2f2cc1fe1409b4d8d33212de76f972c846d8c46bd`

```dockerfile
```

-	Layers:
	-	`sha256:6fd46fce2dd3e7092712a8481fd90a644582c32e5ba9ea39c77ecc42c7ff7511`  
		Last Modified: Thu, 25 Sep 2025 02:22:02 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b376a7e3f08be287cee166060598253dc80b41b60df84212e3b7b21d5ab60cb`  
		Last Modified: Thu, 25 Sep 2025 02:22:02 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json
