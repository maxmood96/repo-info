<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.10-data`](#influxdb110-data)
-	[`influxdb:1.10-data-alpine`](#influxdb110-data-alpine)
-	[`influxdb:1.10-meta`](#influxdb110-meta)
-	[`influxdb:1.10-meta-alpine`](#influxdb110-meta-alpine)
-	[`influxdb:1.10.8-data`](#influxdb1108-data)
-	[`influxdb:1.10.8-data-alpine`](#influxdb1108-data-alpine)
-	[`influxdb:1.10.8-meta`](#influxdb1108-meta)
-	[`influxdb:1.10.8-meta-alpine`](#influxdb1108-meta-alpine)
-	[`influxdb:1.11`](#influxdb111)
-	[`influxdb:1.11-alpine`](#influxdb111-alpine)
-	[`influxdb:1.11-data`](#influxdb111-data)
-	[`influxdb:1.11-data-alpine`](#influxdb111-data-alpine)
-	[`influxdb:1.11-meta`](#influxdb111-meta)
-	[`influxdb:1.11-meta-alpine`](#influxdb111-meta-alpine)
-	[`influxdb:1.11.8`](#influxdb1118)
-	[`influxdb:1.11.8-alpine`](#influxdb1118-alpine)
-	[`influxdb:1.11.8-data`](#influxdb1118-data)
-	[`influxdb:1.11.8-data-alpine`](#influxdb1118-data-alpine)
-	[`influxdb:1.11.8-meta`](#influxdb1118-meta)
-	[`influxdb:1.11.8-meta-alpine`](#influxdb1118-meta-alpine)
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
-	[`influxdb:3.4.1-core`](#influxdb341-core)
-	[`influxdb:3.4.1-enterprise`](#influxdb341-enterprise)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:core`](#influxdbcore)
-	[`influxdb:enterprise`](#influxdbenterprise)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:f70d22063343f166adcefb1d1ddb31fcabc58c165141eb9c2d4c2c4275940ad0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f6132c1e753d7ba93faf51f3000646fcbf8e979cca7edd3b81907c9c78156237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108963918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5150d33d2f7018e9c5ca9b5353eceadf9e489f88ded96b1a241a6109f1f34132`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Thu, 28 Aug 2025 18:37:27 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
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
	-	`sha256:0fdc44680a1e84d773a38af7087fd430a6b65918b14ad5945b4053fd3067cc8d`  
		Last Modified: Mon, 08 Sep 2025 23:22:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8477632abb241a07c1591d3dbb9d37953290f91d0c189627006582aacb32c3e`  
		Last Modified: Mon, 08 Sep 2025 21:57:31 GMT  
		Size: 39.4 MB (39439618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685377eb4481e2a51d0bd93749ca748bbe4afbe541ca08c47ea080681707c5f9`  
		Last Modified: Mon, 08 Sep 2025 23:22:43 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d08f68eded1c60fd06a0274fac93eef2e5c72c0865ed9c0bbb804877f2dbc`  
		Last Modified: Mon, 08 Sep 2025 23:22:43 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a406f96ca7b7b9c9c6f51a396224568a1b884ee5df37c0cb1ffe7e2524e705`  
		Last Modified: Mon, 08 Sep 2025 23:22:43 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:948ac253b3242ea07d1625b70dcdb2fc7966a7e9c6bc99bdcbdc24e9ce043d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4799034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb4270c4c738616f6ca1be157865d4145aaacf917eca2850878cc6d41c2c996`

```dockerfile
```

-	Layers:
	-	`sha256:d0a3f26a6c208bd01ae7c0a1dd97c4118e544a86ca1a1e4c53dd5fde46cad92c`  
		Last Modified: Mon, 08 Sep 2025 23:20:24 GMT  
		Size: 4.8 MB (4784326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4db43c18d2c8e84c6843a188411275e2e484bbe152aa4469c3e286e4eba76f9`  
		Last Modified: Mon, 08 Sep 2025 23:20:25 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:b0abaca7d9485e37b930a0fca141355a0d34ecef17236998134c81ea41785a5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f2e57fd8a9160bd46b2600d467c5a2e4d3a0ad90fece41e31f45eda5e09dd2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44219737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545ab85a3443da042fcca5b877db26de622a9d0ca44593591c103d3b18a5c82f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Thu, 03 Jul 2025 17:46:22 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c626fe462930df3f86c4e07b5b26ec2a44c537ed5d15f7f48bf90ecd31abb1`  
		Last Modified: Tue, 15 Jul 2025 20:47:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294e95ece9e192f943115445d6a36388d1418ba07e45cd8ede7857a31db9217f`  
		Last Modified: Tue, 15 Jul 2025 20:47:25 GMT  
		Size: 1.2 MB (1217670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423ebab50a6e84106c1692fa6ff709c5ec008424c1b5b19af2d0964b1895c077`  
		Last Modified: Thu, 17 Jul 2025 04:06:31 GMT  
		Size: 39.4 MB (39379539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805da5749c2b66591fe59e3c0ddbf0bcd2c2a1eaaa8578c281ad0292700ddcfc`  
		Last Modified: Tue, 15 Jul 2025 20:47:36 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19876754d54508ec6d2f5ceac27a6341e7e373fb2578d657bdb7d11ba243bc`  
		Last Modified: Tue, 15 Jul 2025 20:47:41 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0732396d66653baccffd84c09aa98976ef2b7544a542c4b6d72487ae388ae62d`  
		Last Modified: Tue, 15 Jul 2025 20:47:43 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:95653b2589d2d9282cd3dbd049a435265819ed01799332643bb6c65033b57a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.8 KB (768814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784c3375350d7ae5b3ff9750b3f1ac81544888f3f0c004d29bc494fe5eae205a`

```dockerfile
```

-	Layers:
	-	`sha256:b20159ff8c8b957d8698b493364b34b5d1ad679acf0a9fd90db4718b1e66091f`  
		Last Modified: Tue, 15 Jul 2025 23:20:18 GMT  
		Size: 752.2 KB (752175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8981cb96b24fbf030dc4f6734d02fc671ac4fd5364d9f4fda4a45c4fd84d1b61`  
		Last Modified: Tue, 15 Jul 2025 23:20:19 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:138930c5d58162123bc4cd59d36f5dbcfbd8d5b9055bfff9eb9e1c8f9471c214
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:805c3c270e5de2b7e39e2c8b2e722fe3123f92f9daaa29fc34f97444a6e76c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88163108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3059a3fa28b82f2fd8adb5cd393a89d5775815a5a8d5e2ef37c07120ef3e75e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Thu, 28 Aug 2025 18:37:27 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
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
	-	`sha256:6341b574f6cd703623a4f31a62c3f72864e66fcaa8d957fc01702aea083acc00`  
		Last Modified: Mon, 08 Sep 2025 22:42:52 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655b36b817baec330e0a5ba428217371d04a7384035bb99bc72f01100b6a4aa9`  
		Last Modified: Mon, 08 Sep 2025 21:57:18 GMT  
		Size: 18.6 MB (18640031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79acdc09ec0b6880df8d5a4e23fd389f76f6749fb2eb7e9555cfd2a8a8ca7b2c`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fef472dc4ad2c27d1a0c6311d7726c758cf442f7bad8f000f395515f332999`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:5ab7364ca4c8b696e2f7569073d7a677bd5b7d8e7c6c7858f2593b0a0d7457f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f9bd1271627a8c81f0d4f721f77c2aa801cd2da5afd0179d0bd8894a201359`

```dockerfile
```

-	Layers:
	-	`sha256:d637372cf52dedfc6a636bb79b50853b9d950da2eb7dc2959bd5927556788a09`  
		Last Modified: Mon, 08 Sep 2025 23:20:28 GMT  
		Size: 4.7 MB (4708306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bafb9df1a531c8303c17a169d03906312774ec0df254c1025a10d7b6fbac45d`  
		Last Modified: Mon, 08 Sep 2025 23:20:29 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:3e1a956a422b884a440c0a505c0921b009e8825e0cc6e3ac8bd4fb0d8dea2406
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c7b2e54e4310e9ec3760d428938c1fa46fa17560431b90ff22fc847d4b1a8225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23435278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debd662a6d8899d0d8798c15da2562b255ef34146ea3a758f314aebbc831125b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Thu, 03 Jul 2025 17:46:22 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9cb96868f1562b72f610ec278eee037efe20abe2a0ea153c2f1fa28130ac17`  
		Last Modified: Tue, 15 Jul 2025 20:46:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c616fd2e27446b0727bc43d57664c3509443deecabcde2e87b69481af1236bb`  
		Last Modified: Tue, 15 Jul 2025 20:46:26 GMT  
		Size: 1.2 MB (1217673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd559660b5d06c773dc1097b33dd70bcb7960f22481dbda7788a0abc8f320e56`  
		Last Modified: Wed, 16 Jul 2025 14:39:52 GMT  
		Size: 18.6 MB (18596285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e68b87eb53be69653781a5059589642c27b089d75afec5112ba6711b730d09`  
		Last Modified: Tue, 15 Jul 2025 20:46:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96c08d2d4240556579d6eea6505534972778467142d3edae5cd2074fe866857`  
		Last Modified: Tue, 15 Jul 2025 20:46:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f20ca52c0596039e9662b1cef2b7494a23dd37f8abf8bdc95eeef691714b0d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.3 KB (691319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac3b3ac4c1fea726f8e458ef990aa8bbb40e917f7c87606fde9106adf47a45f`

```dockerfile
```

-	Layers:
	-	`sha256:02ac197e64df2029437e8f9a3c0b82c9f47732af84ecab9171e7817c79d2d83d`  
		Last Modified: Tue, 15 Jul 2025 23:20:23 GMT  
		Size: 676.3 KB (676311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dc0d841f0b56fdb4a5597e4eb62810652b2e5c52f001b67840cd9af8079478e`  
		Last Modified: Tue, 15 Jul 2025 23:20:23 GMT  
		Size: 15.0 KB (15008 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.8-data`

```console
$ docker pull influxdb@sha256:f70d22063343f166adcefb1d1ddb31fcabc58c165141eb9c2d4c2c4275940ad0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f6132c1e753d7ba93faf51f3000646fcbf8e979cca7edd3b81907c9c78156237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108963918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5150d33d2f7018e9c5ca9b5353eceadf9e489f88ded96b1a241a6109f1f34132`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Thu, 28 Aug 2025 18:37:27 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
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
	-	`sha256:0fdc44680a1e84d773a38af7087fd430a6b65918b14ad5945b4053fd3067cc8d`  
		Last Modified: Mon, 08 Sep 2025 23:22:43 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8477632abb241a07c1591d3dbb9d37953290f91d0c189627006582aacb32c3e`  
		Last Modified: Mon, 08 Sep 2025 21:57:31 GMT  
		Size: 39.4 MB (39439618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685377eb4481e2a51d0bd93749ca748bbe4afbe541ca08c47ea080681707c5f9`  
		Last Modified: Mon, 08 Sep 2025 23:22:43 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d08f68eded1c60fd06a0274fac93eef2e5c72c0865ed9c0bbb804877f2dbc`  
		Last Modified: Mon, 08 Sep 2025 23:22:43 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a406f96ca7b7b9c9c6f51a396224568a1b884ee5df37c0cb1ffe7e2524e705`  
		Last Modified: Mon, 08 Sep 2025 23:22:43 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:948ac253b3242ea07d1625b70dcdb2fc7966a7e9c6bc99bdcbdc24e9ce043d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4799034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb4270c4c738616f6ca1be157865d4145aaacf917eca2850878cc6d41c2c996`

```dockerfile
```

-	Layers:
	-	`sha256:d0a3f26a6c208bd01ae7c0a1dd97c4118e544a86ca1a1e4c53dd5fde46cad92c`  
		Last Modified: Mon, 08 Sep 2025 23:20:24 GMT  
		Size: 4.8 MB (4784326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4db43c18d2c8e84c6843a188411275e2e484bbe152aa4469c3e286e4eba76f9`  
		Last Modified: Mon, 08 Sep 2025 23:20:25 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.8-data-alpine`

```console
$ docker pull influxdb@sha256:b0abaca7d9485e37b930a0fca141355a0d34ecef17236998134c81ea41785a5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f2e57fd8a9160bd46b2600d467c5a2e4d3a0ad90fece41e31f45eda5e09dd2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44219737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545ab85a3443da042fcca5b877db26de622a9d0ca44593591c103d3b18a5c82f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Thu, 03 Jul 2025 17:46:22 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c626fe462930df3f86c4e07b5b26ec2a44c537ed5d15f7f48bf90ecd31abb1`  
		Last Modified: Tue, 15 Jul 2025 20:47:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294e95ece9e192f943115445d6a36388d1418ba07e45cd8ede7857a31db9217f`  
		Last Modified: Tue, 15 Jul 2025 20:47:25 GMT  
		Size: 1.2 MB (1217670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423ebab50a6e84106c1692fa6ff709c5ec008424c1b5b19af2d0964b1895c077`  
		Last Modified: Thu, 17 Jul 2025 04:06:31 GMT  
		Size: 39.4 MB (39379539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805da5749c2b66591fe59e3c0ddbf0bcd2c2a1eaaa8578c281ad0292700ddcfc`  
		Last Modified: Tue, 15 Jul 2025 20:47:36 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19876754d54508ec6d2f5ceac27a6341e7e373fb2578d657bdb7d11ba243bc`  
		Last Modified: Tue, 15 Jul 2025 20:47:41 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0732396d66653baccffd84c09aa98976ef2b7544a542c4b6d72487ae388ae62d`  
		Last Modified: Tue, 15 Jul 2025 20:47:43 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:95653b2589d2d9282cd3dbd049a435265819ed01799332643bb6c65033b57a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.8 KB (768814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784c3375350d7ae5b3ff9750b3f1ac81544888f3f0c004d29bc494fe5eae205a`

```dockerfile
```

-	Layers:
	-	`sha256:b20159ff8c8b957d8698b493364b34b5d1ad679acf0a9fd90db4718b1e66091f`  
		Last Modified: Tue, 15 Jul 2025 23:20:18 GMT  
		Size: 752.2 KB (752175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8981cb96b24fbf030dc4f6734d02fc671ac4fd5364d9f4fda4a45c4fd84d1b61`  
		Last Modified: Tue, 15 Jul 2025 23:20:19 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.8-meta`

```console
$ docker pull influxdb@sha256:138930c5d58162123bc4cd59d36f5dbcfbd8d5b9055bfff9eb9e1c8f9471c214
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:805c3c270e5de2b7e39e2c8b2e722fe3123f92f9daaa29fc34f97444a6e76c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88163108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3059a3fa28b82f2fd8adb5cd393a89d5775815a5a8d5e2ef37c07120ef3e75e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Thu, 28 Aug 2025 18:37:27 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
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
	-	`sha256:6341b574f6cd703623a4f31a62c3f72864e66fcaa8d957fc01702aea083acc00`  
		Last Modified: Mon, 08 Sep 2025 22:42:52 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655b36b817baec330e0a5ba428217371d04a7384035bb99bc72f01100b6a4aa9`  
		Last Modified: Mon, 08 Sep 2025 21:57:18 GMT  
		Size: 18.6 MB (18640031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79acdc09ec0b6880df8d5a4e23fd389f76f6749fb2eb7e9555cfd2a8a8ca7b2c`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fef472dc4ad2c27d1a0c6311d7726c758cf442f7bad8f000f395515f332999`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:5ab7364ca4c8b696e2f7569073d7a677bd5b7d8e7c6c7858f2593b0a0d7457f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f9bd1271627a8c81f0d4f721f77c2aa801cd2da5afd0179d0bd8894a201359`

```dockerfile
```

-	Layers:
	-	`sha256:d637372cf52dedfc6a636bb79b50853b9d950da2eb7dc2959bd5927556788a09`  
		Last Modified: Mon, 08 Sep 2025 23:20:28 GMT  
		Size: 4.7 MB (4708306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bafb9df1a531c8303c17a169d03906312774ec0df254c1025a10d7b6fbac45d`  
		Last Modified: Mon, 08 Sep 2025 23:20:29 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.8-meta-alpine`

```console
$ docker pull influxdb@sha256:3e1a956a422b884a440c0a505c0921b009e8825e0cc6e3ac8bd4fb0d8dea2406
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c7b2e54e4310e9ec3760d428938c1fa46fa17560431b90ff22fc847d4b1a8225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23435278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debd662a6d8899d0d8798c15da2562b255ef34146ea3a758f314aebbc831125b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Thu, 03 Jul 2025 17:46:22 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9cb96868f1562b72f610ec278eee037efe20abe2a0ea153c2f1fa28130ac17`  
		Last Modified: Tue, 15 Jul 2025 20:46:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c616fd2e27446b0727bc43d57664c3509443deecabcde2e87b69481af1236bb`  
		Last Modified: Tue, 15 Jul 2025 20:46:26 GMT  
		Size: 1.2 MB (1217673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd559660b5d06c773dc1097b33dd70bcb7960f22481dbda7788a0abc8f320e56`  
		Last Modified: Wed, 16 Jul 2025 14:39:52 GMT  
		Size: 18.6 MB (18596285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e68b87eb53be69653781a5059589642c27b089d75afec5112ba6711b730d09`  
		Last Modified: Tue, 15 Jul 2025 20:46:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96c08d2d4240556579d6eea6505534972778467142d3edae5cd2074fe866857`  
		Last Modified: Tue, 15 Jul 2025 20:46:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f20ca52c0596039e9662b1cef2b7494a23dd37f8abf8bdc95eeef691714b0d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.3 KB (691319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac3b3ac4c1fea726f8e458ef990aa8bbb40e917f7c87606fde9106adf47a45f`

```dockerfile
```

-	Layers:
	-	`sha256:02ac197e64df2029437e8f9a3c0b82c9f47732af84ecab9171e7817c79d2d83d`  
		Last Modified: Tue, 15 Jul 2025 23:20:23 GMT  
		Size: 676.3 KB (676311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dc0d841f0b56fdb4a5597e4eb62810652b2e5c52f001b67840cd9af8079478e`  
		Last Modified: Tue, 15 Jul 2025 23:20:23 GMT  
		Size: 15.0 KB (15008 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11`

```console
$ docker pull influxdb@sha256:1fe652fe46cc9250b1e01f302a4b079c60b263fa7b6c24f0847ce062dbd1bf88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:b350726c3fa501f65b7a94dcf8599a4faca41a61ffb707b453d1d9972ce89049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116163525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e190497e82423991d556cb21eb08f429571a5db54f5376231609a036ee6ab3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 28 Aug 2025 18:37:27 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
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
	-	`sha256:6243170e31ed9b045fc79e3e137b2a451a688c910ecfa7266e4bc56fdabf5681`  
		Last Modified: Mon, 08 Sep 2025 23:20:57 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c571a95dfffaa44436c23181ed3f5c848caa135c53a727fc4a497fe9708cfc`  
		Last Modified: Mon, 08 Sep 2025 23:21:00 GMT  
		Size: 43.7 MB (43654007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d66ea1e5ddf6b93ae0e22ff9b88095e4a2ef8b90c708d20ff8b069a19e08da2`  
		Last Modified: Mon, 08 Sep 2025 23:20:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f32ae8336dbf6b6a3e4a297dd6ea5d84cf58b7a6704afebcb3ec80a26cfbdd3`  
		Last Modified: Mon, 08 Sep 2025 23:20:59 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f293d4b8a1df9bcb5ace025df87993ee45ab4760c39c324aebce3250daa6779`  
		Last Modified: Mon, 08 Sep 2025 23:21:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:eb5c3673b02b7fdc3798525c4b3badfd45a9c4a0fdf2caa6a603b699fd68cdbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2098eb33abddd4daa72dcfdbe42fbe6f592972ca6118ce4e597550e33d1e753a`

```dockerfile
```

-	Layers:
	-	`sha256:3947587988ff4cf36ee42dfa966dfdef9e0a873676c0f644aaab35483c21ed3d`  
		Last Modified: Mon, 08 Sep 2025 23:20:37 GMT  
		Size: 5.1 MB (5078620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04021c33d71220d3d1df1d49293eec7c706e47d626e86bf94012833e5c7acfbd`  
		Last Modified: Mon, 08 Sep 2025 23:20:38 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d6d0563b20c9093cfbc2fe57c1d58290d4640725b04480d3ab012d67e44d4df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113077045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a6729d3504ca5ceb6d85bddd148f07093398e3bdb5b2d06a1b50b0e2045de2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 28 Aug 2025 18:37:27 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
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
	-	`sha256:97955a0cb7e8a0ceb18d8e014531ce1de6577a12664fe21d09e22d665d6dfdb9`  
		Last Modified: Tue, 09 Sep 2025 02:14:56 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aba530552581631f28f3b47d469ecb50292deb4a1160693e543a6d2c6a78b5`  
		Last Modified: Tue, 09 Sep 2025 05:20:28 GMT  
		Size: 41.1 MB (41120326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc12198b70b02d4eba057245b8eafe1367e6c670e5a6b96609dc2ab2632b4ff3`  
		Last Modified: Tue, 09 Sep 2025 02:14:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a707539214d47736871a6e92b02f803f243ea9d1eed1ee899b7ba88500f510`  
		Last Modified: Tue, 09 Sep 2025 02:14:57 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78464ae95a9e74070a124a94124feba1d20bd5bc608764a64813a25887159fe0`  
		Last Modified: Tue, 09 Sep 2025 02:14:56 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:3d85c2244f6342cf6a320532621270ba70230f30ab2bb0706e3b91ed8ca67db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cb108da2bf97cf468b18420762b1ae6cc610d3d834dc9f1cf10963745c1d39`

```dockerfile
```

-	Layers:
	-	`sha256:931b097db463802416e1dc731eb5e3492610263743efb18892becbbf7f96a733`  
		Last Modified: Tue, 09 Sep 2025 05:20:23 GMT  
		Size: 5.1 MB (5078085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff0fe5382aba43f5a674887506c2143e0b09cc7b98179017a94956f57adfbc1`  
		Last Modified: Tue, 09 Sep 2025 05:20:24 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-alpine`

```console
$ docker pull influxdb@sha256:138f19e5685514f3b91dee1b5a53ed6b77134c7356cd0384a7781c902c01c375
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c02e7eb95cd84a5eff5db97efcbd65fc2e3f61e620a5cc7c9a481a3cd12c8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42909082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7f02263b1f21a109432dc16aeadc1c6e1f2243aee678f111997f9faee582cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 03 Jul 2025 17:46:22 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cdf703c988b90a506e51b1a7870074ca976afe3cf8ba4ffefc1a9a3802bc58`  
		Last Modified: Tue, 15 Jul 2025 21:34:26 GMT  
		Size: 1.2 MB (1217662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f4ac331105e966636f8e81b8c44ecac0cdaac1dc1b9f53957cd6d191311b4e`  
		Last Modified: Tue, 15 Jul 2025 23:20:31 GMT  
		Size: 38.1 MB (38068228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a8ce52868a0b7dd9ceb9a61801b5c8aa1f35a5053b5d15761c809b00c29e14`  
		Last Modified: Tue, 15 Jul 2025 21:34:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6892154e596bd1ad278ceac48678c52c980e18fe9dfbd8b6a0d8c3d0884ea5a4`  
		Last Modified: Tue, 15 Jul 2025 21:34:27 GMT  
		Size: 999.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f35936e07afbbc0e42db14df940027b31b3ae625cf0732ded86bf1410764d18`  
		Last Modified: Tue, 15 Jul 2025 21:34:28 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26572fb2dd53dcc1431ee3d783cfae93431609dd1b481f6768e467d50d6f67ac`  
		Last Modified: Tue, 15 Jul 2025 21:34:34 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:15a79bbccbd314af27645833571b31a9aaf700233f748b52cc04de17e487ed8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.7 KB (757742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0963f3c5cedd0b4b3c2cd96f8d92b87bc687a9317881f4489a106c409b901a1e`

```dockerfile
```

-	Layers:
	-	`sha256:4e619d1dac411fcf2dac09dfcddc02b9ebd0a239d75e99ced83817d81966fb20`  
		Last Modified: Tue, 15 Jul 2025 23:20:30 GMT  
		Size: 739.9 KB (739869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aac0057bc38790b1784893af404060f691942579fc819af2761bebc99d3bce4`  
		Last Modified: Tue, 15 Jul 2025 23:20:30 GMT  
		Size: 17.9 KB (17873 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:9cd9ba2e4569693ebccf6cde53197a4e56350586974cbab331772bc4d7b179f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40933009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ad4af985e8f2af1242da5ec46fd4b9926ec0765a37054c1b92787997db839f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 03 Jul 2025 17:46:22 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107448bacbe733297b040236d890a68ba7de0745b30fd384b8d23263a83daefd`  
		Last Modified: Wed, 16 Jul 2025 00:17:01 GMT  
		Size: 1.3 MB (1296536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36431ddb424d34cbad9aa722f22b084252d11fe870db747bfac0e9a476f0134e`  
		Last Modified: Wed, 16 Jul 2025 00:17:06 GMT  
		Size: 35.5 MB (35545387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2746309bcef96c794924b818e9e9b26688d79244496bbb7e371fed1c51e83718`  
		Last Modified: Wed, 16 Jul 2025 00:17:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e74d66f0ddeb59deeb029d729da782f64701fa4543bbb236079461fd4090c1`  
		Last Modified: Wed, 16 Jul 2025 00:17:01 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166127b6c6a42d743c597bb6077eb80b64eb236d8a9071451a2b7616e351140d`  
		Last Modified: Wed, 16 Jul 2025 00:17:01 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46aa7dbe029fbf3145fbbc8d015fbbe445a1bc3bd55476152d55f3745f41d54`  
		Last Modified: Wed, 16 Jul 2025 00:17:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e6f8506d051c4f2b9f28242b342b63df77acc1b058111515374711e1e3455714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.1 KB (757083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eade6518476c5429dd8828f274005e1541cd8af980349da19829ecedffd29d`

```dockerfile
```

-	Layers:
	-	`sha256:851289b34c3ef45e1406cdbaa86c664d47f46980df311c1a8b9dbc38a53a134a`  
		Last Modified: Wed, 16 Jul 2025 02:20:24 GMT  
		Size: 739.1 KB (739096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854f9fc20d333c0b08bda6757b097db1abb4fe6b1782d627613e8bcb56c27f24`  
		Last Modified: Wed, 16 Jul 2025 02:20:25 GMT  
		Size: 18.0 KB (17987 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:d57a2049ec438f6058e0c7acde28cd25f0943739c8bec98c08aebe3765215e47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f51d91478c0b5c8dae1aae6ca557bde6c8617216edf9adbcfd52ac19d640eebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111689695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8d39ebc6b6384182e6e89491fa430c0ff0c39251c8867a8d8108dca7280f91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Thu, 28 Aug 2025 18:37:27 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
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
	-	`sha256:2a19dfb20162d87acc977ac67c19ec82d232c4d1b259e73326fd0d996587f1dd`  
		Last Modified: Mon, 08 Sep 2025 22:38:31 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82f6677cbf9b0a84d343e202f04fbdb1edd600a1d71a9cdaccbfb95cbd4aa81`  
		Last Modified: Mon, 08 Sep 2025 21:57:40 GMT  
		Size: 39.2 MB (39179533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6669a805a8323e4145d710825da67e04134cf2ddd2c77f50d07279f7905da86`  
		Last Modified: Mon, 08 Sep 2025 22:38:34 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9461e8807654eaae8e6739c70c33babd6360fe350a3fd24cf8db5323741fc58d`  
		Last Modified: Mon, 08 Sep 2025 22:38:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3b75326d321c67f3815a0b4fa501147074478dabc930be6bb12fe7d337d83f`  
		Last Modified: Mon, 08 Sep 2025 22:38:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:98adbf06ee5245ee11ccb9e39385e2d543a70fb805964bb06fc887f8871f77af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4682505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff600f27c3d61fc562cbc49d041d5933e457ea3bc9e45e8369259e54601c6b26`

```dockerfile
```

-	Layers:
	-	`sha256:ccf2f8886ff5216ec2b37d70a8ba7df4296e7c495a32667ea0c96f85d5120324`  
		Last Modified: Mon, 08 Sep 2025 23:20:42 GMT  
		Size: 4.7 MB (4667797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ee73478ec9d36d44f5758868a06aa8af164cc1a8f3d3d594633d97068079fcc`  
		Last Modified: Mon, 08 Sep 2025 23:20:43 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:381bd28215770143c72eab8ca2170a3d31e8e88acc3be7c9d198804729414956
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:96b59b101b2a5e451f5f947c04f3e46378c9a3681f41df121bc4dd3eb785d389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43963829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9353a878a5beb3047c128eb9d9149a950e388e5c8b2f0e3a072ff162d9184579`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Thu, 03 Jul 2025 17:46:22 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7cd59a170b5fff4759056f3021cd3a0f8b8b93fd86f3b540f889da699918c6`  
		Last Modified: Tue, 15 Jul 2025 20:46:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c28885a79e009e286e4f9a293cba3159388662f0e7348a60b74ccf232bec4e`  
		Last Modified: Tue, 15 Jul 2025 20:46:50 GMT  
		Size: 1.2 MB (1217668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e9d594775205c1ee1832d8b017c91770b09b6aadfc1ebb9c31d5587fd21a68`  
		Last Modified: Thu, 17 Jul 2025 04:06:22 GMT  
		Size: 39.1 MB (39123633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b71615bfecfb828537f7c993fe93ff50bf019853db7ec1c27609e5df5eeda8`  
		Last Modified: Tue, 15 Jul 2025 20:47:13 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e728fa1ce435bbdea26982955e9b3fefdd18e8c6ad39f5e0ffeba2525a6a49a`  
		Last Modified: Tue, 15 Jul 2025 20:47:16 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4ebfff5a877c2cc2c5b880287f92b8f3c3ec679ec7be2017f0ef35d79c1aaf`  
		Last Modified: Tue, 15 Jul 2025 20:47:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c66ae295b7d7a33b393f6dc9d9c9fe3a94afd550d714d211ec06980498a33908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **767.1 KB (767053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42347b07372c3c71c03691eb26b8eed6f42a77e1bef4fc5c6670e676bc414b4a`

```dockerfile
```

-	Layers:
	-	`sha256:6b19dbadcc4e5898d140eeff835d6e705d6a4ccc08aac69768d773dfc892febd`  
		Last Modified: Tue, 15 Jul 2025 23:20:33 GMT  
		Size: 750.4 KB (750414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f398e7228caee2c145d1f269d0f5839080d1d0d6ccbb809d4fc8b5c7fd2784b`  
		Last Modified: Tue, 15 Jul 2025 23:20:34 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:1c198519bf1b1bded210e6f870d22354b7956fbb8d671fd33bfc7f0e2e2486d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:6b46d915b14f49d0e8cd1c6d30f3b308728246f98438c0ca069c439789c15727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90845710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216dda4bb2297e769c2c36d9cdf09b20a8e7880d96b984850acb78e3a24b9a9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Thu, 28 Aug 2025 18:37:27 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
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
	-	`sha256:7c74cb8773783cd77f8754eaeb3e502846c92918abae8c3e3bf4e55337648ac4`  
		Last Modified: Mon, 08 Sep 2025 23:19:40 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39f58484a4d9d46791fa08eea720f2404c5fc437eee770436c4801dfe04f55b`  
		Last Modified: Mon, 08 Sep 2025 21:57:32 GMT  
		Size: 18.3 MB (18336769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363aad0dd5ed11b8dff8be9dcf3c05c4d4bd0581e7ad1cdf0602210342a96500`  
		Last Modified: Mon, 08 Sep 2025 23:19:40 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9acf1d5fbecd9e151ce21fc93d04afd7c61699106e7c8db4dcf83988cbe351`  
		Last Modified: Mon, 08 Sep 2025 23:19:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:ce17fbeb6da00fbde71f92b66345aa42a468bdb1206f6874f4a2941b79d46665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daba63c065a6ad9f63e638d2afc1d9ccb9a84ffa384ffcf0e8fcae10e07350b`

```dockerfile
```

-	Layers:
	-	`sha256:29872436d95b2a44e130f39c4eb66751e317c25f2b99717bb45aad3c290c26c2`  
		Last Modified: Mon, 08 Sep 2025 23:20:45 GMT  
		Size: 4.6 MB (4592768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1578cdd304420775145399271ffd82a70544e44ddc89eb119fe1b8d0d1923752`  
		Last Modified: Mon, 08 Sep 2025 23:20:46 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:da0e9566f4396db64f4a10c141aa311a00e82e645a111a1dfd56fef9ae951ad6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b97abefab7c7106fa6057621105e848aba41fd0fdb66b6308cc19039e0f761af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23128773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0df6437d61edc97e7c40428bcd145e6c905f99ee52efa098c794df8b96d6fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Thu, 03 Jul 2025 17:46:22 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534473baf39867ec5bacb5b8f2dc27ca789adb0d6f5fbee9c526fd7582f74959`  
		Last Modified: Tue, 15 Jul 2025 20:46:31 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bcd2156d45512bffb3f8aed479e13cecf5497cfbdd271bf851394a230abfea`  
		Last Modified: Tue, 15 Jul 2025 20:46:35 GMT  
		Size: 1.2 MB (1217659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b5c54da1913bc9bd5fc8124eafa7a8c8f57f026ee58f1948c504a819c79036`  
		Last Modified: Wed, 16 Jul 2025 09:12:05 GMT  
		Size: 18.3 MB (18289792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f43f192a2907754b4580c627761a17b4d5fd3e9bc2370919e47a83ce5eab4f6`  
		Last Modified: Tue, 15 Jul 2025 20:46:42 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa30d907170438ad6034d2e4faf3f8b608c62ec4b9d707dc1a2f60e4c560af3`  
		Last Modified: Tue, 15 Jul 2025 20:46:45 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3458f6afa2a4a70430ee4d7a3c5682dbfa8354876088a8d71c58bc6991b02912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.2 KB (691180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c815488ae91a2477e44cfc251cb00dd41a06ef927139f45efa46d6a5ac21d49`

```dockerfile
```

-	Layers:
	-	`sha256:57fa4cb8fc63ded948da28214d2a3984e90a09977c0e9409ffe4c531a86a3365`  
		Last Modified: Tue, 15 Jul 2025 23:20:38 GMT  
		Size: 676.2 KB (676171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6eec4c085d29116bfc347eb69f2f47e22dce4c3d9030a67bcfbfd606021da40`  
		Last Modified: Tue, 15 Jul 2025 23:20:38 GMT  
		Size: 15.0 KB (15009 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8`

```console
$ docker pull influxdb@sha256:1fe652fe46cc9250b1e01f302a4b079c60b263fa7b6c24f0847ce062dbd1bf88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:b350726c3fa501f65b7a94dcf8599a4faca41a61ffb707b453d1d9972ce89049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116163525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e190497e82423991d556cb21eb08f429571a5db54f5376231609a036ee6ab3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 28 Aug 2025 18:37:27 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
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
	-	`sha256:6243170e31ed9b045fc79e3e137b2a451a688c910ecfa7266e4bc56fdabf5681`  
		Last Modified: Mon, 08 Sep 2025 23:20:57 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c571a95dfffaa44436c23181ed3f5c848caa135c53a727fc4a497fe9708cfc`  
		Last Modified: Mon, 08 Sep 2025 23:21:00 GMT  
		Size: 43.7 MB (43654007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d66ea1e5ddf6b93ae0e22ff9b88095e4a2ef8b90c708d20ff8b069a19e08da2`  
		Last Modified: Mon, 08 Sep 2025 23:20:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f32ae8336dbf6b6a3e4a297dd6ea5d84cf58b7a6704afebcb3ec80a26cfbdd3`  
		Last Modified: Mon, 08 Sep 2025 23:20:59 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f293d4b8a1df9bcb5ace025df87993ee45ab4760c39c324aebce3250daa6779`  
		Last Modified: Mon, 08 Sep 2025 23:21:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:eb5c3673b02b7fdc3798525c4b3badfd45a9c4a0fdf2caa6a603b699fd68cdbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2098eb33abddd4daa72dcfdbe42fbe6f592972ca6118ce4e597550e33d1e753a`

```dockerfile
```

-	Layers:
	-	`sha256:3947587988ff4cf36ee42dfa966dfdef9e0a873676c0f644aaab35483c21ed3d`  
		Last Modified: Mon, 08 Sep 2025 23:20:37 GMT  
		Size: 5.1 MB (5078620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04021c33d71220d3d1df1d49293eec7c706e47d626e86bf94012833e5c7acfbd`  
		Last Modified: Mon, 08 Sep 2025 23:20:38 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d6d0563b20c9093cfbc2fe57c1d58290d4640725b04480d3ab012d67e44d4df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113077045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a6729d3504ca5ceb6d85bddd148f07093398e3bdb5b2d06a1b50b0e2045de2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 28 Aug 2025 18:37:27 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
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
	-	`sha256:97955a0cb7e8a0ceb18d8e014531ce1de6577a12664fe21d09e22d665d6dfdb9`  
		Last Modified: Tue, 09 Sep 2025 02:14:56 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aba530552581631f28f3b47d469ecb50292deb4a1160693e543a6d2c6a78b5`  
		Last Modified: Tue, 09 Sep 2025 05:20:28 GMT  
		Size: 41.1 MB (41120326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc12198b70b02d4eba057245b8eafe1367e6c670e5a6b96609dc2ab2632b4ff3`  
		Last Modified: Tue, 09 Sep 2025 02:14:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a707539214d47736871a6e92b02f803f243ea9d1eed1ee899b7ba88500f510`  
		Last Modified: Tue, 09 Sep 2025 02:14:57 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78464ae95a9e74070a124a94124feba1d20bd5bc608764a64813a25887159fe0`  
		Last Modified: Tue, 09 Sep 2025 02:14:56 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:3d85c2244f6342cf6a320532621270ba70230f30ab2bb0706e3b91ed8ca67db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cb108da2bf97cf468b18420762b1ae6cc610d3d834dc9f1cf10963745c1d39`

```dockerfile
```

-	Layers:
	-	`sha256:931b097db463802416e1dc731eb5e3492610263743efb18892becbbf7f96a733`  
		Last Modified: Tue, 09 Sep 2025 05:20:23 GMT  
		Size: 5.1 MB (5078085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff0fe5382aba43f5a674887506c2143e0b09cc7b98179017a94956f57adfbc1`  
		Last Modified: Tue, 09 Sep 2025 05:20:24 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-alpine`

```console
$ docker pull influxdb@sha256:138f19e5685514f3b91dee1b5a53ed6b77134c7356cd0384a7781c902c01c375
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c02e7eb95cd84a5eff5db97efcbd65fc2e3f61e620a5cc7c9a481a3cd12c8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42909082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7f02263b1f21a109432dc16aeadc1c6e1f2243aee678f111997f9faee582cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 03 Jul 2025 17:46:22 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cdf703c988b90a506e51b1a7870074ca976afe3cf8ba4ffefc1a9a3802bc58`  
		Last Modified: Tue, 15 Jul 2025 21:34:26 GMT  
		Size: 1.2 MB (1217662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f4ac331105e966636f8e81b8c44ecac0cdaac1dc1b9f53957cd6d191311b4e`  
		Last Modified: Tue, 15 Jul 2025 23:20:31 GMT  
		Size: 38.1 MB (38068228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a8ce52868a0b7dd9ceb9a61801b5c8aa1f35a5053b5d15761c809b00c29e14`  
		Last Modified: Tue, 15 Jul 2025 21:34:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6892154e596bd1ad278ceac48678c52c980e18fe9dfbd8b6a0d8c3d0884ea5a4`  
		Last Modified: Tue, 15 Jul 2025 21:34:27 GMT  
		Size: 999.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f35936e07afbbc0e42db14df940027b31b3ae625cf0732ded86bf1410764d18`  
		Last Modified: Tue, 15 Jul 2025 21:34:28 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26572fb2dd53dcc1431ee3d783cfae93431609dd1b481f6768e467d50d6f67ac`  
		Last Modified: Tue, 15 Jul 2025 21:34:34 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:15a79bbccbd314af27645833571b31a9aaf700233f748b52cc04de17e487ed8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.7 KB (757742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0963f3c5cedd0b4b3c2cd96f8d92b87bc687a9317881f4489a106c409b901a1e`

```dockerfile
```

-	Layers:
	-	`sha256:4e619d1dac411fcf2dac09dfcddc02b9ebd0a239d75e99ced83817d81966fb20`  
		Last Modified: Tue, 15 Jul 2025 23:20:30 GMT  
		Size: 739.9 KB (739869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aac0057bc38790b1784893af404060f691942579fc819af2761bebc99d3bce4`  
		Last Modified: Tue, 15 Jul 2025 23:20:30 GMT  
		Size: 17.9 KB (17873 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:9cd9ba2e4569693ebccf6cde53197a4e56350586974cbab331772bc4d7b179f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40933009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ad4af985e8f2af1242da5ec46fd4b9926ec0765a37054c1b92787997db839f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 03 Jul 2025 17:46:22 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107448bacbe733297b040236d890a68ba7de0745b30fd384b8d23263a83daefd`  
		Last Modified: Wed, 16 Jul 2025 00:17:01 GMT  
		Size: 1.3 MB (1296536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36431ddb424d34cbad9aa722f22b084252d11fe870db747bfac0e9a476f0134e`  
		Last Modified: Wed, 16 Jul 2025 00:17:06 GMT  
		Size: 35.5 MB (35545387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2746309bcef96c794924b818e9e9b26688d79244496bbb7e371fed1c51e83718`  
		Last Modified: Wed, 16 Jul 2025 00:17:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e74d66f0ddeb59deeb029d729da782f64701fa4543bbb236079461fd4090c1`  
		Last Modified: Wed, 16 Jul 2025 00:17:01 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166127b6c6a42d743c597bb6077eb80b64eb236d8a9071451a2b7616e351140d`  
		Last Modified: Wed, 16 Jul 2025 00:17:01 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46aa7dbe029fbf3145fbbc8d015fbbe445a1bc3bd55476152d55f3745f41d54`  
		Last Modified: Wed, 16 Jul 2025 00:17:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e6f8506d051c4f2b9f28242b342b63df77acc1b058111515374711e1e3455714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.1 KB (757083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eade6518476c5429dd8828f274005e1541cd8af980349da19829ecedffd29d`

```dockerfile
```

-	Layers:
	-	`sha256:851289b34c3ef45e1406cdbaa86c664d47f46980df311c1a8b9dbc38a53a134a`  
		Last Modified: Wed, 16 Jul 2025 02:20:24 GMT  
		Size: 739.1 KB (739096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854f9fc20d333c0b08bda6757b097db1abb4fe6b1782d627613e8bcb56c27f24`  
		Last Modified: Wed, 16 Jul 2025 02:20:25 GMT  
		Size: 18.0 KB (17987 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-data`

```console
$ docker pull influxdb@sha256:d57a2049ec438f6058e0c7acde28cd25f0943739c8bec98c08aebe3765215e47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f51d91478c0b5c8dae1aae6ca557bde6c8617216edf9adbcfd52ac19d640eebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111689695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8d39ebc6b6384182e6e89491fa430c0ff0c39251c8867a8d8108dca7280f91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Thu, 28 Aug 2025 18:37:27 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
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
	-	`sha256:2a19dfb20162d87acc977ac67c19ec82d232c4d1b259e73326fd0d996587f1dd`  
		Last Modified: Mon, 08 Sep 2025 22:38:31 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82f6677cbf9b0a84d343e202f04fbdb1edd600a1d71a9cdaccbfb95cbd4aa81`  
		Last Modified: Mon, 08 Sep 2025 21:57:40 GMT  
		Size: 39.2 MB (39179533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6669a805a8323e4145d710825da67e04134cf2ddd2c77f50d07279f7905da86`  
		Last Modified: Mon, 08 Sep 2025 22:38:34 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9461e8807654eaae8e6739c70c33babd6360fe350a3fd24cf8db5323741fc58d`  
		Last Modified: Mon, 08 Sep 2025 22:38:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3b75326d321c67f3815a0b4fa501147074478dabc930be6bb12fe7d337d83f`  
		Last Modified: Mon, 08 Sep 2025 22:38:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:98adbf06ee5245ee11ccb9e39385e2d543a70fb805964bb06fc887f8871f77af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4682505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff600f27c3d61fc562cbc49d041d5933e457ea3bc9e45e8369259e54601c6b26`

```dockerfile
```

-	Layers:
	-	`sha256:ccf2f8886ff5216ec2b37d70a8ba7df4296e7c495a32667ea0c96f85d5120324`  
		Last Modified: Mon, 08 Sep 2025 23:20:42 GMT  
		Size: 4.7 MB (4667797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ee73478ec9d36d44f5758868a06aa8af164cc1a8f3d3d594633d97068079fcc`  
		Last Modified: Mon, 08 Sep 2025 23:20:43 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-data-alpine`

```console
$ docker pull influxdb@sha256:381bd28215770143c72eab8ca2170a3d31e8e88acc3be7c9d198804729414956
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:96b59b101b2a5e451f5f947c04f3e46378c9a3681f41df121bc4dd3eb785d389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43963829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9353a878a5beb3047c128eb9d9149a950e388e5c8b2f0e3a072ff162d9184579`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Thu, 03 Jul 2025 17:46:22 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7cd59a170b5fff4759056f3021cd3a0f8b8b93fd86f3b540f889da699918c6`  
		Last Modified: Tue, 15 Jul 2025 20:46:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c28885a79e009e286e4f9a293cba3159388662f0e7348a60b74ccf232bec4e`  
		Last Modified: Tue, 15 Jul 2025 20:46:50 GMT  
		Size: 1.2 MB (1217668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e9d594775205c1ee1832d8b017c91770b09b6aadfc1ebb9c31d5587fd21a68`  
		Last Modified: Thu, 17 Jul 2025 04:06:22 GMT  
		Size: 39.1 MB (39123633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b71615bfecfb828537f7c993fe93ff50bf019853db7ec1c27609e5df5eeda8`  
		Last Modified: Tue, 15 Jul 2025 20:47:13 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e728fa1ce435bbdea26982955e9b3fefdd18e8c6ad39f5e0ffeba2525a6a49a`  
		Last Modified: Tue, 15 Jul 2025 20:47:16 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4ebfff5a877c2cc2c5b880287f92b8f3c3ec679ec7be2017f0ef35d79c1aaf`  
		Last Modified: Tue, 15 Jul 2025 20:47:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c66ae295b7d7a33b393f6dc9d9c9fe3a94afd550d714d211ec06980498a33908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **767.1 KB (767053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42347b07372c3c71c03691eb26b8eed6f42a77e1bef4fc5c6670e676bc414b4a`

```dockerfile
```

-	Layers:
	-	`sha256:6b19dbadcc4e5898d140eeff835d6e705d6a4ccc08aac69768d773dfc892febd`  
		Last Modified: Tue, 15 Jul 2025 23:20:33 GMT  
		Size: 750.4 KB (750414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f398e7228caee2c145d1f269d0f5839080d1d0d6ccbb809d4fc8b5c7fd2784b`  
		Last Modified: Tue, 15 Jul 2025 23:20:34 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-meta`

```console
$ docker pull influxdb@sha256:1c198519bf1b1bded210e6f870d22354b7956fbb8d671fd33bfc7f0e2e2486d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:6b46d915b14f49d0e8cd1c6d30f3b308728246f98438c0ca069c439789c15727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90845710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216dda4bb2297e769c2c36d9cdf09b20a8e7880d96b984850acb78e3a24b9a9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Thu, 28 Aug 2025 18:37:27 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
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
	-	`sha256:7c74cb8773783cd77f8754eaeb3e502846c92918abae8c3e3bf4e55337648ac4`  
		Last Modified: Mon, 08 Sep 2025 23:19:40 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39f58484a4d9d46791fa08eea720f2404c5fc437eee770436c4801dfe04f55b`  
		Last Modified: Mon, 08 Sep 2025 21:57:32 GMT  
		Size: 18.3 MB (18336769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363aad0dd5ed11b8dff8be9dcf3c05c4d4bd0581e7ad1cdf0602210342a96500`  
		Last Modified: Mon, 08 Sep 2025 23:19:40 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9acf1d5fbecd9e151ce21fc93d04afd7c61699106e7c8db4dcf83988cbe351`  
		Last Modified: Mon, 08 Sep 2025 23:19:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:ce17fbeb6da00fbde71f92b66345aa42a468bdb1206f6874f4a2941b79d46665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daba63c065a6ad9f63e638d2afc1d9ccb9a84ffa384ffcf0e8fcae10e07350b`

```dockerfile
```

-	Layers:
	-	`sha256:29872436d95b2a44e130f39c4eb66751e317c25f2b99717bb45aad3c290c26c2`  
		Last Modified: Mon, 08 Sep 2025 23:20:45 GMT  
		Size: 4.6 MB (4592768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1578cdd304420775145399271ffd82a70544e44ddc89eb119fe1b8d0d1923752`  
		Last Modified: Mon, 08 Sep 2025 23:20:46 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-meta-alpine`

```console
$ docker pull influxdb@sha256:da0e9566f4396db64f4a10c141aa311a00e82e645a111a1dfd56fef9ae951ad6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b97abefab7c7106fa6057621105e848aba41fd0fdb66b6308cc19039e0f761af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23128773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0df6437d61edc97e7c40428bcd145e6c905f99ee52efa098c794df8b96d6fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Thu, 03 Jul 2025 17:46:22 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534473baf39867ec5bacb5b8f2dc27ca789adb0d6f5fbee9c526fd7582f74959`  
		Last Modified: Tue, 15 Jul 2025 20:46:31 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bcd2156d45512bffb3f8aed479e13cecf5497cfbdd271bf851394a230abfea`  
		Last Modified: Tue, 15 Jul 2025 20:46:35 GMT  
		Size: 1.2 MB (1217659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b5c54da1913bc9bd5fc8124eafa7a8c8f57f026ee58f1948c504a819c79036`  
		Last Modified: Wed, 16 Jul 2025 09:12:05 GMT  
		Size: 18.3 MB (18289792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f43f192a2907754b4580c627761a17b4d5fd3e9bc2370919e47a83ce5eab4f6`  
		Last Modified: Tue, 15 Jul 2025 20:46:42 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa30d907170438ad6034d2e4faf3f8b608c62ec4b9d707dc1a2f60e4c560af3`  
		Last Modified: Tue, 15 Jul 2025 20:46:45 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3458f6afa2a4a70430ee4d7a3c5682dbfa8354876088a8d71c58bc6991b02912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.2 KB (691180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c815488ae91a2477e44cfc251cb00dd41a06ef927139f45efa46d6a5ac21d49`

```dockerfile
```

-	Layers:
	-	`sha256:57fa4cb8fc63ded948da28214d2a3984e90a09977c0e9409ffe4c531a86a3365`  
		Last Modified: Tue, 15 Jul 2025 23:20:38 GMT  
		Size: 676.2 KB (676171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6eec4c085d29116bfc347eb69f2f47e22dce4c3d9030a67bcfbfd606021da40`  
		Last Modified: Tue, 15 Jul 2025 23:20:38 GMT  
		Size: 15.0 KB (15009 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:23bc959dcb97f85e1fbc3a739805203eb3bcb779afede002cb205a37e14442bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:24439270fc10f3ad0aba36141f7d7d52d34496276ee0764fc8b687c10a7ff06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157220044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f693f2f6769e614b3926cb90bdd5a735f5934041e9aea399e321b720263ac6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 28 Aug 2025 18:37:27 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV GOSU_VER=1.16
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxd"]
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 28 Aug 2025 18:37:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62782c24a9fe40dad4bf8cdf7cf711a21c3430aef8b8568cfe22075c1b21d1d8`  
		Last Modified: Mon, 08 Sep 2025 22:09:55 GMT  
		Size: 9.8 MB (9796155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf10daca95d762897f2ecf3cc91f43c962f253a5d0850c712901f95ebc6cb860`  
		Last Modified: Mon, 08 Sep 2025 22:10:05 GMT  
		Size: 6.2 MB (6156969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69db941034b2f17178f1dee377fadcb052a3ba542951e2934630396c6ce38fff`  
		Last Modified: Mon, 08 Sep 2025 21:47:10 GMT  
		Size: 3.2 KB (3223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61ffd991d4118be05db267ed6b812395d53627ef54ab190548986977c47c91e`  
		Last Modified: Mon, 08 Sep 2025 21:47:14 GMT  
		Size: 1.0 MB (1012032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f089b773084833b051906a5cfc60dcfef719bccf6b472ff9ee8d313cef8beb95`  
		Last Modified: Mon, 08 Sep 2025 22:10:04 GMT  
		Size: 100.2 MB (100242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac18979dc6ef4c7cd439951f425f1285ef162444373e71cc329baeb1a239d03`  
		Last Modified: Mon, 08 Sep 2025 22:09:57 GMT  
		Size: 11.8 MB (11773668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea94f0bff41ed9285df20bae80b5eb0dba18abbbd5c689d03f539fc90c36b87`  
		Last Modified: Mon, 08 Sep 2025 21:47:20 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3fb6e72c97e5f0b88c165d61c791108d570d28a19b3fc8bf936d8968909afc`  
		Last Modified: Mon, 08 Sep 2025 21:47:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be06895ccb48e141a348befe63f5e6e265e07f3499e0ae5adfe23d28041ddfd`  
		Last Modified: Mon, 08 Sep 2025 21:47:28 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:87d7fb0a7704b203b9ba3ae556b4fe1579ddf9b0cb50a155d55bf01f012c2042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26666dc8233778fa995b2a30eb768571b0cc44154d2e843bb2551c63524aa458`

```dockerfile
```

-	Layers:
	-	`sha256:48309e5b7a6aa05829612b0ee07f5d5c51a876dd8b8f365132bec7bc483e29da`  
		Last Modified: Mon, 08 Sep 2025 23:21:00 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6155ac10102e3b3601478f687ab5fd30a0dbb728df25a23a218fd0339ed6ecf`  
		Last Modified: Mon, 08 Sep 2025 23:21:01 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4e2d08ccb2c6770b9bff4c99761464ae15a730142cf0aeef319b90e00bd5e195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151605052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90938dcb7ac0d05de4a3bba4fbd2f504535461956d40d5a8899111aa4bd5e3c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 28 Aug 2025 18:37:27 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV GOSU_VER=1.16
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxd"]
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 28 Aug 2025 18:37:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353a7ea5fa5c6bb8b5a3d2b2c549b5e78bcc3b3630e1425b9e2b5060f03b27c8`  
		Last Modified: Mon, 08 Sep 2025 22:03:59 GMT  
		Size: 9.6 MB (9626321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008c23392941f0ac573975e38eea9ca2f9a0a8d3eb1357b62cb7e185b995ddda`  
		Last Modified: Mon, 08 Sep 2025 22:03:58 GMT  
		Size: 5.8 MB (5790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a89d0e27e07debed5bf9f5500a2b514ded8d886adc7bd972274bd0cabe12b53`  
		Last Modified: Mon, 08 Sep 2025 22:04:00 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0565416d429978172f33f8473916faadb6f12a060860d0273296d7ac2e62ef9`  
		Last Modified: Mon, 08 Sep 2025 22:04:00 GMT  
		Size: 938.9 KB (938872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b6049e0c4a3b07a790ade738d82f9596efcfcaf637d1333684f32d33dbe6f`  
		Last Modified: Mon, 08 Sep 2025 22:04:07 GMT  
		Size: 96.0 MB (96038383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c066f3f4b5389cda111c7878c0c65a2d0100653973ecb6bf54a1855adade6ec5`  
		Last Modified: Mon, 08 Sep 2025 22:04:03 GMT  
		Size: 11.1 MB (11099009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5133689e87cf1b79291ba55551327073e4d99a4e804d53a6036bb8b9e5a3163`  
		Last Modified: Mon, 08 Sep 2025 22:04:02 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f59bf53b4c222d5ca0dc84ed4b20b4928d85383181f31cd86e7fcaf7fc8b697`  
		Last Modified: Mon, 08 Sep 2025 22:04:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5fb088dd891a90819393b8659ba6044dd6dddc731bf8e3241fa29084ad1164`  
		Last Modified: Mon, 08 Sep 2025 22:04:05 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:5bf7cd22c06c8e4195d8131ee52bfa54009d01e75ab39be142892fc14bb0a7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6a28f3d1e3ff56b67cab1bc08b8057940cbd92f6912df2fa2bbb626876aa35`

```dockerfile
```

-	Layers:
	-	`sha256:2ff50b519056e71fa024bf8d57a9b4667d37e331e5d809b20b2a0c6ee63c4a13`  
		Last Modified: Mon, 08 Sep 2025 23:21:05 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22aacdacdbb80e9c7f62beb9c6ef09e69eb0ac8a92f104d1aa2fa9c35bf0891`  
		Last Modified: Mon, 08 Sep 2025 23:21:06 GMT  
		Size: 33.7 KB (33718 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:d948cd7aa274696d76ccc3f7ef732180d9f9a4229aace3cf68ae008693665137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5ab58e6acde4a641694f7a2e6671a9f39921f3b8200e7cb04153599ff24a0171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81511579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fcb7b71c691969ff5b9884bf92ef34f16ca26efabcfb7fbd6d0ada332fe1458`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 03 Jul 2025 17:46:22 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41588b948a36335f02b1fe372411528fc71bf105e403c9b8476eaed4bc61b296`  
		Last Modified: Tue, 15 Jul 2025 20:47:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176c40e86352d8732707283812cf31b4cb48410b4d43bd9a1ea799b969178e28`  
		Last Modified: Tue, 15 Jul 2025 23:20:58 GMT  
		Size: 9.8 MB (9819933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124accecbf9a5d3fa58778cf7d727740b1808d84760e163ecbfe05c76fde911c`  
		Last Modified: Tue, 15 Jul 2025 23:20:58 GMT  
		Size: 6.2 MB (6156984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02be05aac4069c435b4c30f7102f4fef9d496612908c506d00a74fe121e992b`  
		Last Modified: Tue, 15 Jul 2025 20:47:43 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54aba977cca3a9f384b93f852720b3fdb29821d9601ec5402b7fabb7b84ed188`  
		Last Modified: Tue, 15 Jul 2025 23:21:07 GMT  
		Size: 50.1 MB (50115466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e18b3dde9d2ebba50fb26deb3e132dbff7bce833d3dec715b997305f4b7ead`  
		Last Modified: Tue, 15 Jul 2025 23:21:00 GMT  
		Size: 11.8 MB (11773676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a605a3944855fed4b0dc37407f21364b863d736d62e512592c17f37614f634b`  
		Last Modified: Tue, 15 Jul 2025 20:47:48 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3144ed5ee0ead4cb9ab07f97753eff4055313e54d6469a9a22feb04cc627f5b6`  
		Last Modified: Tue, 15 Jul 2025 20:47:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05126e91032baacdbb215f10aae69bd77e06da4add32161c42104ad83744d068`  
		Last Modified: Tue, 15 Jul 2025 20:47:55 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bce540c47d1075fe3bc1f3a18410f096d9a73701106a04b8724a850baa2a7e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 KB (941372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9814dc0d960e1dd48ab16ce3799261d16c65d82603d5e8c7d98111eeac6cb7`

```dockerfile
```

-	Layers:
	-	`sha256:6d325d7ce69647356cfcce291f65ab689996946f197ffff1db072b832f421271`  
		Last Modified: Tue, 15 Jul 2025 23:20:47 GMT  
		Size: 910.6 KB (910603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba6a4bbacf5ac36dfae6df2b86429b3103a25fc72709e829c3ba8afe8cf53a8`  
		Last Modified: Tue, 15 Jul 2025 23:20:48 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:328a4a0ffd4b2631ebbf3b75b62e14f3ddee93b48bca78be21da8f0fa818a823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78683906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d78e27ffcd6dd1fce93b95dcaddaa6c654dc6e7e6ee859bafc1df18b61481f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 03 Jul 2025 17:46:22 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600bb37154aec80b9f15e982c92a4e37ba42feeb4cc42826f6add6b7fb79ad89`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1672beef7b2cc4b76db6451487d605bebd392e9d0f8c39b48d43cd4f0aba306`  
		Last Modified: Wed, 16 Jul 2025 00:17:26 GMT  
		Size: 9.8 MB (9783360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9529e7bf79faa4c179f30c08b6771dac030c31ecdd63018c7651338afdae27e3`  
		Last Modified: Wed, 16 Jul 2025 00:17:26 GMT  
		Size: 5.8 MB (5790433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e0f93130bfcea152418034fcf70f62c1b31b5edcf475d536ee84548219f449`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d60bf4032b74fcc73c1c56e254540e8960145dace3efcea4bd97297bd88523`  
		Last Modified: Wed, 16 Jul 2025 00:17:30 GMT  
		Size: 48.0 MB (48016245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084d0c42d1d38a2397dde3e42086f8db8b36e263f884f0ce8262e26b056739eb`  
		Last Modified: Wed, 16 Jul 2025 00:17:27 GMT  
		Size: 11.1 MB (11098981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6bb2ad4fede2ef39df25c988f059baf0bb037f19a4120a3d05e07cc1bda614`  
		Last Modified: Wed, 16 Jul 2025 00:17:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9162549b851b3e4b3fa90cbc20f18519037f21bc774bb33be16d4d12d3c8d7`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1c7cb76b0374befb4a7b810686ef1d646abcb15428a55630c40d2bb6535310`  
		Last Modified: Wed, 16 Jul 2025 00:17:25 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cd7717fcd61869be57b993a9722525fd3640ca6c52d336aff4389c12cfa83d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.8 KB (940817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ba9a3b2a06597910ffc721dcc16534874f8b6068066a163f2298bf924c6ca2`

```dockerfile
```

-	Layers:
	-	`sha256:2e4eaed119ab9bd7fb9ec406598f4850075f76a7dc60d7ae0ec0cd6ad73111a4`  
		Last Modified: Wed, 16 Jul 2025 02:20:35 GMT  
		Size: 909.9 KB (909854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98b6129a43b1892d4bc0921a75ca680f9d9266e51b357532a467764c49c8f244`  
		Last Modified: Wed, 16 Jul 2025 02:20:36 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:23bc959dcb97f85e1fbc3a739805203eb3bcb779afede002cb205a37e14442bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:24439270fc10f3ad0aba36141f7d7d52d34496276ee0764fc8b687c10a7ff06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157220044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f693f2f6769e614b3926cb90bdd5a735f5934041e9aea399e321b720263ac6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 28 Aug 2025 18:37:27 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV GOSU_VER=1.16
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxd"]
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 28 Aug 2025 18:37:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62782c24a9fe40dad4bf8cdf7cf711a21c3430aef8b8568cfe22075c1b21d1d8`  
		Last Modified: Mon, 08 Sep 2025 22:09:55 GMT  
		Size: 9.8 MB (9796155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf10daca95d762897f2ecf3cc91f43c962f253a5d0850c712901f95ebc6cb860`  
		Last Modified: Mon, 08 Sep 2025 22:10:05 GMT  
		Size: 6.2 MB (6156969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69db941034b2f17178f1dee377fadcb052a3ba542951e2934630396c6ce38fff`  
		Last Modified: Mon, 08 Sep 2025 21:47:10 GMT  
		Size: 3.2 KB (3223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61ffd991d4118be05db267ed6b812395d53627ef54ab190548986977c47c91e`  
		Last Modified: Mon, 08 Sep 2025 21:47:14 GMT  
		Size: 1.0 MB (1012032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f089b773084833b051906a5cfc60dcfef719bccf6b472ff9ee8d313cef8beb95`  
		Last Modified: Mon, 08 Sep 2025 22:10:04 GMT  
		Size: 100.2 MB (100242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac18979dc6ef4c7cd439951f425f1285ef162444373e71cc329baeb1a239d03`  
		Last Modified: Mon, 08 Sep 2025 22:09:57 GMT  
		Size: 11.8 MB (11773668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea94f0bff41ed9285df20bae80b5eb0dba18abbbd5c689d03f539fc90c36b87`  
		Last Modified: Mon, 08 Sep 2025 21:47:20 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3fb6e72c97e5f0b88c165d61c791108d570d28a19b3fc8bf936d8968909afc`  
		Last Modified: Mon, 08 Sep 2025 21:47:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be06895ccb48e141a348befe63f5e6e265e07f3499e0ae5adfe23d28041ddfd`  
		Last Modified: Mon, 08 Sep 2025 21:47:28 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:87d7fb0a7704b203b9ba3ae556b4fe1579ddf9b0cb50a155d55bf01f012c2042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26666dc8233778fa995b2a30eb768571b0cc44154d2e843bb2551c63524aa458`

```dockerfile
```

-	Layers:
	-	`sha256:48309e5b7a6aa05829612b0ee07f5d5c51a876dd8b8f365132bec7bc483e29da`  
		Last Modified: Mon, 08 Sep 2025 23:21:00 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6155ac10102e3b3601478f687ab5fd30a0dbb728df25a23a218fd0339ed6ecf`  
		Last Modified: Mon, 08 Sep 2025 23:21:01 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4e2d08ccb2c6770b9bff4c99761464ae15a730142cf0aeef319b90e00bd5e195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151605052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90938dcb7ac0d05de4a3bba4fbd2f504535461956d40d5a8899111aa4bd5e3c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 28 Aug 2025 18:37:27 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV GOSU_VER=1.16
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxd"]
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 28 Aug 2025 18:37:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353a7ea5fa5c6bb8b5a3d2b2c549b5e78bcc3b3630e1425b9e2b5060f03b27c8`  
		Last Modified: Mon, 08 Sep 2025 22:03:59 GMT  
		Size: 9.6 MB (9626321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008c23392941f0ac573975e38eea9ca2f9a0a8d3eb1357b62cb7e185b995ddda`  
		Last Modified: Mon, 08 Sep 2025 22:03:58 GMT  
		Size: 5.8 MB (5790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a89d0e27e07debed5bf9f5500a2b514ded8d886adc7bd972274bd0cabe12b53`  
		Last Modified: Mon, 08 Sep 2025 22:04:00 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0565416d429978172f33f8473916faadb6f12a060860d0273296d7ac2e62ef9`  
		Last Modified: Mon, 08 Sep 2025 22:04:00 GMT  
		Size: 938.9 KB (938872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b6049e0c4a3b07a790ade738d82f9596efcfcaf637d1333684f32d33dbe6f`  
		Last Modified: Mon, 08 Sep 2025 22:04:07 GMT  
		Size: 96.0 MB (96038383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c066f3f4b5389cda111c7878c0c65a2d0100653973ecb6bf54a1855adade6ec5`  
		Last Modified: Mon, 08 Sep 2025 22:04:03 GMT  
		Size: 11.1 MB (11099009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5133689e87cf1b79291ba55551327073e4d99a4e804d53a6036bb8b9e5a3163`  
		Last Modified: Mon, 08 Sep 2025 22:04:02 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f59bf53b4c222d5ca0dc84ed4b20b4928d85383181f31cd86e7fcaf7fc8b697`  
		Last Modified: Mon, 08 Sep 2025 22:04:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5fb088dd891a90819393b8659ba6044dd6dddc731bf8e3241fa29084ad1164`  
		Last Modified: Mon, 08 Sep 2025 22:04:05 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:5bf7cd22c06c8e4195d8131ee52bfa54009d01e75ab39be142892fc14bb0a7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6a28f3d1e3ff56b67cab1bc08b8057940cbd92f6912df2fa2bbb626876aa35`

```dockerfile
```

-	Layers:
	-	`sha256:2ff50b519056e71fa024bf8d57a9b4667d37e331e5d809b20b2a0c6ee63c4a13`  
		Last Modified: Mon, 08 Sep 2025 23:21:05 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22aacdacdbb80e9c7f62beb9c6ef09e69eb0ac8a92f104d1aa2fa9c35bf0891`  
		Last Modified: Mon, 08 Sep 2025 23:21:06 GMT  
		Size: 33.7 KB (33718 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:d948cd7aa274696d76ccc3f7ef732180d9f9a4229aace3cf68ae008693665137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5ab58e6acde4a641694f7a2e6671a9f39921f3b8200e7cb04153599ff24a0171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81511579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fcb7b71c691969ff5b9884bf92ef34f16ca26efabcfb7fbd6d0ada332fe1458`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 03 Jul 2025 17:46:22 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41588b948a36335f02b1fe372411528fc71bf105e403c9b8476eaed4bc61b296`  
		Last Modified: Tue, 15 Jul 2025 20:47:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176c40e86352d8732707283812cf31b4cb48410b4d43bd9a1ea799b969178e28`  
		Last Modified: Tue, 15 Jul 2025 23:20:58 GMT  
		Size: 9.8 MB (9819933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124accecbf9a5d3fa58778cf7d727740b1808d84760e163ecbfe05c76fde911c`  
		Last Modified: Tue, 15 Jul 2025 23:20:58 GMT  
		Size: 6.2 MB (6156984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02be05aac4069c435b4c30f7102f4fef9d496612908c506d00a74fe121e992b`  
		Last Modified: Tue, 15 Jul 2025 20:47:43 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54aba977cca3a9f384b93f852720b3fdb29821d9601ec5402b7fabb7b84ed188`  
		Last Modified: Tue, 15 Jul 2025 23:21:07 GMT  
		Size: 50.1 MB (50115466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e18b3dde9d2ebba50fb26deb3e132dbff7bce833d3dec715b997305f4b7ead`  
		Last Modified: Tue, 15 Jul 2025 23:21:00 GMT  
		Size: 11.8 MB (11773676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a605a3944855fed4b0dc37407f21364b863d736d62e512592c17f37614f634b`  
		Last Modified: Tue, 15 Jul 2025 20:47:48 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3144ed5ee0ead4cb9ab07f97753eff4055313e54d6469a9a22feb04cc627f5b6`  
		Last Modified: Tue, 15 Jul 2025 20:47:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05126e91032baacdbb215f10aae69bd77e06da4add32161c42104ad83744d068`  
		Last Modified: Tue, 15 Jul 2025 20:47:55 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bce540c47d1075fe3bc1f3a18410f096d9a73701106a04b8724a850baa2a7e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 KB (941372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9814dc0d960e1dd48ab16ce3799261d16c65d82603d5e8c7d98111eeac6cb7`

```dockerfile
```

-	Layers:
	-	`sha256:6d325d7ce69647356cfcce291f65ab689996946f197ffff1db072b832f421271`  
		Last Modified: Tue, 15 Jul 2025 23:20:47 GMT  
		Size: 910.6 KB (910603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba6a4bbacf5ac36dfae6df2b86429b3103a25fc72709e829c3ba8afe8cf53a8`  
		Last Modified: Tue, 15 Jul 2025 23:20:48 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:328a4a0ffd4b2631ebbf3b75b62e14f3ddee93b48bca78be21da8f0fa818a823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78683906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d78e27ffcd6dd1fce93b95dcaddaa6c654dc6e7e6ee859bafc1df18b61481f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 03 Jul 2025 17:46:22 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600bb37154aec80b9f15e982c92a4e37ba42feeb4cc42826f6add6b7fb79ad89`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1672beef7b2cc4b76db6451487d605bebd392e9d0f8c39b48d43cd4f0aba306`  
		Last Modified: Wed, 16 Jul 2025 00:17:26 GMT  
		Size: 9.8 MB (9783360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9529e7bf79faa4c179f30c08b6771dac030c31ecdd63018c7651338afdae27e3`  
		Last Modified: Wed, 16 Jul 2025 00:17:26 GMT  
		Size: 5.8 MB (5790433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e0f93130bfcea152418034fcf70f62c1b31b5edcf475d536ee84548219f449`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d60bf4032b74fcc73c1c56e254540e8960145dace3efcea4bd97297bd88523`  
		Last Modified: Wed, 16 Jul 2025 00:17:30 GMT  
		Size: 48.0 MB (48016245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084d0c42d1d38a2397dde3e42086f8db8b36e263f884f0ce8262e26b056739eb`  
		Last Modified: Wed, 16 Jul 2025 00:17:27 GMT  
		Size: 11.1 MB (11098981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6bb2ad4fede2ef39df25c988f059baf0bb037f19a4120a3d05e07cc1bda614`  
		Last Modified: Wed, 16 Jul 2025 00:17:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9162549b851b3e4b3fa90cbc20f18519037f21bc774bb33be16d4d12d3c8d7`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1c7cb76b0374befb4a7b810686ef1d646abcb15428a55630c40d2bb6535310`  
		Last Modified: Wed, 16 Jul 2025 00:17:25 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cd7717fcd61869be57b993a9722525fd3640ca6c52d336aff4389c12cfa83d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.8 KB (940817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ba9a3b2a06597910ffc721dcc16534874f8b6068066a163f2298bf924c6ca2`

```dockerfile
```

-	Layers:
	-	`sha256:2e4eaed119ab9bd7fb9ec406598f4850075f76a7dc60d7ae0ec0cd6ad73111a4`  
		Last Modified: Wed, 16 Jul 2025 02:20:35 GMT  
		Size: 909.9 KB (909854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98b6129a43b1892d4bc0921a75ca680f9d9266e51b357532a467764c49c8f244`  
		Last Modified: Wed, 16 Jul 2025 02:20:36 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12`

```console
$ docker pull influxdb@sha256:23bc959dcb97f85e1fbc3a739805203eb3bcb779afede002cb205a37e14442bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:24439270fc10f3ad0aba36141f7d7d52d34496276ee0764fc8b687c10a7ff06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157220044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f693f2f6769e614b3926cb90bdd5a735f5934041e9aea399e321b720263ac6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 28 Aug 2025 18:37:27 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV GOSU_VER=1.16
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxd"]
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 28 Aug 2025 18:37:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62782c24a9fe40dad4bf8cdf7cf711a21c3430aef8b8568cfe22075c1b21d1d8`  
		Last Modified: Mon, 08 Sep 2025 22:09:55 GMT  
		Size: 9.8 MB (9796155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf10daca95d762897f2ecf3cc91f43c962f253a5d0850c712901f95ebc6cb860`  
		Last Modified: Mon, 08 Sep 2025 22:10:05 GMT  
		Size: 6.2 MB (6156969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69db941034b2f17178f1dee377fadcb052a3ba542951e2934630396c6ce38fff`  
		Last Modified: Mon, 08 Sep 2025 21:47:10 GMT  
		Size: 3.2 KB (3223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61ffd991d4118be05db267ed6b812395d53627ef54ab190548986977c47c91e`  
		Last Modified: Mon, 08 Sep 2025 21:47:14 GMT  
		Size: 1.0 MB (1012032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f089b773084833b051906a5cfc60dcfef719bccf6b472ff9ee8d313cef8beb95`  
		Last Modified: Mon, 08 Sep 2025 22:10:04 GMT  
		Size: 100.2 MB (100242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac18979dc6ef4c7cd439951f425f1285ef162444373e71cc329baeb1a239d03`  
		Last Modified: Mon, 08 Sep 2025 22:09:57 GMT  
		Size: 11.8 MB (11773668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea94f0bff41ed9285df20bae80b5eb0dba18abbbd5c689d03f539fc90c36b87`  
		Last Modified: Mon, 08 Sep 2025 21:47:20 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3fb6e72c97e5f0b88c165d61c791108d570d28a19b3fc8bf936d8968909afc`  
		Last Modified: Mon, 08 Sep 2025 21:47:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be06895ccb48e141a348befe63f5e6e265e07f3499e0ae5adfe23d28041ddfd`  
		Last Modified: Mon, 08 Sep 2025 21:47:28 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:87d7fb0a7704b203b9ba3ae556b4fe1579ddf9b0cb50a155d55bf01f012c2042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26666dc8233778fa995b2a30eb768571b0cc44154d2e843bb2551c63524aa458`

```dockerfile
```

-	Layers:
	-	`sha256:48309e5b7a6aa05829612b0ee07f5d5c51a876dd8b8f365132bec7bc483e29da`  
		Last Modified: Mon, 08 Sep 2025 23:21:00 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6155ac10102e3b3601478f687ab5fd30a0dbb728df25a23a218fd0339ed6ecf`  
		Last Modified: Mon, 08 Sep 2025 23:21:01 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4e2d08ccb2c6770b9bff4c99761464ae15a730142cf0aeef319b90e00bd5e195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151605052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90938dcb7ac0d05de4a3bba4fbd2f504535461956d40d5a8899111aa4bd5e3c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 28 Aug 2025 18:37:27 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV GOSU_VER=1.16
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxd"]
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 28 Aug 2025 18:37:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353a7ea5fa5c6bb8b5a3d2b2c549b5e78bcc3b3630e1425b9e2b5060f03b27c8`  
		Last Modified: Mon, 08 Sep 2025 22:03:59 GMT  
		Size: 9.6 MB (9626321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008c23392941f0ac573975e38eea9ca2f9a0a8d3eb1357b62cb7e185b995ddda`  
		Last Modified: Mon, 08 Sep 2025 22:03:58 GMT  
		Size: 5.8 MB (5790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a89d0e27e07debed5bf9f5500a2b514ded8d886adc7bd972274bd0cabe12b53`  
		Last Modified: Mon, 08 Sep 2025 22:04:00 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0565416d429978172f33f8473916faadb6f12a060860d0273296d7ac2e62ef9`  
		Last Modified: Mon, 08 Sep 2025 22:04:00 GMT  
		Size: 938.9 KB (938872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b6049e0c4a3b07a790ade738d82f9596efcfcaf637d1333684f32d33dbe6f`  
		Last Modified: Mon, 08 Sep 2025 22:04:07 GMT  
		Size: 96.0 MB (96038383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c066f3f4b5389cda111c7878c0c65a2d0100653973ecb6bf54a1855adade6ec5`  
		Last Modified: Mon, 08 Sep 2025 22:04:03 GMT  
		Size: 11.1 MB (11099009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5133689e87cf1b79291ba55551327073e4d99a4e804d53a6036bb8b9e5a3163`  
		Last Modified: Mon, 08 Sep 2025 22:04:02 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f59bf53b4c222d5ca0dc84ed4b20b4928d85383181f31cd86e7fcaf7fc8b697`  
		Last Modified: Mon, 08 Sep 2025 22:04:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5fb088dd891a90819393b8659ba6044dd6dddc731bf8e3241fa29084ad1164`  
		Last Modified: Mon, 08 Sep 2025 22:04:05 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:5bf7cd22c06c8e4195d8131ee52bfa54009d01e75ab39be142892fc14bb0a7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6a28f3d1e3ff56b67cab1bc08b8057940cbd92f6912df2fa2bbb626876aa35`

```dockerfile
```

-	Layers:
	-	`sha256:2ff50b519056e71fa024bf8d57a9b4667d37e331e5d809b20b2a0c6ee63c4a13`  
		Last Modified: Mon, 08 Sep 2025 23:21:05 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22aacdacdbb80e9c7f62beb9c6ef09e69eb0ac8a92f104d1aa2fa9c35bf0891`  
		Last Modified: Mon, 08 Sep 2025 23:21:06 GMT  
		Size: 33.7 KB (33718 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12-alpine`

```console
$ docker pull influxdb@sha256:d948cd7aa274696d76ccc3f7ef732180d9f9a4229aace3cf68ae008693665137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5ab58e6acde4a641694f7a2e6671a9f39921f3b8200e7cb04153599ff24a0171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81511579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fcb7b71c691969ff5b9884bf92ef34f16ca26efabcfb7fbd6d0ada332fe1458`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 03 Jul 2025 17:46:22 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41588b948a36335f02b1fe372411528fc71bf105e403c9b8476eaed4bc61b296`  
		Last Modified: Tue, 15 Jul 2025 20:47:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176c40e86352d8732707283812cf31b4cb48410b4d43bd9a1ea799b969178e28`  
		Last Modified: Tue, 15 Jul 2025 23:20:58 GMT  
		Size: 9.8 MB (9819933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124accecbf9a5d3fa58778cf7d727740b1808d84760e163ecbfe05c76fde911c`  
		Last Modified: Tue, 15 Jul 2025 23:20:58 GMT  
		Size: 6.2 MB (6156984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02be05aac4069c435b4c30f7102f4fef9d496612908c506d00a74fe121e992b`  
		Last Modified: Tue, 15 Jul 2025 20:47:43 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54aba977cca3a9f384b93f852720b3fdb29821d9601ec5402b7fabb7b84ed188`  
		Last Modified: Tue, 15 Jul 2025 23:21:07 GMT  
		Size: 50.1 MB (50115466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e18b3dde9d2ebba50fb26deb3e132dbff7bce833d3dec715b997305f4b7ead`  
		Last Modified: Tue, 15 Jul 2025 23:21:00 GMT  
		Size: 11.8 MB (11773676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a605a3944855fed4b0dc37407f21364b863d736d62e512592c17f37614f634b`  
		Last Modified: Tue, 15 Jul 2025 20:47:48 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3144ed5ee0ead4cb9ab07f97753eff4055313e54d6469a9a22feb04cc627f5b6`  
		Last Modified: Tue, 15 Jul 2025 20:47:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05126e91032baacdbb215f10aae69bd77e06da4add32161c42104ad83744d068`  
		Last Modified: Tue, 15 Jul 2025 20:47:55 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bce540c47d1075fe3bc1f3a18410f096d9a73701106a04b8724a850baa2a7e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 KB (941372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9814dc0d960e1dd48ab16ce3799261d16c65d82603d5e8c7d98111eeac6cb7`

```dockerfile
```

-	Layers:
	-	`sha256:6d325d7ce69647356cfcce291f65ab689996946f197ffff1db072b832f421271`  
		Last Modified: Tue, 15 Jul 2025 23:20:47 GMT  
		Size: 910.6 KB (910603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba6a4bbacf5ac36dfae6df2b86429b3103a25fc72709e829c3ba8afe8cf53a8`  
		Last Modified: Tue, 15 Jul 2025 23:20:48 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:328a4a0ffd4b2631ebbf3b75b62e14f3ddee93b48bca78be21da8f0fa818a823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78683906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d78e27ffcd6dd1fce93b95dcaddaa6c654dc6e7e6ee859bafc1df18b61481f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 03 Jul 2025 17:46:22 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600bb37154aec80b9f15e982c92a4e37ba42feeb4cc42826f6add6b7fb79ad89`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1672beef7b2cc4b76db6451487d605bebd392e9d0f8c39b48d43cd4f0aba306`  
		Last Modified: Wed, 16 Jul 2025 00:17:26 GMT  
		Size: 9.8 MB (9783360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9529e7bf79faa4c179f30c08b6771dac030c31ecdd63018c7651338afdae27e3`  
		Last Modified: Wed, 16 Jul 2025 00:17:26 GMT  
		Size: 5.8 MB (5790433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e0f93130bfcea152418034fcf70f62c1b31b5edcf475d536ee84548219f449`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d60bf4032b74fcc73c1c56e254540e8960145dace3efcea4bd97297bd88523`  
		Last Modified: Wed, 16 Jul 2025 00:17:30 GMT  
		Size: 48.0 MB (48016245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084d0c42d1d38a2397dde3e42086f8db8b36e263f884f0ce8262e26b056739eb`  
		Last Modified: Wed, 16 Jul 2025 00:17:27 GMT  
		Size: 11.1 MB (11098981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6bb2ad4fede2ef39df25c988f059baf0bb037f19a4120a3d05e07cc1bda614`  
		Last Modified: Wed, 16 Jul 2025 00:17:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9162549b851b3e4b3fa90cbc20f18519037f21bc774bb33be16d4d12d3c8d7`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1c7cb76b0374befb4a7b810686ef1d646abcb15428a55630c40d2bb6535310`  
		Last Modified: Wed, 16 Jul 2025 00:17:25 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cd7717fcd61869be57b993a9722525fd3640ca6c52d336aff4389c12cfa83d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.8 KB (940817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ba9a3b2a06597910ffc721dcc16534874f8b6068066a163f2298bf924c6ca2`

```dockerfile
```

-	Layers:
	-	`sha256:2e4eaed119ab9bd7fb9ec406598f4850075f76a7dc60d7ae0ec0cd6ad73111a4`  
		Last Modified: Wed, 16 Jul 2025 02:20:35 GMT  
		Size: 909.9 KB (909854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98b6129a43b1892d4bc0921a75ca680f9d9266e51b357532a467764c49c8f244`  
		Last Modified: Wed, 16 Jul 2025 02:20:36 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:8c3f00e2753ae66e10d4ed703f1dd81db837ca44b77a02f807ad3452305c4398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:277e9bb79fc0d67ed0887ecad7e727b984e91c4bd17712009a760727170a4cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115970202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e09d535f57ec1618d718dbb8b321860a8f514110036fbbb94f3c04f1d729c`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58caa54dae6936392a7d6810c9eeca044e5577994d946e6d522b76a83f52f59f`  
		Last Modified: Tue, 02 Sep 2025 00:24:06 GMT  
		Size: 6.7 MB (6665866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0b406ae8788be66faac6c384c5f7812bf46980a092f0b4aa0725d3956a368b`  
		Last Modified: Mon, 01 Sep 2025 23:46:44 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c3b64e38059133ace238c3245222415d08b3dfd73e6184dfcdc0f57f5fea5`  
		Last Modified: Tue, 02 Sep 2025 00:24:16 GMT  
		Size: 79.6 MB (79577148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34674521d2d4724573cf4ed17e4ad132029957d5b57778b2caacc90416a72286`  
		Last Modified: Mon, 01 Sep 2025 23:46:43 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b7e55a70382fd70564f93819b4cbcf759cd42c69fc75bc56a9de325fa6883`  
		Last Modified: Mon, 01 Sep 2025 23:46:43 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:ce91f2aae27acb09b2166a43b8ced0b3182217b3888543809781fec0753b0988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c890ae03564b3efa65be90026287be84a5662795b27d57ee77495da681b98c05`

```dockerfile
```

-	Layers:
	-	`sha256:511b04d131f1e70ca40ca6a34b183af114bdaede0a96a7380a90ca57d647ec23`  
		Last Modified: Tue, 02 Sep 2025 02:20:35 GMT  
		Size: 2.3 MB (2311325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3e58644f894989c3832fee34f59b2ee2996400a1344525df0927fbe9613e00`  
		Last Modified: Tue, 02 Sep 2025 02:20:36 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:645c2db68ce0c9719dc36cef4f0942f04b4c2a765ec7ddd73f9c28566b47dfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106744391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c167dbdce8c3c2146c1af1303819f7b65f838f0c195d3422b062005ef1f7a4cf`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721c5a748f13282a6d7aa41e6163030ef39209e05b4989378fb3ce8651e50756`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 6.7 MB (6676253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63690f73b0940ac63456c13f244f6534063ec34d4807eeeffcffcfb15ce3b6eb`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3102fbfd72fdd51b8b4567f96f3f202572c056064b12d7f88e7725485131fe`  
		Last Modified: Tue, 02 Sep 2025 01:50:13 GMT  
		Size: 71.2 MB (71203770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1402cc014213ad6daf2e15b070d46ffb5bf7f94eec764ed85c8af4183d3bc3fe`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5940274ce8f96af68b646040a97b261c971b60dd71c8d53d628991b29fc883bb`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:564ad84bbfe4a79a85f11cac717a492900dcccefa2c1320788515fdd9c9e3fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4414ee60de0301656ac337c9c8f28b535bb99ca966730724f26bdb03a71531c`

```dockerfile
```

-	Layers:
	-	`sha256:2a732303da3ec80b3fdedca489e93a6dc6ccdf95857ed0996a1a4c2ccdf2462c`  
		Last Modified: Tue, 02 Sep 2025 02:20:40 GMT  
		Size: 2.3 MB (2312407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfe401fef75d3354d0c656e0b0713ab11383b720eccc193c6caee349f8e87c0`  
		Last Modified: Tue, 02 Sep 2025 02:20:41 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:2705f859113e396082f25c5a02c383b5bfce1b85deee28add750baabbc4eb57a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:d7427d66ff098238d7d39d024867c88c7aebea02002d49fe5b89d2d8f4104c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121181366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1157615603865e564cbf0a219bc80e65b870bb382d0b76c538f5d3383418f6`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9d5f827eb8eca90390fd589f88dd065a7d851a594df4778d97ae1014df82e`  
		Last Modified: Tue, 02 Sep 2025 00:23:42 GMT  
		Size: 6.7 MB (6665842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbda502fb4d0358f433a1c3db886bae96b68b51c86b00c910ffdbc0881d1549f`  
		Last Modified: Tue, 02 Sep 2025 00:23:42 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c89a2b1b24e47a60949fbb2eb6286410242a82c86c396186179e1c3eedb786`  
		Last Modified: Tue, 02 Sep 2025 00:23:49 GMT  
		Size: 84.8 MB (84788329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5325733384351bfd4c2b6bb31adde56de17c077fe45e66ab6d90e20b90f0acdc`  
		Last Modified: Tue, 02 Sep 2025 00:23:44 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d531b7e648ab1fe95cefea15516c39a12d2040089e44d29d23fa0029e23971`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:37d9e1d11d561d75df794eb5fff433961cf461e2c2aa50c32a32002d1dbfd944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a89569d0e2ef289801fe4c0cdb20fca7c94d69b5ea16d316c7b6f1afbc6de6`

```dockerfile
```

-	Layers:
	-	`sha256:0ee87fb221431de07a081ffb9ab7827931b84bb48989175668f708270636400f`  
		Last Modified: Tue, 02 Sep 2025 02:20:40 GMT  
		Size: 2.3 MB (2311373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd7e10e153c07e691c557b4edc30d91062895b72ac998bf72c8b66d565b7734`  
		Last Modified: Tue, 02 Sep 2025 02:20:41 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:193b2986d48877977f3f3ef1a2885ba3302c771662961bbbee1298be42ead12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111857548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20454e8ee9489b025c4a703f9d8f7f3e30f39567faba03930430a2cc2461511f`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721c5a748f13282a6d7aa41e6163030ef39209e05b4989378fb3ce8651e50756`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 6.7 MB (6676253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63690f73b0940ac63456c13f244f6534063ec34d4807eeeffcffcfb15ce3b6eb`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775f887875d1de61d38c456440ee83cd7c87051b5ec89287949ed097ff6af128`  
		Last Modified: Tue, 02 Sep 2025 01:50:56 GMT  
		Size: 76.3 MB (76316927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758aeb03ced38391e8a9113dde32459fb360c135baa930db156a3dc8bbbcd26`  
		Last Modified: Tue, 02 Sep 2025 01:50:42 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a452d6c461e8935ec145def42d811c8424e3b06d6ee50678249cd8c5f32430dd`  
		Last Modified: Tue, 02 Sep 2025 01:50:42 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:e4bd0831c5a66037c502f54b045eb6f0ef7166e3c34698875c1ec47959ffd5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa204429c90abcf525f4ce4935b08ea87bd384564636e00d2a05d43da323f0d2`

```dockerfile
```

-	Layers:
	-	`sha256:38bdfe97535201c5d8d99be23dac098fd0e8974914e66d539424a2c4cdc5528e`  
		Last Modified: Tue, 02 Sep 2025 02:20:46 GMT  
		Size: 2.3 MB (2312455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09a20ded3e91e10654de13ece113ab472f1e1e9ec9e213c62e21c1e68e10607`  
		Last Modified: Tue, 02 Sep 2025 02:20:47 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.4-core`

```console
$ docker pull influxdb@sha256:8c3f00e2753ae66e10d4ed703f1dd81db837ca44b77a02f807ad3452305c4398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.4-core` - linux; amd64

```console
$ docker pull influxdb@sha256:277e9bb79fc0d67ed0887ecad7e727b984e91c4bd17712009a760727170a4cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115970202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e09d535f57ec1618d718dbb8b321860a8f514110036fbbb94f3c04f1d729c`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58caa54dae6936392a7d6810c9eeca044e5577994d946e6d522b76a83f52f59f`  
		Last Modified: Tue, 02 Sep 2025 00:24:06 GMT  
		Size: 6.7 MB (6665866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0b406ae8788be66faac6c384c5f7812bf46980a092f0b4aa0725d3956a368b`  
		Last Modified: Mon, 01 Sep 2025 23:46:44 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c3b64e38059133ace238c3245222415d08b3dfd73e6184dfcdc0f57f5fea5`  
		Last Modified: Tue, 02 Sep 2025 00:24:16 GMT  
		Size: 79.6 MB (79577148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34674521d2d4724573cf4ed17e4ad132029957d5b57778b2caacc90416a72286`  
		Last Modified: Mon, 01 Sep 2025 23:46:43 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b7e55a70382fd70564f93819b4cbcf759cd42c69fc75bc56a9de325fa6883`  
		Last Modified: Mon, 01 Sep 2025 23:46:43 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:ce91f2aae27acb09b2166a43b8ced0b3182217b3888543809781fec0753b0988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c890ae03564b3efa65be90026287be84a5662795b27d57ee77495da681b98c05`

```dockerfile
```

-	Layers:
	-	`sha256:511b04d131f1e70ca40ca6a34b183af114bdaede0a96a7380a90ca57d647ec23`  
		Last Modified: Tue, 02 Sep 2025 02:20:35 GMT  
		Size: 2.3 MB (2311325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3e58644f894989c3832fee34f59b2ee2996400a1344525df0927fbe9613e00`  
		Last Modified: Tue, 02 Sep 2025 02:20:36 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.4-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:645c2db68ce0c9719dc36cef4f0942f04b4c2a765ec7ddd73f9c28566b47dfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106744391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c167dbdce8c3c2146c1af1303819f7b65f838f0c195d3422b062005ef1f7a4cf`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721c5a748f13282a6d7aa41e6163030ef39209e05b4989378fb3ce8651e50756`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 6.7 MB (6676253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63690f73b0940ac63456c13f244f6534063ec34d4807eeeffcffcfb15ce3b6eb`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3102fbfd72fdd51b8b4567f96f3f202572c056064b12d7f88e7725485131fe`  
		Last Modified: Tue, 02 Sep 2025 01:50:13 GMT  
		Size: 71.2 MB (71203770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1402cc014213ad6daf2e15b070d46ffb5bf7f94eec764ed85c8af4183d3bc3fe`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5940274ce8f96af68b646040a97b261c971b60dd71c8d53d628991b29fc883bb`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:564ad84bbfe4a79a85f11cac717a492900dcccefa2c1320788515fdd9c9e3fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4414ee60de0301656ac337c9c8f28b535bb99ca966730724f26bdb03a71531c`

```dockerfile
```

-	Layers:
	-	`sha256:2a732303da3ec80b3fdedca489e93a6dc6ccdf95857ed0996a1a4c2ccdf2462c`  
		Last Modified: Tue, 02 Sep 2025 02:20:40 GMT  
		Size: 2.3 MB (2312407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfe401fef75d3354d0c656e0b0713ab11383b720eccc193c6caee349f8e87c0`  
		Last Modified: Tue, 02 Sep 2025 02:20:41 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.4-enterprise`

```console
$ docker pull influxdb@sha256:2705f859113e396082f25c5a02c383b5bfce1b85deee28add750baabbc4eb57a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.4-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:d7427d66ff098238d7d39d024867c88c7aebea02002d49fe5b89d2d8f4104c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121181366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1157615603865e564cbf0a219bc80e65b870bb382d0b76c538f5d3383418f6`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9d5f827eb8eca90390fd589f88dd065a7d851a594df4778d97ae1014df82e`  
		Last Modified: Tue, 02 Sep 2025 00:23:42 GMT  
		Size: 6.7 MB (6665842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbda502fb4d0358f433a1c3db886bae96b68b51c86b00c910ffdbc0881d1549f`  
		Last Modified: Tue, 02 Sep 2025 00:23:42 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c89a2b1b24e47a60949fbb2eb6286410242a82c86c396186179e1c3eedb786`  
		Last Modified: Tue, 02 Sep 2025 00:23:49 GMT  
		Size: 84.8 MB (84788329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5325733384351bfd4c2b6bb31adde56de17c077fe45e66ab6d90e20b90f0acdc`  
		Last Modified: Tue, 02 Sep 2025 00:23:44 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d531b7e648ab1fe95cefea15516c39a12d2040089e44d29d23fa0029e23971`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:37d9e1d11d561d75df794eb5fff433961cf461e2c2aa50c32a32002d1dbfd944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a89569d0e2ef289801fe4c0cdb20fca7c94d69b5ea16d316c7b6f1afbc6de6`

```dockerfile
```

-	Layers:
	-	`sha256:0ee87fb221431de07a081ffb9ab7827931b84bb48989175668f708270636400f`  
		Last Modified: Tue, 02 Sep 2025 02:20:40 GMT  
		Size: 2.3 MB (2311373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd7e10e153c07e691c557b4edc30d91062895b72ac998bf72c8b66d565b7734`  
		Last Modified: Tue, 02 Sep 2025 02:20:41 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:193b2986d48877977f3f3ef1a2885ba3302c771662961bbbee1298be42ead12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111857548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20454e8ee9489b025c4a703f9d8f7f3e30f39567faba03930430a2cc2461511f`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721c5a748f13282a6d7aa41e6163030ef39209e05b4989378fb3ce8651e50756`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 6.7 MB (6676253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63690f73b0940ac63456c13f244f6534063ec34d4807eeeffcffcfb15ce3b6eb`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775f887875d1de61d38c456440ee83cd7c87051b5ec89287949ed097ff6af128`  
		Last Modified: Tue, 02 Sep 2025 01:50:56 GMT  
		Size: 76.3 MB (76316927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758aeb03ced38391e8a9113dde32459fb360c135baa930db156a3dc8bbbcd26`  
		Last Modified: Tue, 02 Sep 2025 01:50:42 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a452d6c461e8935ec145def42d811c8424e3b06d6ee50678249cd8c5f32430dd`  
		Last Modified: Tue, 02 Sep 2025 01:50:42 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:e4bd0831c5a66037c502f54b045eb6f0ef7166e3c34698875c1ec47959ffd5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa204429c90abcf525f4ce4935b08ea87bd384564636e00d2a05d43da323f0d2`

```dockerfile
```

-	Layers:
	-	`sha256:38bdfe97535201c5d8d99be23dac098fd0e8974914e66d539424a2c4cdc5528e`  
		Last Modified: Tue, 02 Sep 2025 02:20:46 GMT  
		Size: 2.3 MB (2312455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09a20ded3e91e10654de13ece113ab472f1e1e9ec9e213c62e21c1e68e10607`  
		Last Modified: Tue, 02 Sep 2025 02:20:47 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.4.1-core`

```console
$ docker pull influxdb@sha256:8c3f00e2753ae66e10d4ed703f1dd81db837ca44b77a02f807ad3452305c4398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.4.1-core` - linux; amd64

```console
$ docker pull influxdb@sha256:277e9bb79fc0d67ed0887ecad7e727b984e91c4bd17712009a760727170a4cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115970202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e09d535f57ec1618d718dbb8b321860a8f514110036fbbb94f3c04f1d729c`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58caa54dae6936392a7d6810c9eeca044e5577994d946e6d522b76a83f52f59f`  
		Last Modified: Tue, 02 Sep 2025 00:24:06 GMT  
		Size: 6.7 MB (6665866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0b406ae8788be66faac6c384c5f7812bf46980a092f0b4aa0725d3956a368b`  
		Last Modified: Mon, 01 Sep 2025 23:46:44 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c3b64e38059133ace238c3245222415d08b3dfd73e6184dfcdc0f57f5fea5`  
		Last Modified: Tue, 02 Sep 2025 00:24:16 GMT  
		Size: 79.6 MB (79577148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34674521d2d4724573cf4ed17e4ad132029957d5b57778b2caacc90416a72286`  
		Last Modified: Mon, 01 Sep 2025 23:46:43 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b7e55a70382fd70564f93819b4cbcf759cd42c69fc75bc56a9de325fa6883`  
		Last Modified: Mon, 01 Sep 2025 23:46:43 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4.1-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:ce91f2aae27acb09b2166a43b8ced0b3182217b3888543809781fec0753b0988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c890ae03564b3efa65be90026287be84a5662795b27d57ee77495da681b98c05`

```dockerfile
```

-	Layers:
	-	`sha256:511b04d131f1e70ca40ca6a34b183af114bdaede0a96a7380a90ca57d647ec23`  
		Last Modified: Tue, 02 Sep 2025 02:20:35 GMT  
		Size: 2.3 MB (2311325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3e58644f894989c3832fee34f59b2ee2996400a1344525df0927fbe9613e00`  
		Last Modified: Tue, 02 Sep 2025 02:20:36 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.4.1-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:645c2db68ce0c9719dc36cef4f0942f04b4c2a765ec7ddd73f9c28566b47dfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106744391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c167dbdce8c3c2146c1af1303819f7b65f838f0c195d3422b062005ef1f7a4cf`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721c5a748f13282a6d7aa41e6163030ef39209e05b4989378fb3ce8651e50756`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 6.7 MB (6676253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63690f73b0940ac63456c13f244f6534063ec34d4807eeeffcffcfb15ce3b6eb`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3102fbfd72fdd51b8b4567f96f3f202572c056064b12d7f88e7725485131fe`  
		Last Modified: Tue, 02 Sep 2025 01:50:13 GMT  
		Size: 71.2 MB (71203770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1402cc014213ad6daf2e15b070d46ffb5bf7f94eec764ed85c8af4183d3bc3fe`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5940274ce8f96af68b646040a97b261c971b60dd71c8d53d628991b29fc883bb`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4.1-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:564ad84bbfe4a79a85f11cac717a492900dcccefa2c1320788515fdd9c9e3fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4414ee60de0301656ac337c9c8f28b535bb99ca966730724f26bdb03a71531c`

```dockerfile
```

-	Layers:
	-	`sha256:2a732303da3ec80b3fdedca489e93a6dc6ccdf95857ed0996a1a4c2ccdf2462c`  
		Last Modified: Tue, 02 Sep 2025 02:20:40 GMT  
		Size: 2.3 MB (2312407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfe401fef75d3354d0c656e0b0713ab11383b720eccc193c6caee349f8e87c0`  
		Last Modified: Tue, 02 Sep 2025 02:20:41 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.4.1-enterprise`

```console
$ docker pull influxdb@sha256:2705f859113e396082f25c5a02c383b5bfce1b85deee28add750baabbc4eb57a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.4.1-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:d7427d66ff098238d7d39d024867c88c7aebea02002d49fe5b89d2d8f4104c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121181366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1157615603865e564cbf0a219bc80e65b870bb382d0b76c538f5d3383418f6`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9d5f827eb8eca90390fd589f88dd065a7d851a594df4778d97ae1014df82e`  
		Last Modified: Tue, 02 Sep 2025 00:23:42 GMT  
		Size: 6.7 MB (6665842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbda502fb4d0358f433a1c3db886bae96b68b51c86b00c910ffdbc0881d1549f`  
		Last Modified: Tue, 02 Sep 2025 00:23:42 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c89a2b1b24e47a60949fbb2eb6286410242a82c86c396186179e1c3eedb786`  
		Last Modified: Tue, 02 Sep 2025 00:23:49 GMT  
		Size: 84.8 MB (84788329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5325733384351bfd4c2b6bb31adde56de17c077fe45e66ab6d90e20b90f0acdc`  
		Last Modified: Tue, 02 Sep 2025 00:23:44 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d531b7e648ab1fe95cefea15516c39a12d2040089e44d29d23fa0029e23971`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4.1-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:37d9e1d11d561d75df794eb5fff433961cf461e2c2aa50c32a32002d1dbfd944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a89569d0e2ef289801fe4c0cdb20fca7c94d69b5ea16d316c7b6f1afbc6de6`

```dockerfile
```

-	Layers:
	-	`sha256:0ee87fb221431de07a081ffb9ab7827931b84bb48989175668f708270636400f`  
		Last Modified: Tue, 02 Sep 2025 02:20:40 GMT  
		Size: 2.3 MB (2311373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd7e10e153c07e691c557b4edc30d91062895b72ac998bf72c8b66d565b7734`  
		Last Modified: Tue, 02 Sep 2025 02:20:41 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.4.1-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:193b2986d48877977f3f3ef1a2885ba3302c771662961bbbee1298be42ead12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111857548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20454e8ee9489b025c4a703f9d8f7f3e30f39567faba03930430a2cc2461511f`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721c5a748f13282a6d7aa41e6163030ef39209e05b4989378fb3ce8651e50756`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 6.7 MB (6676253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63690f73b0940ac63456c13f244f6534063ec34d4807eeeffcffcfb15ce3b6eb`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775f887875d1de61d38c456440ee83cd7c87051b5ec89287949ed097ff6af128`  
		Last Modified: Tue, 02 Sep 2025 01:50:56 GMT  
		Size: 76.3 MB (76316927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758aeb03ced38391e8a9113dde32459fb360c135baa930db156a3dc8bbbcd26`  
		Last Modified: Tue, 02 Sep 2025 01:50:42 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a452d6c461e8935ec145def42d811c8424e3b06d6ee50678249cd8c5f32430dd`  
		Last Modified: Tue, 02 Sep 2025 01:50:42 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4.1-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:e4bd0831c5a66037c502f54b045eb6f0ef7166e3c34698875c1ec47959ffd5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa204429c90abcf525f4ce4935b08ea87bd384564636e00d2a05d43da323f0d2`

```dockerfile
```

-	Layers:
	-	`sha256:38bdfe97535201c5d8d99be23dac098fd0e8974914e66d539424a2c4cdc5528e`  
		Last Modified: Tue, 02 Sep 2025 02:20:46 GMT  
		Size: 2.3 MB (2312455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09a20ded3e91e10654de13ece113ab472f1e1e9ec9e213c62e21c1e68e10607`  
		Last Modified: Tue, 02 Sep 2025 02:20:47 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:d948cd7aa274696d76ccc3f7ef732180d9f9a4229aace3cf68ae008693665137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5ab58e6acde4a641694f7a2e6671a9f39921f3b8200e7cb04153599ff24a0171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81511579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fcb7b71c691969ff5b9884bf92ef34f16ca26efabcfb7fbd6d0ada332fe1458`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 03 Jul 2025 17:46:22 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41588b948a36335f02b1fe372411528fc71bf105e403c9b8476eaed4bc61b296`  
		Last Modified: Tue, 15 Jul 2025 20:47:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176c40e86352d8732707283812cf31b4cb48410b4d43bd9a1ea799b969178e28`  
		Last Modified: Tue, 15 Jul 2025 23:20:58 GMT  
		Size: 9.8 MB (9819933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124accecbf9a5d3fa58778cf7d727740b1808d84760e163ecbfe05c76fde911c`  
		Last Modified: Tue, 15 Jul 2025 23:20:58 GMT  
		Size: 6.2 MB (6156984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02be05aac4069c435b4c30f7102f4fef9d496612908c506d00a74fe121e992b`  
		Last Modified: Tue, 15 Jul 2025 20:47:43 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54aba977cca3a9f384b93f852720b3fdb29821d9601ec5402b7fabb7b84ed188`  
		Last Modified: Tue, 15 Jul 2025 23:21:07 GMT  
		Size: 50.1 MB (50115466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e18b3dde9d2ebba50fb26deb3e132dbff7bce833d3dec715b997305f4b7ead`  
		Last Modified: Tue, 15 Jul 2025 23:21:00 GMT  
		Size: 11.8 MB (11773676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a605a3944855fed4b0dc37407f21364b863d736d62e512592c17f37614f634b`  
		Last Modified: Tue, 15 Jul 2025 20:47:48 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3144ed5ee0ead4cb9ab07f97753eff4055313e54d6469a9a22feb04cc627f5b6`  
		Last Modified: Tue, 15 Jul 2025 20:47:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05126e91032baacdbb215f10aae69bd77e06da4add32161c42104ad83744d068`  
		Last Modified: Tue, 15 Jul 2025 20:47:55 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bce540c47d1075fe3bc1f3a18410f096d9a73701106a04b8724a850baa2a7e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 KB (941372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9814dc0d960e1dd48ab16ce3799261d16c65d82603d5e8c7d98111eeac6cb7`

```dockerfile
```

-	Layers:
	-	`sha256:6d325d7ce69647356cfcce291f65ab689996946f197ffff1db072b832f421271`  
		Last Modified: Tue, 15 Jul 2025 23:20:47 GMT  
		Size: 910.6 KB (910603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba6a4bbacf5ac36dfae6df2b86429b3103a25fc72709e829c3ba8afe8cf53a8`  
		Last Modified: Tue, 15 Jul 2025 23:20:48 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:328a4a0ffd4b2631ebbf3b75b62e14f3ddee93b48bca78be21da8f0fa818a823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78683906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d78e27ffcd6dd1fce93b95dcaddaa6c654dc6e7e6ee859bafc1df18b61481f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 03 Jul 2025 17:46:22 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600bb37154aec80b9f15e982c92a4e37ba42feeb4cc42826f6add6b7fb79ad89`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1672beef7b2cc4b76db6451487d605bebd392e9d0f8c39b48d43cd4f0aba306`  
		Last Modified: Wed, 16 Jul 2025 00:17:26 GMT  
		Size: 9.8 MB (9783360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9529e7bf79faa4c179f30c08b6771dac030c31ecdd63018c7651338afdae27e3`  
		Last Modified: Wed, 16 Jul 2025 00:17:26 GMT  
		Size: 5.8 MB (5790433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e0f93130bfcea152418034fcf70f62c1b31b5edcf475d536ee84548219f449`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d60bf4032b74fcc73c1c56e254540e8960145dace3efcea4bd97297bd88523`  
		Last Modified: Wed, 16 Jul 2025 00:17:30 GMT  
		Size: 48.0 MB (48016245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084d0c42d1d38a2397dde3e42086f8db8b36e263f884f0ce8262e26b056739eb`  
		Last Modified: Wed, 16 Jul 2025 00:17:27 GMT  
		Size: 11.1 MB (11098981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6bb2ad4fede2ef39df25c988f059baf0bb037f19a4120a3d05e07cc1bda614`  
		Last Modified: Wed, 16 Jul 2025 00:17:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9162549b851b3e4b3fa90cbc20f18519037f21bc774bb33be16d4d12d3c8d7`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1c7cb76b0374befb4a7b810686ef1d646abcb15428a55630c40d2bb6535310`  
		Last Modified: Wed, 16 Jul 2025 00:17:25 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cd7717fcd61869be57b993a9722525fd3640ca6c52d336aff4389c12cfa83d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.8 KB (940817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ba9a3b2a06597910ffc721dcc16534874f8b6068066a163f2298bf924c6ca2`

```dockerfile
```

-	Layers:
	-	`sha256:2e4eaed119ab9bd7fb9ec406598f4850075f76a7dc60d7ae0ec0cd6ad73111a4`  
		Last Modified: Wed, 16 Jul 2025 02:20:35 GMT  
		Size: 909.9 KB (909854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98b6129a43b1892d4bc0921a75ca680f9d9266e51b357532a467764c49c8f244`  
		Last Modified: Wed, 16 Jul 2025 02:20:36 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:core`

```console
$ docker pull influxdb@sha256:8c3f00e2753ae66e10d4ed703f1dd81db837ca44b77a02f807ad3452305c4398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:277e9bb79fc0d67ed0887ecad7e727b984e91c4bd17712009a760727170a4cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115970202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e09d535f57ec1618d718dbb8b321860a8f514110036fbbb94f3c04f1d729c`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58caa54dae6936392a7d6810c9eeca044e5577994d946e6d522b76a83f52f59f`  
		Last Modified: Tue, 02 Sep 2025 00:24:06 GMT  
		Size: 6.7 MB (6665866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0b406ae8788be66faac6c384c5f7812bf46980a092f0b4aa0725d3956a368b`  
		Last Modified: Mon, 01 Sep 2025 23:46:44 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c3b64e38059133ace238c3245222415d08b3dfd73e6184dfcdc0f57f5fea5`  
		Last Modified: Tue, 02 Sep 2025 00:24:16 GMT  
		Size: 79.6 MB (79577148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34674521d2d4724573cf4ed17e4ad132029957d5b57778b2caacc90416a72286`  
		Last Modified: Mon, 01 Sep 2025 23:46:43 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b7e55a70382fd70564f93819b4cbcf759cd42c69fc75bc56a9de325fa6883`  
		Last Modified: Mon, 01 Sep 2025 23:46:43 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:ce91f2aae27acb09b2166a43b8ced0b3182217b3888543809781fec0753b0988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c890ae03564b3efa65be90026287be84a5662795b27d57ee77495da681b98c05`

```dockerfile
```

-	Layers:
	-	`sha256:511b04d131f1e70ca40ca6a34b183af114bdaede0a96a7380a90ca57d647ec23`  
		Last Modified: Tue, 02 Sep 2025 02:20:35 GMT  
		Size: 2.3 MB (2311325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3e58644f894989c3832fee34f59b2ee2996400a1344525df0927fbe9613e00`  
		Last Modified: Tue, 02 Sep 2025 02:20:36 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:645c2db68ce0c9719dc36cef4f0942f04b4c2a765ec7ddd73f9c28566b47dfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106744391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c167dbdce8c3c2146c1af1303819f7b65f838f0c195d3422b062005ef1f7a4cf`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721c5a748f13282a6d7aa41e6163030ef39209e05b4989378fb3ce8651e50756`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 6.7 MB (6676253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63690f73b0940ac63456c13f244f6534063ec34d4807eeeffcffcfb15ce3b6eb`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3102fbfd72fdd51b8b4567f96f3f202572c056064b12d7f88e7725485131fe`  
		Last Modified: Tue, 02 Sep 2025 01:50:13 GMT  
		Size: 71.2 MB (71203770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1402cc014213ad6daf2e15b070d46ffb5bf7f94eec764ed85c8af4183d3bc3fe`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5940274ce8f96af68b646040a97b261c971b60dd71c8d53d628991b29fc883bb`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:564ad84bbfe4a79a85f11cac717a492900dcccefa2c1320788515fdd9c9e3fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4414ee60de0301656ac337c9c8f28b535bb99ca966730724f26bdb03a71531c`

```dockerfile
```

-	Layers:
	-	`sha256:2a732303da3ec80b3fdedca489e93a6dc6ccdf95857ed0996a1a4c2ccdf2462c`  
		Last Modified: Tue, 02 Sep 2025 02:20:40 GMT  
		Size: 2.3 MB (2312407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfe401fef75d3354d0c656e0b0713ab11383b720eccc193c6caee349f8e87c0`  
		Last Modified: Tue, 02 Sep 2025 02:20:41 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:2705f859113e396082f25c5a02c383b5bfce1b85deee28add750baabbc4eb57a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:d7427d66ff098238d7d39d024867c88c7aebea02002d49fe5b89d2d8f4104c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121181366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1157615603865e564cbf0a219bc80e65b870bb382d0b76c538f5d3383418f6`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9d5f827eb8eca90390fd589f88dd065a7d851a594df4778d97ae1014df82e`  
		Last Modified: Tue, 02 Sep 2025 00:23:42 GMT  
		Size: 6.7 MB (6665842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbda502fb4d0358f433a1c3db886bae96b68b51c86b00c910ffdbc0881d1549f`  
		Last Modified: Tue, 02 Sep 2025 00:23:42 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c89a2b1b24e47a60949fbb2eb6286410242a82c86c396186179e1c3eedb786`  
		Last Modified: Tue, 02 Sep 2025 00:23:49 GMT  
		Size: 84.8 MB (84788329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5325733384351bfd4c2b6bb31adde56de17c077fe45e66ab6d90e20b90f0acdc`  
		Last Modified: Tue, 02 Sep 2025 00:23:44 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d531b7e648ab1fe95cefea15516c39a12d2040089e44d29d23fa0029e23971`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:37d9e1d11d561d75df794eb5fff433961cf461e2c2aa50c32a32002d1dbfd944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a89569d0e2ef289801fe4c0cdb20fca7c94d69b5ea16d316c7b6f1afbc6de6`

```dockerfile
```

-	Layers:
	-	`sha256:0ee87fb221431de07a081ffb9ab7827931b84bb48989175668f708270636400f`  
		Last Modified: Tue, 02 Sep 2025 02:20:40 GMT  
		Size: 2.3 MB (2311373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd7e10e153c07e691c557b4edc30d91062895b72ac998bf72c8b66d565b7734`  
		Last Modified: Tue, 02 Sep 2025 02:20:41 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:193b2986d48877977f3f3ef1a2885ba3302c771662961bbbee1298be42ead12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111857548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20454e8ee9489b025c4a703f9d8f7f3e30f39567faba03930430a2cc2461511f`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721c5a748f13282a6d7aa41e6163030ef39209e05b4989378fb3ce8651e50756`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 6.7 MB (6676253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63690f73b0940ac63456c13f244f6534063ec34d4807eeeffcffcfb15ce3b6eb`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775f887875d1de61d38c456440ee83cd7c87051b5ec89287949ed097ff6af128`  
		Last Modified: Tue, 02 Sep 2025 01:50:56 GMT  
		Size: 76.3 MB (76316927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3758aeb03ced38391e8a9113dde32459fb360c135baa930db156a3dc8bbbcd26`  
		Last Modified: Tue, 02 Sep 2025 01:50:42 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a452d6c461e8935ec145def42d811c8424e3b06d6ee50678249cd8c5f32430dd`  
		Last Modified: Tue, 02 Sep 2025 01:50:42 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:e4bd0831c5a66037c502f54b045eb6f0ef7166e3c34698875c1ec47959ffd5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa204429c90abcf525f4ce4935b08ea87bd384564636e00d2a05d43da323f0d2`

```dockerfile
```

-	Layers:
	-	`sha256:38bdfe97535201c5d8d99be23dac098fd0e8974914e66d539424a2c4cdc5528e`  
		Last Modified: Tue, 02 Sep 2025 02:20:46 GMT  
		Size: 2.3 MB (2312455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09a20ded3e91e10654de13ece113ab472f1e1e9ec9e213c62e21c1e68e10607`  
		Last Modified: Tue, 02 Sep 2025 02:20:47 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:23bc959dcb97f85e1fbc3a739805203eb3bcb779afede002cb205a37e14442bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:24439270fc10f3ad0aba36141f7d7d52d34496276ee0764fc8b687c10a7ff06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157220044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f693f2f6769e614b3926cb90bdd5a735f5934041e9aea399e321b720263ac6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 28 Aug 2025 18:37:27 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV GOSU_VER=1.16
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxd"]
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 28 Aug 2025 18:37:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62782c24a9fe40dad4bf8cdf7cf711a21c3430aef8b8568cfe22075c1b21d1d8`  
		Last Modified: Mon, 08 Sep 2025 22:09:55 GMT  
		Size: 9.8 MB (9796155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf10daca95d762897f2ecf3cc91f43c962f253a5d0850c712901f95ebc6cb860`  
		Last Modified: Mon, 08 Sep 2025 22:10:05 GMT  
		Size: 6.2 MB (6156969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69db941034b2f17178f1dee377fadcb052a3ba542951e2934630396c6ce38fff`  
		Last Modified: Mon, 08 Sep 2025 21:47:10 GMT  
		Size: 3.2 KB (3223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61ffd991d4118be05db267ed6b812395d53627ef54ab190548986977c47c91e`  
		Last Modified: Mon, 08 Sep 2025 21:47:14 GMT  
		Size: 1.0 MB (1012032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f089b773084833b051906a5cfc60dcfef719bccf6b472ff9ee8d313cef8beb95`  
		Last Modified: Mon, 08 Sep 2025 22:10:04 GMT  
		Size: 100.2 MB (100242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac18979dc6ef4c7cd439951f425f1285ef162444373e71cc329baeb1a239d03`  
		Last Modified: Mon, 08 Sep 2025 22:09:57 GMT  
		Size: 11.8 MB (11773668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea94f0bff41ed9285df20bae80b5eb0dba18abbbd5c689d03f539fc90c36b87`  
		Last Modified: Mon, 08 Sep 2025 21:47:20 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3fb6e72c97e5f0b88c165d61c791108d570d28a19b3fc8bf936d8968909afc`  
		Last Modified: Mon, 08 Sep 2025 21:47:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be06895ccb48e141a348befe63f5e6e265e07f3499e0ae5adfe23d28041ddfd`  
		Last Modified: Mon, 08 Sep 2025 21:47:28 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:87d7fb0a7704b203b9ba3ae556b4fe1579ddf9b0cb50a155d55bf01f012c2042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26666dc8233778fa995b2a30eb768571b0cc44154d2e843bb2551c63524aa458`

```dockerfile
```

-	Layers:
	-	`sha256:48309e5b7a6aa05829612b0ee07f5d5c51a876dd8b8f365132bec7bc483e29da`  
		Last Modified: Mon, 08 Sep 2025 23:21:00 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6155ac10102e3b3601478f687ab5fd30a0dbb728df25a23a218fd0339ed6ecf`  
		Last Modified: Mon, 08 Sep 2025 23:21:01 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4e2d08ccb2c6770b9bff4c99761464ae15a730142cf0aeef319b90e00bd5e195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151605052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90938dcb7ac0d05de4a3bba4fbd2f504535461956d40d5a8899111aa4bd5e3c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 28 Aug 2025 18:37:27 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV GOSU_VER=1.16
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 28 Aug 2025 18:37:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxd"]
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 28 Aug 2025 18:37:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353a7ea5fa5c6bb8b5a3d2b2c549b5e78bcc3b3630e1425b9e2b5060f03b27c8`  
		Last Modified: Mon, 08 Sep 2025 22:03:59 GMT  
		Size: 9.6 MB (9626321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008c23392941f0ac573975e38eea9ca2f9a0a8d3eb1357b62cb7e185b995ddda`  
		Last Modified: Mon, 08 Sep 2025 22:03:58 GMT  
		Size: 5.8 MB (5790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a89d0e27e07debed5bf9f5500a2b514ded8d886adc7bd972274bd0cabe12b53`  
		Last Modified: Mon, 08 Sep 2025 22:04:00 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0565416d429978172f33f8473916faadb6f12a060860d0273296d7ac2e62ef9`  
		Last Modified: Mon, 08 Sep 2025 22:04:00 GMT  
		Size: 938.9 KB (938872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b6049e0c4a3b07a790ade738d82f9596efcfcaf637d1333684f32d33dbe6f`  
		Last Modified: Mon, 08 Sep 2025 22:04:07 GMT  
		Size: 96.0 MB (96038383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c066f3f4b5389cda111c7878c0c65a2d0100653973ecb6bf54a1855adade6ec5`  
		Last Modified: Mon, 08 Sep 2025 22:04:03 GMT  
		Size: 11.1 MB (11099009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5133689e87cf1b79291ba55551327073e4d99a4e804d53a6036bb8b9e5a3163`  
		Last Modified: Mon, 08 Sep 2025 22:04:02 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f59bf53b4c222d5ca0dc84ed4b20b4928d85383181f31cd86e7fcaf7fc8b697`  
		Last Modified: Mon, 08 Sep 2025 22:04:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5fb088dd891a90819393b8659ba6044dd6dddc731bf8e3241fa29084ad1164`  
		Last Modified: Mon, 08 Sep 2025 22:04:05 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:5bf7cd22c06c8e4195d8131ee52bfa54009d01e75ab39be142892fc14bb0a7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6a28f3d1e3ff56b67cab1bc08b8057940cbd92f6912df2fa2bbb626876aa35`

```dockerfile
```

-	Layers:
	-	`sha256:2ff50b519056e71fa024bf8d57a9b4667d37e331e5d809b20b2a0c6ee63c4a13`  
		Last Modified: Mon, 08 Sep 2025 23:21:05 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22aacdacdbb80e9c7f62beb9c6ef09e69eb0ac8a92f104d1aa2fa9c35bf0891`  
		Last Modified: Mon, 08 Sep 2025 23:21:06 GMT  
		Size: 33.7 KB (33718 bytes)  
		MIME: application/vnd.in-toto+json
