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
-	[`influxdb:3.4.0-core`](#influxdb340-core)
-	[`influxdb:3.4.0-enterprise`](#influxdb340-enterprise)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:core`](#influxdbcore)
-	[`influxdb:enterprise`](#influxdbenterprise)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:2d37276e5b59bc58c1008e9a155b0d7555b4f3bea5ad622951dd70ad601db37b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:51b520102687fc5cb02a49441555e3461c8d80f1eba183e4921b059e3a77cfd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108963810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26ad4fe4fa19f081113b0a4c8d6af1b763c24a7c651e00d434c9505b102fe60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 30 Jul 2025 00:49:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620e616831b3851d274036e48fee788599fe355ea621ba7b912b9c15925e81f`  
		Last Modified: Tue, 12 Aug 2025 21:21:48 GMT  
		Size: 15.8 MB (15765318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4a61d792301316a3358ac2b699f383d6846b516fce0d2182758050a3e4be10`  
		Last Modified: Tue, 12 Aug 2025 22:18:33 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9b004ccd5e20cd92a0d21528352ab1cbae86e61de60e7ba42e51562b77bfce`  
		Last Modified: Tue, 12 Aug 2025 22:18:38 GMT  
		Size: 39.4 MB (39439599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66102a25615757e74ba0890051c6b6f811b0c312c87f0646a7438665f8a9d60a`  
		Last Modified: Tue, 12 Aug 2025 22:18:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26222da7d713ec6aeb232bcbddf4a80fe3b7ca4166a5c7df5aad2c1c8046b6f2`  
		Last Modified: Tue, 12 Aug 2025 22:18:34 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1035b592032cf2b9b37343c9da013ae8f40ada54b113c94f91952ef06f6fd98`  
		Last Modified: Tue, 12 Aug 2025 22:18:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:0babe93eae6aab7041c1e753b6d479470dee49c91ca11ca0c54a734ae8f2a03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4799034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e34ccf26ac6440f3ca868e11526466393221cd0e5d2c9365c3406ff8b3b767c`

```dockerfile
```

-	Layers:
	-	`sha256:18f263be990d50b620a735a31d3eafd7b54f6790e6a62777a8ac07d9c73e3255`  
		Last Modified: Tue, 12 Aug 2025 23:20:18 GMT  
		Size: 4.8 MB (4784326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:917e48080c8ed371503bb0f757a9b456dfd45bbdc75dbcd875541a4261c8ec3c`  
		Last Modified: Tue, 12 Aug 2025 23:20:19 GMT  
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
$ docker pull influxdb@sha256:167d9fce659f6ee2bab88281c9753741daf51609aa0607236a0c283be26d69c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:6b9bc220d299d963ba2aee37c2dff2548431bace3dce19edf905418b390f50b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88163017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1f5af78c4968e23785d61b5ec5f3eb16c5d8227360d68697b24b0c4f083b23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 30 Jul 2025 00:49:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620e616831b3851d274036e48fee788599fe355ea621ba7b912b9c15925e81f`  
		Last Modified: Tue, 12 Aug 2025 21:21:48 GMT  
		Size: 15.8 MB (15765318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5f7d5a5d873d38a042ba0a75713d4ee57ed3f4f18949803fbd4395414391fc`  
		Last Modified: Tue, 12 Aug 2025 22:18:43 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a51087700716863129e39337b34d09e04261a49f33421a4e6d073bd2231953`  
		Last Modified: Tue, 12 Aug 2025 22:18:48 GMT  
		Size: 18.6 MB (18640003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f2586887e2b8611d80f05d412cc800d0a16cf553a4720592e02ec16560e94a`  
		Last Modified: Tue, 12 Aug 2025 22:18:44 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ce0a9546b404b7826c5bfded3b5f5e8382b421e94dc57903e5bb2cc1d0725`  
		Last Modified: Tue, 12 Aug 2025 22:18:45 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:5761b11c98814c4926f94fbc9658ffff19e41e12226f4eba8b5372b71bb3381b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d7ce2c4a705a6bccbee976aaf19de7a604ea0e0e993da301d9e6239c0f9c04`

```dockerfile
```

-	Layers:
	-	`sha256:df4e79e3ba7184f2fda76f34b552f0bae6364021e36d9f94f957742604b34685`  
		Last Modified: Tue, 12 Aug 2025 23:20:22 GMT  
		Size: 4.7 MB (4708306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b21c34f04dd8ccbc096d6884ec4481966af1d301a0879664f5407853aa1773`  
		Last Modified: Tue, 12 Aug 2025 23:20:22 GMT  
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
$ docker pull influxdb@sha256:2d37276e5b59bc58c1008e9a155b0d7555b4f3bea5ad622951dd70ad601db37b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:51b520102687fc5cb02a49441555e3461c8d80f1eba183e4921b059e3a77cfd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108963810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26ad4fe4fa19f081113b0a4c8d6af1b763c24a7c651e00d434c9505b102fe60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 30 Jul 2025 00:49:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620e616831b3851d274036e48fee788599fe355ea621ba7b912b9c15925e81f`  
		Last Modified: Tue, 12 Aug 2025 21:21:48 GMT  
		Size: 15.8 MB (15765318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4a61d792301316a3358ac2b699f383d6846b516fce0d2182758050a3e4be10`  
		Last Modified: Tue, 12 Aug 2025 22:18:33 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9b004ccd5e20cd92a0d21528352ab1cbae86e61de60e7ba42e51562b77bfce`  
		Last Modified: Tue, 12 Aug 2025 22:18:38 GMT  
		Size: 39.4 MB (39439599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66102a25615757e74ba0890051c6b6f811b0c312c87f0646a7438665f8a9d60a`  
		Last Modified: Tue, 12 Aug 2025 22:18:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26222da7d713ec6aeb232bcbddf4a80fe3b7ca4166a5c7df5aad2c1c8046b6f2`  
		Last Modified: Tue, 12 Aug 2025 22:18:34 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1035b592032cf2b9b37343c9da013ae8f40ada54b113c94f91952ef06f6fd98`  
		Last Modified: Tue, 12 Aug 2025 22:18:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:0babe93eae6aab7041c1e753b6d479470dee49c91ca11ca0c54a734ae8f2a03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4799034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e34ccf26ac6440f3ca868e11526466393221cd0e5d2c9365c3406ff8b3b767c`

```dockerfile
```

-	Layers:
	-	`sha256:18f263be990d50b620a735a31d3eafd7b54f6790e6a62777a8ac07d9c73e3255`  
		Last Modified: Tue, 12 Aug 2025 23:20:18 GMT  
		Size: 4.8 MB (4784326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:917e48080c8ed371503bb0f757a9b456dfd45bbdc75dbcd875541a4261c8ec3c`  
		Last Modified: Tue, 12 Aug 2025 23:20:19 GMT  
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
$ docker pull influxdb@sha256:167d9fce659f6ee2bab88281c9753741daf51609aa0607236a0c283be26d69c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:6b9bc220d299d963ba2aee37c2dff2548431bace3dce19edf905418b390f50b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88163017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1f5af78c4968e23785d61b5ec5f3eb16c5d8227360d68697b24b0c4f083b23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 30 Jul 2025 00:49:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620e616831b3851d274036e48fee788599fe355ea621ba7b912b9c15925e81f`  
		Last Modified: Tue, 12 Aug 2025 21:21:48 GMT  
		Size: 15.8 MB (15765318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5f7d5a5d873d38a042ba0a75713d4ee57ed3f4f18949803fbd4395414391fc`  
		Last Modified: Tue, 12 Aug 2025 22:18:43 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a51087700716863129e39337b34d09e04261a49f33421a4e6d073bd2231953`  
		Last Modified: Tue, 12 Aug 2025 22:18:48 GMT  
		Size: 18.6 MB (18640003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f2586887e2b8611d80f05d412cc800d0a16cf553a4720592e02ec16560e94a`  
		Last Modified: Tue, 12 Aug 2025 22:18:44 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ce0a9546b404b7826c5bfded3b5f5e8382b421e94dc57903e5bb2cc1d0725`  
		Last Modified: Tue, 12 Aug 2025 22:18:45 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:5761b11c98814c4926f94fbc9658ffff19e41e12226f4eba8b5372b71bb3381b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d7ce2c4a705a6bccbee976aaf19de7a604ea0e0e993da301d9e6239c0f9c04`

```dockerfile
```

-	Layers:
	-	`sha256:df4e79e3ba7184f2fda76f34b552f0bae6364021e36d9f94f957742604b34685`  
		Last Modified: Tue, 12 Aug 2025 23:20:22 GMT  
		Size: 4.7 MB (4708306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b21c34f04dd8ccbc096d6884ec4481966af1d301a0879664f5407853aa1773`  
		Last Modified: Tue, 12 Aug 2025 23:20:22 GMT  
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
$ docker pull influxdb@sha256:1f877df099074570f1aeb50e019506851aff177bcc3e34e63c5900539f9db261
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:331e6f23bc13da82dbe1188dbd55f485316b760f2ee3a09f0d009c519c245039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116170308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a76bffa188c8aff79d99459635716e9f4f833337d3678811ae54936d1867d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 30 Jul 2025 00:49:58 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
USER influxdb
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e689de727132c42b45d88714a1e83af061195523f5403d14c7e76a6000351d`  
		Last Modified: Tue, 12 Aug 2025 22:42:40 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48a9bd76662279fabd1ff1ac075e488f48fef8642b52287cbdabd453e5d6f9`  
		Last Modified: Tue, 12 Aug 2025 22:42:46 GMT  
		Size: 43.7 MB (43652045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9fc20ec45ca33ca7eaf21cb4d1903a53c6ff0873b4795f3b58bd32e57c60b7`  
		Last Modified: Tue, 12 Aug 2025 22:42:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a041cb57de5a94b193827742e8a64b5f59684571a33c7ddde5fcf161d829397`  
		Last Modified: Tue, 12 Aug 2025 22:42:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354730316dfbf6c0e44d5de83399585b788e0cd8276feb2c2a2ca871ec9ac681`  
		Last Modified: Tue, 12 Aug 2025 22:42:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:f2a422dda4111a997f972b2923747f4b634d0e613289e1535a64fb494e945b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b70dfee8fbb0a92f9b5f5bf433cd2168976f350fb621c5769bfb583b1e7db9d`

```dockerfile
```

-	Layers:
	-	`sha256:1eaf98e71480e4b0505fb953584fccf740ea712c267142e7c324b6e5c575bd03`  
		Last Modified: Tue, 12 Aug 2025 23:20:30 GMT  
		Size: 5.1 MB (5071847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c2b879b822cac6d5d1ba1bd2d665ee896f04d1572a069930683100321090bb2`  
		Last Modified: Tue, 12 Aug 2025 23:20:30 GMT  
		Size: 15.5 KB (15528 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0ec637ed3a2eaa0285f22347b63c7f2c452150b829111690e5c6426b0fd9b3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113034765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daeb3b4de15f1625926c39d778270c222895a7cb81142115b9e48ce75a26a146`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 30 Jul 2025 00:49:58 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
USER influxdb
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4bd18caf809911554ad2949b95522744ad8a053b93dd4057b556effda46760`  
		Last Modified: Wed, 13 Aug 2025 16:09:49 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde048fbc70489fe5776633008cdb457571a2ec82ba408553f7094bf4bc7e184`  
		Last Modified: Wed, 13 Aug 2025 16:09:54 GMT  
		Size: 41.1 MB (41119554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9448ada95bb3ab7f8513f8fb6ce94397b6c0f4dd330c662b1cd602587103b8`  
		Last Modified: Wed, 13 Aug 2025 16:09:49 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504d79e451dfcd251c11bcaea7537efe3926577c145fc2a50fb21df50e029051`  
		Last Modified: Wed, 13 Aug 2025 16:09:51 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38601ae97a7d2e3d683961073c29936e9077c4d29e9f41323c6c27935be270af`  
		Last Modified: Wed, 13 Aug 2025 16:09:50 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:384ebd3cffa60a87bcb2f44dd5ecbb80d0bbc9b5b445cf4fc8d20eddcca3b58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f0d371fd7234da38f5bd278104fa7ca0bfc2185370041675374bb1e06b0354`

```dockerfile
```

-	Layers:
	-	`sha256:0d603a76a5105da230e8937ffa279a4019d905d1324590e78728d0a1bda45e80`  
		Last Modified: Wed, 13 Aug 2025 17:20:25 GMT  
		Size: 5.1 MB (5071312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53794770039668e1f5fed0b9cf454004eb3a9e54422b5c7659a7f844c1f23ae7`  
		Last Modified: Wed, 13 Aug 2025 17:20:27 GMT  
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
$ docker pull influxdb@sha256:74e1102becacc83847ba95c007a9b8dccbb959bd2f5de138f24ae85df32d9108
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f205de772096b0a0665356bda5bf595ee9a033edd05e8402263ce57db2b65ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111698193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7194ef729ea5af8646df53edeee5b62eb26bda4351ed4c2b4bf1766ed7f5bb0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Wed, 30 Jul 2025 00:49:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c7fcfc69686db7983c945bde5178e60aa46d3103de85760324f6dc93844a59`  
		Last Modified: Tue, 12 Aug 2025 22:42:41 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9867965bfc7f8f2056173dc3a6c84a77b69b239ffdf8f07afb1515dac7c206ff`  
		Last Modified: Tue, 12 Aug 2025 22:42:49 GMT  
		Size: 39.2 MB (39179296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd2ff849459b96951444f2f5f0c77cbe2eafdb0a8047c6ccf58bfb857837f74`  
		Last Modified: Tue, 12 Aug 2025 22:42:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96503ac2bdeebfc92f010317cda477aa4bb06a15be1314b792cd486a7033bd2`  
		Last Modified: Tue, 12 Aug 2025 22:42:42 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dc9dd74402e6fcaedb82fc68224d8742ac3ee166b747fc1de2aa499e69bb20`  
		Last Modified: Tue, 12 Aug 2025 22:42:44 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:d34b17725da5dddb3e0f0d74724e257538c66bf2b3571459c54349bb75d63d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09afb9971a4bab0614b3e77e82d743d2bcf5780d8b431280ab96143b622651db`

```dockerfile
```

-	Layers:
	-	`sha256:cb8c813442725887d6024fb12d18ba0c424f4bb28600a5be869e8692e4fb8dfa`  
		Last Modified: Tue, 12 Aug 2025 23:20:34 GMT  
		Size: 4.7 MB (4661024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a259063d0c9ce7f0d339e8991782f4fcfc19fb6751616d796bcacdb040fb77f7`  
		Last Modified: Tue, 12 Aug 2025 23:20:35 GMT  
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
$ docker pull influxdb@sha256:7eee0b3c1d94c9651bd1a2b01fea329a0e5179c4b87ec6b7c11858abd5deee02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:5e61fcacfd2d01c5590e1e4afdb3b7b4c3134c9a6b9c9cbbf1299e554bfb291f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90854251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c941c6c41f642f89dd4ff1320e3157bea3b03d28b92370c9fcf28f242ebedc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Wed, 30 Jul 2025 00:49:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744315724b130569e2aaacb40f2b8357938360899b49a1a8524c852742a637de`  
		Last Modified: Tue, 12 Aug 2025 22:42:43 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456a7c13ea1b681605ad134d6860e74b98957e4116936593594f0573e5508e84`  
		Last Modified: Tue, 12 Aug 2025 22:42:45 GMT  
		Size: 18.3 MB (18336565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9ea9b0ea45a67115bc7e96d16b20c64f71f5be62da453187fb89dba4490ba2`  
		Last Modified: Tue, 12 Aug 2025 22:42:38 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8480b69b443aab4ee2b8191c4c8866c1a2a11e19a1784809aa8e132327d238e`  
		Last Modified: Tue, 12 Aug 2025 22:42:38 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:1cdd9b7e08aa18032b9b061ae98b4a2b53842424acd02495dce3d4dc71a38999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4599062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbe2115339bb97c1cbb50a926e472587f5b14347fe0caf665aac950bbeedf9e`

```dockerfile
```

-	Layers:
	-	`sha256:4241aee2e71134dd895821407f1538e57ef6f71df9c7e904b0a93c581bb40c6b`  
		Last Modified: Tue, 12 Aug 2025 23:20:40 GMT  
		Size: 4.6 MB (4585995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61a829f5f052dcf56cfb7f1356c83df8288a5870359b6844cb4f95998ed0248`  
		Last Modified: Tue, 12 Aug 2025 23:20:41 GMT  
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
$ docker pull influxdb@sha256:1f877df099074570f1aeb50e019506851aff177bcc3e34e63c5900539f9db261
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:331e6f23bc13da82dbe1188dbd55f485316b760f2ee3a09f0d009c519c245039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116170308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a76bffa188c8aff79d99459635716e9f4f833337d3678811ae54936d1867d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 30 Jul 2025 00:49:58 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
USER influxdb
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e689de727132c42b45d88714a1e83af061195523f5403d14c7e76a6000351d`  
		Last Modified: Tue, 12 Aug 2025 22:42:40 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48a9bd76662279fabd1ff1ac075e488f48fef8642b52287cbdabd453e5d6f9`  
		Last Modified: Tue, 12 Aug 2025 22:42:46 GMT  
		Size: 43.7 MB (43652045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9fc20ec45ca33ca7eaf21cb4d1903a53c6ff0873b4795f3b58bd32e57c60b7`  
		Last Modified: Tue, 12 Aug 2025 22:42:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a041cb57de5a94b193827742e8a64b5f59684571a33c7ddde5fcf161d829397`  
		Last Modified: Tue, 12 Aug 2025 22:42:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354730316dfbf6c0e44d5de83399585b788e0cd8276feb2c2a2ca871ec9ac681`  
		Last Modified: Tue, 12 Aug 2025 22:42:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:f2a422dda4111a997f972b2923747f4b634d0e613289e1535a64fb494e945b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b70dfee8fbb0a92f9b5f5bf433cd2168976f350fb621c5769bfb583b1e7db9d`

```dockerfile
```

-	Layers:
	-	`sha256:1eaf98e71480e4b0505fb953584fccf740ea712c267142e7c324b6e5c575bd03`  
		Last Modified: Tue, 12 Aug 2025 23:20:30 GMT  
		Size: 5.1 MB (5071847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c2b879b822cac6d5d1ba1bd2d665ee896f04d1572a069930683100321090bb2`  
		Last Modified: Tue, 12 Aug 2025 23:20:30 GMT  
		Size: 15.5 KB (15528 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0ec637ed3a2eaa0285f22347b63c7f2c452150b829111690e5c6426b0fd9b3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113034765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daeb3b4de15f1625926c39d778270c222895a7cb81142115b9e48ce75a26a146`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 30 Jul 2025 00:49:58 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
USER influxdb
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4bd18caf809911554ad2949b95522744ad8a053b93dd4057b556effda46760`  
		Last Modified: Wed, 13 Aug 2025 16:09:49 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde048fbc70489fe5776633008cdb457571a2ec82ba408553f7094bf4bc7e184`  
		Last Modified: Wed, 13 Aug 2025 16:09:54 GMT  
		Size: 41.1 MB (41119554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9448ada95bb3ab7f8513f8fb6ce94397b6c0f4dd330c662b1cd602587103b8`  
		Last Modified: Wed, 13 Aug 2025 16:09:49 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504d79e451dfcd251c11bcaea7537efe3926577c145fc2a50fb21df50e029051`  
		Last Modified: Wed, 13 Aug 2025 16:09:51 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38601ae97a7d2e3d683961073c29936e9077c4d29e9f41323c6c27935be270af`  
		Last Modified: Wed, 13 Aug 2025 16:09:50 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:384ebd3cffa60a87bcb2f44dd5ecbb80d0bbc9b5b445cf4fc8d20eddcca3b58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f0d371fd7234da38f5bd278104fa7ca0bfc2185370041675374bb1e06b0354`

```dockerfile
```

-	Layers:
	-	`sha256:0d603a76a5105da230e8937ffa279a4019d905d1324590e78728d0a1bda45e80`  
		Last Modified: Wed, 13 Aug 2025 17:20:25 GMT  
		Size: 5.1 MB (5071312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53794770039668e1f5fed0b9cf454004eb3a9e54422b5c7659a7f844c1f23ae7`  
		Last Modified: Wed, 13 Aug 2025 17:20:27 GMT  
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
$ docker pull influxdb@sha256:74e1102becacc83847ba95c007a9b8dccbb959bd2f5de138f24ae85df32d9108
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f205de772096b0a0665356bda5bf595ee9a033edd05e8402263ce57db2b65ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111698193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7194ef729ea5af8646df53edeee5b62eb26bda4351ed4c2b4bf1766ed7f5bb0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Wed, 30 Jul 2025 00:49:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c7fcfc69686db7983c945bde5178e60aa46d3103de85760324f6dc93844a59`  
		Last Modified: Tue, 12 Aug 2025 22:42:41 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9867965bfc7f8f2056173dc3a6c84a77b69b239ffdf8f07afb1515dac7c206ff`  
		Last Modified: Tue, 12 Aug 2025 22:42:49 GMT  
		Size: 39.2 MB (39179296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd2ff849459b96951444f2f5f0c77cbe2eafdb0a8047c6ccf58bfb857837f74`  
		Last Modified: Tue, 12 Aug 2025 22:42:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96503ac2bdeebfc92f010317cda477aa4bb06a15be1314b792cd486a7033bd2`  
		Last Modified: Tue, 12 Aug 2025 22:42:42 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dc9dd74402e6fcaedb82fc68224d8742ac3ee166b747fc1de2aa499e69bb20`  
		Last Modified: Tue, 12 Aug 2025 22:42:44 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:d34b17725da5dddb3e0f0d74724e257538c66bf2b3571459c54349bb75d63d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09afb9971a4bab0614b3e77e82d743d2bcf5780d8b431280ab96143b622651db`

```dockerfile
```

-	Layers:
	-	`sha256:cb8c813442725887d6024fb12d18ba0c424f4bb28600a5be869e8692e4fb8dfa`  
		Last Modified: Tue, 12 Aug 2025 23:20:34 GMT  
		Size: 4.7 MB (4661024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a259063d0c9ce7f0d339e8991782f4fcfc19fb6751616d796bcacdb040fb77f7`  
		Last Modified: Tue, 12 Aug 2025 23:20:35 GMT  
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
$ docker pull influxdb@sha256:7eee0b3c1d94c9651bd1a2b01fea329a0e5179c4b87ec6b7c11858abd5deee02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:5e61fcacfd2d01c5590e1e4afdb3b7b4c3134c9a6b9c9cbbf1299e554bfb291f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90854251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c941c6c41f642f89dd4ff1320e3157bea3b03d28b92370c9fcf28f242ebedc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Wed, 30 Jul 2025 00:49:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744315724b130569e2aaacb40f2b8357938360899b49a1a8524c852742a637de`  
		Last Modified: Tue, 12 Aug 2025 22:42:43 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456a7c13ea1b681605ad134d6860e74b98957e4116936593594f0573e5508e84`  
		Last Modified: Tue, 12 Aug 2025 22:42:45 GMT  
		Size: 18.3 MB (18336565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9ea9b0ea45a67115bc7e96d16b20c64f71f5be62da453187fb89dba4490ba2`  
		Last Modified: Tue, 12 Aug 2025 22:42:38 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8480b69b443aab4ee2b8191c4c8866c1a2a11e19a1784809aa8e132327d238e`  
		Last Modified: Tue, 12 Aug 2025 22:42:38 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:1cdd9b7e08aa18032b9b061ae98b4a2b53842424acd02495dce3d4dc71a38999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4599062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbe2115339bb97c1cbb50a926e472587f5b14347fe0caf665aac950bbeedf9e`

```dockerfile
```

-	Layers:
	-	`sha256:4241aee2e71134dd895821407f1538e57ef6f71df9c7e904b0a93c581bb40c6b`  
		Last Modified: Tue, 12 Aug 2025 23:20:40 GMT  
		Size: 4.6 MB (4585995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61a829f5f052dcf56cfb7f1356c83df8288a5870359b6844cb4f95998ed0248`  
		Last Modified: Tue, 12 Aug 2025 23:20:41 GMT  
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
$ docker pull influxdb@sha256:59fe0181a3b161d36e9ce53001d7e1678762013ab0a284969ec2ebc517b529cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:b53805c0d05ab8d6dfc1443601ad539a1a395da0cb245bc771e487bff51345b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c43ca08192493c2c7a92559ab42c7ba3d7ca8820315d48ec1796a12c4a455`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 30 Jul 2025 00:49:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 30 Jul 2025 00:49:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV GOSU_VER=1.16
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Jul 2025 00:49:58 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d787a2de635a3059a66130180c8fc200a1b06c38135e8cd8092bc7be831ace62`  
		Last Modified: Tue, 12 Aug 2025 23:20:48 GMT  
		Size: 9.8 MB (9795849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3898caa9f81699d8c89fab840780c3e4ad1614949afc5ce26e4f7f4c0aff53d6`  
		Last Modified: Tue, 12 Aug 2025 23:20:48 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a784fc11f9cc8e18ae504d7e632e1939db12d92f983a2f2fa779a6ecca9c1d2`  
		Last Modified: Tue, 12 Aug 2025 22:58:11 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef6cfa01d55151e6bcf217da71c7f68545a5c18d96f9565242c69768b406265`  
		Last Modified: Tue, 12 Aug 2025 22:58:11 GMT  
		Size: 1.0 MB (1012033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0c0f100724b45479445b6b5d7c4a4d81379501181d0bcab57536fd0878359a`  
		Last Modified: Tue, 12 Aug 2025 23:20:51 GMT  
		Size: 100.2 MB (100242976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e3abb7a1c83e8e7d62bf3f915c57ce0c1bc7210cdc92072470a587fbaaced0`  
		Last Modified: Tue, 12 Aug 2025 23:20:49 GMT  
		Size: 11.8 MB (11773671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672405b61b597ccf9c47b82c19804743221a5c728b7283d286ceded23f96a3d7`  
		Last Modified: Tue, 12 Aug 2025 22:58:10 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fb7af7503dcb240d9098512683f3ab6cfe53693042dcfb4ad4791438537855`  
		Last Modified: Tue, 12 Aug 2025 22:58:10 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15b9d9b72b45d2fd3c4b139e6ce2bce52ff022fe54fa1a42d3f3e4161e3e695`  
		Last Modified: Tue, 12 Aug 2025 22:58:11 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:41c53b569e3968e48c2e3fb0bad86c21eaa53afbc1219b275999868e500cb471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870727706d286cdb78d544afb60f0642a9075e7ec604b54f50a428e860f7b4cf`

```dockerfile
```

-	Layers:
	-	`sha256:833fa77c36bca1fe044b59077abcaa17c696946bc525d08f30d929e096b99a01`  
		Last Modified: Tue, 12 Aug 2025 23:20:48 GMT  
		Size: 3.0 MB (2979773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:102e59daf6dad6a14362a76a2df673a1914b76715da79f233ce7b38425351419`  
		Last Modified: Tue, 12 Aug 2025 23:20:49 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2d87899848fdf17168f462257180eba7b9f0af14c8e7e6cf67ac1d62767a1327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151562670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4975da0824c5c96699fda1d1e4182c08b3a58f6b8d2064bfbeeb645bf8ed052d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 30 Jul 2025 00:49:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 30 Jul 2025 00:49:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV GOSU_VER=1.16
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Jul 2025 00:49:58 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c026c42412052a849302d1bc1a482c7b98fa2d12405b32c97adec0d9c56e3fe4`  
		Last Modified: Wed, 13 Aug 2025 07:22:09 GMT  
		Size: 9.6 MB (9604087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eee77d755dd2d844b449975406cc1e1c2908f0afcd9324d28c8aa0c70916a2a`  
		Last Modified: Wed, 13 Aug 2025 07:22:08 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab848f6b6270e3c24e7e67135ef9dace2ec1fc33044f6678689a82018cf191bc`  
		Last Modified: Wed, 13 Aug 2025 07:22:07 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9161c401ca944e27ae18c8bcd2dccc2391fb9fd6d1985e1a1e187491dbe0a69a`  
		Last Modified: Wed, 13 Aug 2025 07:22:08 GMT  
		Size: 938.9 KB (938872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ba89214edd2033d506033c5ec7fe54a46c771966ee15c8d6b58f1a36aad21b`  
		Last Modified: Wed, 13 Aug 2025 07:22:24 GMT  
		Size: 96.0 MB (96038357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4ef359ca1b842e78b94aad324b7e730a3b62744e613a42d5da5e722179a50a`  
		Last Modified: Wed, 13 Aug 2025 07:22:13 GMT  
		Size: 11.1 MB (11098980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ada0ae98a5739a0e1048827172476b7ed060163489d15ec64c503b3cf6b55aa`  
		Last Modified: Wed, 13 Aug 2025 07:22:09 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d345df6ce09d782b63b9aaa7ad325cafd46a7ba81ea5b58fd6bb8bc9160e2`  
		Last Modified: Wed, 13 Aug 2025 07:22:09 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4dd95daf0c07d74d01cac8f7a18a40b925e0d72a6e8409c48aa0551fa237c4`  
		Last Modified: Wed, 13 Aug 2025 07:22:10 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:b0da987852dee4a6b78680a77dc096b0600503d1dfaa9dc6d2504604329f04ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bed5658cab02aaa02b5cda753fd3ea271d88c3a0176c025491b327cf88ccc5`

```dockerfile
```

-	Layers:
	-	`sha256:c5a89415627d964a8e85936370549e0229c00c2ddcf2b59848caa52cc76554f4`  
		Last Modified: Wed, 13 Aug 2025 08:20:30 GMT  
		Size: 3.0 MB (2979001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842880aad603ccf0a2fd09aa6e78baec38e0aaf06cc65738fa777df3b6b0088f`  
		Last Modified: Wed, 13 Aug 2025 08:20:31 GMT  
		Size: 33.7 KB (33721 bytes)  
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
$ docker pull influxdb@sha256:59fe0181a3b161d36e9ce53001d7e1678762013ab0a284969ec2ebc517b529cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:b53805c0d05ab8d6dfc1443601ad539a1a395da0cb245bc771e487bff51345b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c43ca08192493c2c7a92559ab42c7ba3d7ca8820315d48ec1796a12c4a455`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 30 Jul 2025 00:49:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 30 Jul 2025 00:49:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV GOSU_VER=1.16
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Jul 2025 00:49:58 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d787a2de635a3059a66130180c8fc200a1b06c38135e8cd8092bc7be831ace62`  
		Last Modified: Tue, 12 Aug 2025 23:20:48 GMT  
		Size: 9.8 MB (9795849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3898caa9f81699d8c89fab840780c3e4ad1614949afc5ce26e4f7f4c0aff53d6`  
		Last Modified: Tue, 12 Aug 2025 23:20:48 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a784fc11f9cc8e18ae504d7e632e1939db12d92f983a2f2fa779a6ecca9c1d2`  
		Last Modified: Tue, 12 Aug 2025 22:58:11 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef6cfa01d55151e6bcf217da71c7f68545a5c18d96f9565242c69768b406265`  
		Last Modified: Tue, 12 Aug 2025 22:58:11 GMT  
		Size: 1.0 MB (1012033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0c0f100724b45479445b6b5d7c4a4d81379501181d0bcab57536fd0878359a`  
		Last Modified: Tue, 12 Aug 2025 23:20:51 GMT  
		Size: 100.2 MB (100242976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e3abb7a1c83e8e7d62bf3f915c57ce0c1bc7210cdc92072470a587fbaaced0`  
		Last Modified: Tue, 12 Aug 2025 23:20:49 GMT  
		Size: 11.8 MB (11773671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672405b61b597ccf9c47b82c19804743221a5c728b7283d286ceded23f96a3d7`  
		Last Modified: Tue, 12 Aug 2025 22:58:10 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fb7af7503dcb240d9098512683f3ab6cfe53693042dcfb4ad4791438537855`  
		Last Modified: Tue, 12 Aug 2025 22:58:10 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15b9d9b72b45d2fd3c4b139e6ce2bce52ff022fe54fa1a42d3f3e4161e3e695`  
		Last Modified: Tue, 12 Aug 2025 22:58:11 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:41c53b569e3968e48c2e3fb0bad86c21eaa53afbc1219b275999868e500cb471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870727706d286cdb78d544afb60f0642a9075e7ec604b54f50a428e860f7b4cf`

```dockerfile
```

-	Layers:
	-	`sha256:833fa77c36bca1fe044b59077abcaa17c696946bc525d08f30d929e096b99a01`  
		Last Modified: Tue, 12 Aug 2025 23:20:48 GMT  
		Size: 3.0 MB (2979773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:102e59daf6dad6a14362a76a2df673a1914b76715da79f233ce7b38425351419`  
		Last Modified: Tue, 12 Aug 2025 23:20:49 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2d87899848fdf17168f462257180eba7b9f0af14c8e7e6cf67ac1d62767a1327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151562670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4975da0824c5c96699fda1d1e4182c08b3a58f6b8d2064bfbeeb645bf8ed052d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 30 Jul 2025 00:49:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 30 Jul 2025 00:49:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV GOSU_VER=1.16
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Jul 2025 00:49:58 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c026c42412052a849302d1bc1a482c7b98fa2d12405b32c97adec0d9c56e3fe4`  
		Last Modified: Wed, 13 Aug 2025 07:22:09 GMT  
		Size: 9.6 MB (9604087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eee77d755dd2d844b449975406cc1e1c2908f0afcd9324d28c8aa0c70916a2a`  
		Last Modified: Wed, 13 Aug 2025 07:22:08 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab848f6b6270e3c24e7e67135ef9dace2ec1fc33044f6678689a82018cf191bc`  
		Last Modified: Wed, 13 Aug 2025 07:22:07 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9161c401ca944e27ae18c8bcd2dccc2391fb9fd6d1985e1a1e187491dbe0a69a`  
		Last Modified: Wed, 13 Aug 2025 07:22:08 GMT  
		Size: 938.9 KB (938872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ba89214edd2033d506033c5ec7fe54a46c771966ee15c8d6b58f1a36aad21b`  
		Last Modified: Wed, 13 Aug 2025 07:22:24 GMT  
		Size: 96.0 MB (96038357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4ef359ca1b842e78b94aad324b7e730a3b62744e613a42d5da5e722179a50a`  
		Last Modified: Wed, 13 Aug 2025 07:22:13 GMT  
		Size: 11.1 MB (11098980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ada0ae98a5739a0e1048827172476b7ed060163489d15ec64c503b3cf6b55aa`  
		Last Modified: Wed, 13 Aug 2025 07:22:09 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d345df6ce09d782b63b9aaa7ad325cafd46a7ba81ea5b58fd6bb8bc9160e2`  
		Last Modified: Wed, 13 Aug 2025 07:22:09 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4dd95daf0c07d74d01cac8f7a18a40b925e0d72a6e8409c48aa0551fa237c4`  
		Last Modified: Wed, 13 Aug 2025 07:22:10 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:b0da987852dee4a6b78680a77dc096b0600503d1dfaa9dc6d2504604329f04ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bed5658cab02aaa02b5cda753fd3ea271d88c3a0176c025491b327cf88ccc5`

```dockerfile
```

-	Layers:
	-	`sha256:c5a89415627d964a8e85936370549e0229c00c2ddcf2b59848caa52cc76554f4`  
		Last Modified: Wed, 13 Aug 2025 08:20:30 GMT  
		Size: 3.0 MB (2979001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842880aad603ccf0a2fd09aa6e78baec38e0aaf06cc65738fa777df3b6b0088f`  
		Last Modified: Wed, 13 Aug 2025 08:20:31 GMT  
		Size: 33.7 KB (33721 bytes)  
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
$ docker pull influxdb@sha256:59fe0181a3b161d36e9ce53001d7e1678762013ab0a284969ec2ebc517b529cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:b53805c0d05ab8d6dfc1443601ad539a1a395da0cb245bc771e487bff51345b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c43ca08192493c2c7a92559ab42c7ba3d7ca8820315d48ec1796a12c4a455`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 30 Jul 2025 00:49:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 30 Jul 2025 00:49:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV GOSU_VER=1.16
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Jul 2025 00:49:58 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d787a2de635a3059a66130180c8fc200a1b06c38135e8cd8092bc7be831ace62`  
		Last Modified: Tue, 12 Aug 2025 23:20:48 GMT  
		Size: 9.8 MB (9795849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3898caa9f81699d8c89fab840780c3e4ad1614949afc5ce26e4f7f4c0aff53d6`  
		Last Modified: Tue, 12 Aug 2025 23:20:48 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a784fc11f9cc8e18ae504d7e632e1939db12d92f983a2f2fa779a6ecca9c1d2`  
		Last Modified: Tue, 12 Aug 2025 22:58:11 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef6cfa01d55151e6bcf217da71c7f68545a5c18d96f9565242c69768b406265`  
		Last Modified: Tue, 12 Aug 2025 22:58:11 GMT  
		Size: 1.0 MB (1012033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0c0f100724b45479445b6b5d7c4a4d81379501181d0bcab57536fd0878359a`  
		Last Modified: Tue, 12 Aug 2025 23:20:51 GMT  
		Size: 100.2 MB (100242976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e3abb7a1c83e8e7d62bf3f915c57ce0c1bc7210cdc92072470a587fbaaced0`  
		Last Modified: Tue, 12 Aug 2025 23:20:49 GMT  
		Size: 11.8 MB (11773671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672405b61b597ccf9c47b82c19804743221a5c728b7283d286ceded23f96a3d7`  
		Last Modified: Tue, 12 Aug 2025 22:58:10 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fb7af7503dcb240d9098512683f3ab6cfe53693042dcfb4ad4791438537855`  
		Last Modified: Tue, 12 Aug 2025 22:58:10 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15b9d9b72b45d2fd3c4b139e6ce2bce52ff022fe54fa1a42d3f3e4161e3e695`  
		Last Modified: Tue, 12 Aug 2025 22:58:11 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:41c53b569e3968e48c2e3fb0bad86c21eaa53afbc1219b275999868e500cb471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870727706d286cdb78d544afb60f0642a9075e7ec604b54f50a428e860f7b4cf`

```dockerfile
```

-	Layers:
	-	`sha256:833fa77c36bca1fe044b59077abcaa17c696946bc525d08f30d929e096b99a01`  
		Last Modified: Tue, 12 Aug 2025 23:20:48 GMT  
		Size: 3.0 MB (2979773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:102e59daf6dad6a14362a76a2df673a1914b76715da79f233ce7b38425351419`  
		Last Modified: Tue, 12 Aug 2025 23:20:49 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2d87899848fdf17168f462257180eba7b9f0af14c8e7e6cf67ac1d62767a1327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151562670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4975da0824c5c96699fda1d1e4182c08b3a58f6b8d2064bfbeeb645bf8ed052d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 30 Jul 2025 00:49:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 30 Jul 2025 00:49:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV GOSU_VER=1.16
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Jul 2025 00:49:58 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c026c42412052a849302d1bc1a482c7b98fa2d12405b32c97adec0d9c56e3fe4`  
		Last Modified: Wed, 13 Aug 2025 07:22:09 GMT  
		Size: 9.6 MB (9604087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eee77d755dd2d844b449975406cc1e1c2908f0afcd9324d28c8aa0c70916a2a`  
		Last Modified: Wed, 13 Aug 2025 07:22:08 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab848f6b6270e3c24e7e67135ef9dace2ec1fc33044f6678689a82018cf191bc`  
		Last Modified: Wed, 13 Aug 2025 07:22:07 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9161c401ca944e27ae18c8bcd2dccc2391fb9fd6d1985e1a1e187491dbe0a69a`  
		Last Modified: Wed, 13 Aug 2025 07:22:08 GMT  
		Size: 938.9 KB (938872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ba89214edd2033d506033c5ec7fe54a46c771966ee15c8d6b58f1a36aad21b`  
		Last Modified: Wed, 13 Aug 2025 07:22:24 GMT  
		Size: 96.0 MB (96038357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4ef359ca1b842e78b94aad324b7e730a3b62744e613a42d5da5e722179a50a`  
		Last Modified: Wed, 13 Aug 2025 07:22:13 GMT  
		Size: 11.1 MB (11098980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ada0ae98a5739a0e1048827172476b7ed060163489d15ec64c503b3cf6b55aa`  
		Last Modified: Wed, 13 Aug 2025 07:22:09 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d345df6ce09d782b63b9aaa7ad325cafd46a7ba81ea5b58fd6bb8bc9160e2`  
		Last Modified: Wed, 13 Aug 2025 07:22:09 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4dd95daf0c07d74d01cac8f7a18a40b925e0d72a6e8409c48aa0551fa237c4`  
		Last Modified: Wed, 13 Aug 2025 07:22:10 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:b0da987852dee4a6b78680a77dc096b0600503d1dfaa9dc6d2504604329f04ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bed5658cab02aaa02b5cda753fd3ea271d88c3a0176c025491b327cf88ccc5`

```dockerfile
```

-	Layers:
	-	`sha256:c5a89415627d964a8e85936370549e0229c00c2ddcf2b59848caa52cc76554f4`  
		Last Modified: Wed, 13 Aug 2025 08:20:30 GMT  
		Size: 3.0 MB (2979001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842880aad603ccf0a2fd09aa6e78baec38e0aaf06cc65738fa777df3b6b0088f`  
		Last Modified: Wed, 13 Aug 2025 08:20:31 GMT  
		Size: 33.7 KB (33721 bytes)  
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
$ docker pull influxdb@sha256:49865a86159adc2aabb4199785c12afb2cabfa85e4a36f332a5c2891d3ba82ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:13f0b4dcdfd71cfd0fd16e2cb2c9128fdc25e45741c157d9a8766c2542b0b73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115974556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b059bf14de933fe57d323952d5a7012e8e2e8894ce1546633d2130613d7799cf`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cdfc8a1d408d8810643874b24d2a77e76638768a9403b94e7084789a41e2df`  
		Last Modified: Wed, 27 Aug 2025 17:20:37 GMT  
		Size: 6.7 MB (6665822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc452c623f024a6dffab2ed0eda980e28c6d6ae3b7b1e0311694778d30d4f781`  
		Last Modified: Wed, 27 Aug 2025 17:02:37 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5eb169ed24a9802925f19ea9f07900c37d85cae68c28faed075a11bead7997`  
		Last Modified: Wed, 27 Aug 2025 17:20:54 GMT  
		Size: 79.6 MB (79581394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478a741c27067a815444a0d3f4a2ccbb14af5100de237b679788fba32ee790f8`  
		Last Modified: Wed, 27 Aug 2025 17:02:40 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0389d5878b7e1b2ff6d8c5a6effbfa01672ece1f5827e4176afe4be98ee04fc3`  
		Last Modified: Wed, 27 Aug 2025 17:02:43 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:1d66b71fcdb18933ce34ed1c4830ca7f30b76df80d7a22fbf47236ed2c54c80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d41c14677a4716cb29765e9a346bd137b68e28d80a69b97109fcca43ad61e4`

```dockerfile
```

-	Layers:
	-	`sha256:e295deba1a642908561f74f1dcf989c36a5cfda50a3167062c6e5f9f4c64d66a`  
		Last Modified: Wed, 27 Aug 2025 17:20:36 GMT  
		Size: 2.3 MB (2311325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dc157fccebd69cc970178ab6004dd24389f3cb6e4dcc4b5f1bc23854f51a4ed`  
		Last Modified: Wed, 27 Aug 2025 17:20:36 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:43013d277870eeb121bb131657cb487330f6ef6c485e802a5583dcd2b1086224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106731706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec39a2e38e137ea62b13d26c70bdd0824c52d0f0dbfbb6f10be600b7ec2131f9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8628ffec9dda4bc049719755d628560ca16ac61364a101ff6c22478848e1806`  
		Last Modified: Wed, 27 Aug 2025 17:02:54 GMT  
		Size: 6.7 MB (6676366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432ca6bd3af57def5016ada52bbb59e768669a06687a6c4b3bed81b95299952d`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d79e94db37660a93066252beae47907c1fba67b47132eef0cc879f6f015ee3`  
		Last Modified: Wed, 27 Aug 2025 17:13:02 GMT  
		Size: 71.2 MB (71190828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a780ca8b6a0885ae430b6c5d71d8688a1b0e8687bcb8d7b64333b27eddf401`  
		Last Modified: Wed, 27 Aug 2025 17:12:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e3d87a0335d0b53598505c2c7bfdaf4f90bf198e86681990ed0209aaca8e20`  
		Last Modified: Wed, 27 Aug 2025 17:12:32 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:03579e42dab4c8c538725fb63fdc69996194041d7baaadd511e82b2dd8f89086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8aa42aac4dcc06e62b2dde25dc5c14119d1f52315181350d7306e6c142a35b`

```dockerfile
```

-	Layers:
	-	`sha256:8571a28cbd628d61724e7ea72c51900f8e636954510199e2ff0c656fea32a2d9`  
		Last Modified: Wed, 27 Aug 2025 20:20:30 GMT  
		Size: 2.3 MB (2312407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a0830961173158d014f9819f35cd7061fd439b0e26553104146b6d60bb5040`  
		Last Modified: Wed, 27 Aug 2025 20:20:31 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:836b684bace36fe0b4949e06d92dd8a128610b172cd05db7f71748b7bcf7c6a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:b4f9c35de188dc1bb4462653afeb09532ed777f8ef2a8a4e09f1de8211e1e5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121175418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5707e1f389aa1d8fad1e509ae59c199f8420eca6c2cd6ed7107a69a68a37d73`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3272ce2eee08ecb6f0369231e760aac7686371309745bd558dcd9069d459fd31`  
		Last Modified: Wed, 27 Aug 2025 17:20:44 GMT  
		Size: 6.7 MB (6665919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9b54db7f1cf80ca69f09dded7e4ba1ae7a5412826a08fec04efd0839aca6e0`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9413c7bf58876e45a7561210d0799857f190304c806684b8ba02618c8232fe`  
		Last Modified: Wed, 27 Aug 2025 17:20:58 GMT  
		Size: 84.8 MB (84782153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0a7808357ee36cccd09ea2bcb39fa6b2a92885c8f226483a81aa708b6fcd09`  
		Last Modified: Wed, 27 Aug 2025 17:02:58 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8387b6e0d8e41d716ae36f06a42f2512ea0473a901551a0b6f0dd9120bcbaee`  
		Last Modified: Wed, 27 Aug 2025 17:03:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:d004ec1867494a91c026a1252fcae00fb109d1a8269c45c674d5e381de9f2991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15f7d58860988ef4d8e44be0e91fd5c114497d551958ced04d5ce34195ba02b`

```dockerfile
```

-	Layers:
	-	`sha256:3645f91cd44dc82ce3651c2d792dc438ed8c23beac0a82b970d08c2585c4169b`  
		Last Modified: Wed, 27 Aug 2025 17:20:37 GMT  
		Size: 2.3 MB (2311373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48f8b4ec384dd47f4f5dffbce59b6310e7a4cbd33c1c520e045e1e643b95c424`  
		Last Modified: Wed, 27 Aug 2025 17:20:38 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f1f251f053c53c148bbb84d7726d719e725986fc886330a00b7fd7e145227d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111853246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8aa50a8435e9832d0e12b02590ac02d0c6409ffc51c3473856a87aa2aa2bc4`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8628ffec9dda4bc049719755d628560ca16ac61364a101ff6c22478848e1806`  
		Last Modified: Wed, 27 Aug 2025 17:02:54 GMT  
		Size: 6.7 MB (6676366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432ca6bd3af57def5016ada52bbb59e768669a06687a6c4b3bed81b95299952d`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abad28f90cfd07ae2a34346f534f0a5afa3f2ba1808ca6e188ac9c1e98be7171`  
		Last Modified: Wed, 27 Aug 2025 17:03:02 GMT  
		Size: 76.3 MB (76312368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab21b027a1b91134863f0d6a8b0280defda9e18b27c6ff7dcfe45b94d481d663`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a834f37dd732c0c9d9c6642f3d91c1d86a731d30bf5daa86ec2c477b3cddf95`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:692d56b80cade7cfac47d3b76427653e6444d222446943f72fe932572b961fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad5d878640e4ee213646beabdbd456adcbd69f0edf5fbfba2f702a98b5349b3`

```dockerfile
```

-	Layers:
	-	`sha256:f0de14be245955e27425063a3aa8640a256813fec0ec831f32483765689df663`  
		Last Modified: Wed, 27 Aug 2025 17:20:42 GMT  
		Size: 2.3 MB (2312455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3826b90ba182cf0fef86bdac9486bff26094964668218dcabc8efa7ca68c2acf`  
		Last Modified: Wed, 27 Aug 2025 17:20:43 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.4-core`

```console
$ docker pull influxdb@sha256:49865a86159adc2aabb4199785c12afb2cabfa85e4a36f332a5c2891d3ba82ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.4-core` - linux; amd64

```console
$ docker pull influxdb@sha256:13f0b4dcdfd71cfd0fd16e2cb2c9128fdc25e45741c157d9a8766c2542b0b73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115974556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b059bf14de933fe57d323952d5a7012e8e2e8894ce1546633d2130613d7799cf`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cdfc8a1d408d8810643874b24d2a77e76638768a9403b94e7084789a41e2df`  
		Last Modified: Wed, 27 Aug 2025 17:20:37 GMT  
		Size: 6.7 MB (6665822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc452c623f024a6dffab2ed0eda980e28c6d6ae3b7b1e0311694778d30d4f781`  
		Last Modified: Wed, 27 Aug 2025 17:02:37 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5eb169ed24a9802925f19ea9f07900c37d85cae68c28faed075a11bead7997`  
		Last Modified: Wed, 27 Aug 2025 17:20:54 GMT  
		Size: 79.6 MB (79581394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478a741c27067a815444a0d3f4a2ccbb14af5100de237b679788fba32ee790f8`  
		Last Modified: Wed, 27 Aug 2025 17:02:40 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0389d5878b7e1b2ff6d8c5a6effbfa01672ece1f5827e4176afe4be98ee04fc3`  
		Last Modified: Wed, 27 Aug 2025 17:02:43 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:1d66b71fcdb18933ce34ed1c4830ca7f30b76df80d7a22fbf47236ed2c54c80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d41c14677a4716cb29765e9a346bd137b68e28d80a69b97109fcca43ad61e4`

```dockerfile
```

-	Layers:
	-	`sha256:e295deba1a642908561f74f1dcf989c36a5cfda50a3167062c6e5f9f4c64d66a`  
		Last Modified: Wed, 27 Aug 2025 17:20:36 GMT  
		Size: 2.3 MB (2311325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dc157fccebd69cc970178ab6004dd24389f3cb6e4dcc4b5f1bc23854f51a4ed`  
		Last Modified: Wed, 27 Aug 2025 17:20:36 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.4-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:43013d277870eeb121bb131657cb487330f6ef6c485e802a5583dcd2b1086224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106731706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec39a2e38e137ea62b13d26c70bdd0824c52d0f0dbfbb6f10be600b7ec2131f9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8628ffec9dda4bc049719755d628560ca16ac61364a101ff6c22478848e1806`  
		Last Modified: Wed, 27 Aug 2025 17:02:54 GMT  
		Size: 6.7 MB (6676366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432ca6bd3af57def5016ada52bbb59e768669a06687a6c4b3bed81b95299952d`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d79e94db37660a93066252beae47907c1fba67b47132eef0cc879f6f015ee3`  
		Last Modified: Wed, 27 Aug 2025 17:13:02 GMT  
		Size: 71.2 MB (71190828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a780ca8b6a0885ae430b6c5d71d8688a1b0e8687bcb8d7b64333b27eddf401`  
		Last Modified: Wed, 27 Aug 2025 17:12:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e3d87a0335d0b53598505c2c7bfdaf4f90bf198e86681990ed0209aaca8e20`  
		Last Modified: Wed, 27 Aug 2025 17:12:32 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:03579e42dab4c8c538725fb63fdc69996194041d7baaadd511e82b2dd8f89086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8aa42aac4dcc06e62b2dde25dc5c14119d1f52315181350d7306e6c142a35b`

```dockerfile
```

-	Layers:
	-	`sha256:8571a28cbd628d61724e7ea72c51900f8e636954510199e2ff0c656fea32a2d9`  
		Last Modified: Wed, 27 Aug 2025 20:20:30 GMT  
		Size: 2.3 MB (2312407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a0830961173158d014f9819f35cd7061fd439b0e26553104146b6d60bb5040`  
		Last Modified: Wed, 27 Aug 2025 20:20:31 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.4-enterprise`

```console
$ docker pull influxdb@sha256:836b684bace36fe0b4949e06d92dd8a128610b172cd05db7f71748b7bcf7c6a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.4-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:b4f9c35de188dc1bb4462653afeb09532ed777f8ef2a8a4e09f1de8211e1e5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121175418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5707e1f389aa1d8fad1e509ae59c199f8420eca6c2cd6ed7107a69a68a37d73`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3272ce2eee08ecb6f0369231e760aac7686371309745bd558dcd9069d459fd31`  
		Last Modified: Wed, 27 Aug 2025 17:20:44 GMT  
		Size: 6.7 MB (6665919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9b54db7f1cf80ca69f09dded7e4ba1ae7a5412826a08fec04efd0839aca6e0`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9413c7bf58876e45a7561210d0799857f190304c806684b8ba02618c8232fe`  
		Last Modified: Wed, 27 Aug 2025 17:20:58 GMT  
		Size: 84.8 MB (84782153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0a7808357ee36cccd09ea2bcb39fa6b2a92885c8f226483a81aa708b6fcd09`  
		Last Modified: Wed, 27 Aug 2025 17:02:58 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8387b6e0d8e41d716ae36f06a42f2512ea0473a901551a0b6f0dd9120bcbaee`  
		Last Modified: Wed, 27 Aug 2025 17:03:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:d004ec1867494a91c026a1252fcae00fb109d1a8269c45c674d5e381de9f2991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15f7d58860988ef4d8e44be0e91fd5c114497d551958ced04d5ce34195ba02b`

```dockerfile
```

-	Layers:
	-	`sha256:3645f91cd44dc82ce3651c2d792dc438ed8c23beac0a82b970d08c2585c4169b`  
		Last Modified: Wed, 27 Aug 2025 17:20:37 GMT  
		Size: 2.3 MB (2311373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48f8b4ec384dd47f4f5dffbce59b6310e7a4cbd33c1c520e045e1e643b95c424`  
		Last Modified: Wed, 27 Aug 2025 17:20:38 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f1f251f053c53c148bbb84d7726d719e725986fc886330a00b7fd7e145227d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111853246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8aa50a8435e9832d0e12b02590ac02d0c6409ffc51c3473856a87aa2aa2bc4`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8628ffec9dda4bc049719755d628560ca16ac61364a101ff6c22478848e1806`  
		Last Modified: Wed, 27 Aug 2025 17:02:54 GMT  
		Size: 6.7 MB (6676366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432ca6bd3af57def5016ada52bbb59e768669a06687a6c4b3bed81b95299952d`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abad28f90cfd07ae2a34346f534f0a5afa3f2ba1808ca6e188ac9c1e98be7171`  
		Last Modified: Wed, 27 Aug 2025 17:03:02 GMT  
		Size: 76.3 MB (76312368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab21b027a1b91134863f0d6a8b0280defda9e18b27c6ff7dcfe45b94d481d663`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a834f37dd732c0c9d9c6642f3d91c1d86a731d30bf5daa86ec2c477b3cddf95`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:692d56b80cade7cfac47d3b76427653e6444d222446943f72fe932572b961fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad5d878640e4ee213646beabdbd456adcbd69f0edf5fbfba2f702a98b5349b3`

```dockerfile
```

-	Layers:
	-	`sha256:f0de14be245955e27425063a3aa8640a256813fec0ec831f32483765689df663`  
		Last Modified: Wed, 27 Aug 2025 17:20:42 GMT  
		Size: 2.3 MB (2312455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3826b90ba182cf0fef86bdac9486bff26094964668218dcabc8efa7ca68c2acf`  
		Last Modified: Wed, 27 Aug 2025 17:20:43 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.4.0-core`

```console
$ docker pull influxdb@sha256:49865a86159adc2aabb4199785c12afb2cabfa85e4a36f332a5c2891d3ba82ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.4.0-core` - linux; amd64

```console
$ docker pull influxdb@sha256:13f0b4dcdfd71cfd0fd16e2cb2c9128fdc25e45741c157d9a8766c2542b0b73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115974556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b059bf14de933fe57d323952d5a7012e8e2e8894ce1546633d2130613d7799cf`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cdfc8a1d408d8810643874b24d2a77e76638768a9403b94e7084789a41e2df`  
		Last Modified: Wed, 27 Aug 2025 17:20:37 GMT  
		Size: 6.7 MB (6665822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc452c623f024a6dffab2ed0eda980e28c6d6ae3b7b1e0311694778d30d4f781`  
		Last Modified: Wed, 27 Aug 2025 17:02:37 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5eb169ed24a9802925f19ea9f07900c37d85cae68c28faed075a11bead7997`  
		Last Modified: Wed, 27 Aug 2025 17:20:54 GMT  
		Size: 79.6 MB (79581394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478a741c27067a815444a0d3f4a2ccbb14af5100de237b679788fba32ee790f8`  
		Last Modified: Wed, 27 Aug 2025 17:02:40 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0389d5878b7e1b2ff6d8c5a6effbfa01672ece1f5827e4176afe4be98ee04fc3`  
		Last Modified: Wed, 27 Aug 2025 17:02:43 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:1d66b71fcdb18933ce34ed1c4830ca7f30b76df80d7a22fbf47236ed2c54c80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d41c14677a4716cb29765e9a346bd137b68e28d80a69b97109fcca43ad61e4`

```dockerfile
```

-	Layers:
	-	`sha256:e295deba1a642908561f74f1dcf989c36a5cfda50a3167062c6e5f9f4c64d66a`  
		Last Modified: Wed, 27 Aug 2025 17:20:36 GMT  
		Size: 2.3 MB (2311325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dc157fccebd69cc970178ab6004dd24389f3cb6e4dcc4b5f1bc23854f51a4ed`  
		Last Modified: Wed, 27 Aug 2025 17:20:36 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.4.0-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:43013d277870eeb121bb131657cb487330f6ef6c485e802a5583dcd2b1086224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106731706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec39a2e38e137ea62b13d26c70bdd0824c52d0f0dbfbb6f10be600b7ec2131f9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8628ffec9dda4bc049719755d628560ca16ac61364a101ff6c22478848e1806`  
		Last Modified: Wed, 27 Aug 2025 17:02:54 GMT  
		Size: 6.7 MB (6676366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432ca6bd3af57def5016ada52bbb59e768669a06687a6c4b3bed81b95299952d`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d79e94db37660a93066252beae47907c1fba67b47132eef0cc879f6f015ee3`  
		Last Modified: Wed, 27 Aug 2025 17:13:02 GMT  
		Size: 71.2 MB (71190828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a780ca8b6a0885ae430b6c5d71d8688a1b0e8687bcb8d7b64333b27eddf401`  
		Last Modified: Wed, 27 Aug 2025 17:12:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e3d87a0335d0b53598505c2c7bfdaf4f90bf198e86681990ed0209aaca8e20`  
		Last Modified: Wed, 27 Aug 2025 17:12:32 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:03579e42dab4c8c538725fb63fdc69996194041d7baaadd511e82b2dd8f89086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8aa42aac4dcc06e62b2dde25dc5c14119d1f52315181350d7306e6c142a35b`

```dockerfile
```

-	Layers:
	-	`sha256:8571a28cbd628d61724e7ea72c51900f8e636954510199e2ff0c656fea32a2d9`  
		Last Modified: Wed, 27 Aug 2025 20:20:30 GMT  
		Size: 2.3 MB (2312407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a0830961173158d014f9819f35cd7061fd439b0e26553104146b6d60bb5040`  
		Last Modified: Wed, 27 Aug 2025 20:20:31 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.4.0-enterprise`

```console
$ docker pull influxdb@sha256:836b684bace36fe0b4949e06d92dd8a128610b172cd05db7f71748b7bcf7c6a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.4.0-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:b4f9c35de188dc1bb4462653afeb09532ed777f8ef2a8a4e09f1de8211e1e5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121175418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5707e1f389aa1d8fad1e509ae59c199f8420eca6c2cd6ed7107a69a68a37d73`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3272ce2eee08ecb6f0369231e760aac7686371309745bd558dcd9069d459fd31`  
		Last Modified: Wed, 27 Aug 2025 17:20:44 GMT  
		Size: 6.7 MB (6665919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9b54db7f1cf80ca69f09dded7e4ba1ae7a5412826a08fec04efd0839aca6e0`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9413c7bf58876e45a7561210d0799857f190304c806684b8ba02618c8232fe`  
		Last Modified: Wed, 27 Aug 2025 17:20:58 GMT  
		Size: 84.8 MB (84782153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0a7808357ee36cccd09ea2bcb39fa6b2a92885c8f226483a81aa708b6fcd09`  
		Last Modified: Wed, 27 Aug 2025 17:02:58 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8387b6e0d8e41d716ae36f06a42f2512ea0473a901551a0b6f0dd9120bcbaee`  
		Last Modified: Wed, 27 Aug 2025 17:03:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:d004ec1867494a91c026a1252fcae00fb109d1a8269c45c674d5e381de9f2991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15f7d58860988ef4d8e44be0e91fd5c114497d551958ced04d5ce34195ba02b`

```dockerfile
```

-	Layers:
	-	`sha256:3645f91cd44dc82ce3651c2d792dc438ed8c23beac0a82b970d08c2585c4169b`  
		Last Modified: Wed, 27 Aug 2025 17:20:37 GMT  
		Size: 2.3 MB (2311373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48f8b4ec384dd47f4f5dffbce59b6310e7a4cbd33c1c520e045e1e643b95c424`  
		Last Modified: Wed, 27 Aug 2025 17:20:38 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.4.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f1f251f053c53c148bbb84d7726d719e725986fc886330a00b7fd7e145227d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111853246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8aa50a8435e9832d0e12b02590ac02d0c6409ffc51c3473856a87aa2aa2bc4`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8628ffec9dda4bc049719755d628560ca16ac61364a101ff6c22478848e1806`  
		Last Modified: Wed, 27 Aug 2025 17:02:54 GMT  
		Size: 6.7 MB (6676366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432ca6bd3af57def5016ada52bbb59e768669a06687a6c4b3bed81b95299952d`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abad28f90cfd07ae2a34346f534f0a5afa3f2ba1808ca6e188ac9c1e98be7171`  
		Last Modified: Wed, 27 Aug 2025 17:03:02 GMT  
		Size: 76.3 MB (76312368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab21b027a1b91134863f0d6a8b0280defda9e18b27c6ff7dcfe45b94d481d663`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a834f37dd732c0c9d9c6642f3d91c1d86a731d30bf5daa86ec2c477b3cddf95`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.4.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:692d56b80cade7cfac47d3b76427653e6444d222446943f72fe932572b961fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad5d878640e4ee213646beabdbd456adcbd69f0edf5fbfba2f702a98b5349b3`

```dockerfile
```

-	Layers:
	-	`sha256:f0de14be245955e27425063a3aa8640a256813fec0ec831f32483765689df663`  
		Last Modified: Wed, 27 Aug 2025 17:20:42 GMT  
		Size: 2.3 MB (2312455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3826b90ba182cf0fef86bdac9486bff26094964668218dcabc8efa7ca68c2acf`  
		Last Modified: Wed, 27 Aug 2025 17:20:43 GMT  
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
$ docker pull influxdb@sha256:49865a86159adc2aabb4199785c12afb2cabfa85e4a36f332a5c2891d3ba82ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:13f0b4dcdfd71cfd0fd16e2cb2c9128fdc25e45741c157d9a8766c2542b0b73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115974556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b059bf14de933fe57d323952d5a7012e8e2e8894ce1546633d2130613d7799cf`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cdfc8a1d408d8810643874b24d2a77e76638768a9403b94e7084789a41e2df`  
		Last Modified: Wed, 27 Aug 2025 17:20:37 GMT  
		Size: 6.7 MB (6665822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc452c623f024a6dffab2ed0eda980e28c6d6ae3b7b1e0311694778d30d4f781`  
		Last Modified: Wed, 27 Aug 2025 17:02:37 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5eb169ed24a9802925f19ea9f07900c37d85cae68c28faed075a11bead7997`  
		Last Modified: Wed, 27 Aug 2025 17:20:54 GMT  
		Size: 79.6 MB (79581394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478a741c27067a815444a0d3f4a2ccbb14af5100de237b679788fba32ee790f8`  
		Last Modified: Wed, 27 Aug 2025 17:02:40 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0389d5878b7e1b2ff6d8c5a6effbfa01672ece1f5827e4176afe4be98ee04fc3`  
		Last Modified: Wed, 27 Aug 2025 17:02:43 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:1d66b71fcdb18933ce34ed1c4830ca7f30b76df80d7a22fbf47236ed2c54c80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d41c14677a4716cb29765e9a346bd137b68e28d80a69b97109fcca43ad61e4`

```dockerfile
```

-	Layers:
	-	`sha256:e295deba1a642908561f74f1dcf989c36a5cfda50a3167062c6e5f9f4c64d66a`  
		Last Modified: Wed, 27 Aug 2025 17:20:36 GMT  
		Size: 2.3 MB (2311325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dc157fccebd69cc970178ab6004dd24389f3cb6e4dcc4b5f1bc23854f51a4ed`  
		Last Modified: Wed, 27 Aug 2025 17:20:36 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:43013d277870eeb121bb131657cb487330f6ef6c485e802a5583dcd2b1086224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106731706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec39a2e38e137ea62b13d26c70bdd0824c52d0f0dbfbb6f10be600b7ec2131f9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8628ffec9dda4bc049719755d628560ca16ac61364a101ff6c22478848e1806`  
		Last Modified: Wed, 27 Aug 2025 17:02:54 GMT  
		Size: 6.7 MB (6676366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432ca6bd3af57def5016ada52bbb59e768669a06687a6c4b3bed81b95299952d`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d79e94db37660a93066252beae47907c1fba67b47132eef0cc879f6f015ee3`  
		Last Modified: Wed, 27 Aug 2025 17:13:02 GMT  
		Size: 71.2 MB (71190828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a780ca8b6a0885ae430b6c5d71d8688a1b0e8687bcb8d7b64333b27eddf401`  
		Last Modified: Wed, 27 Aug 2025 17:12:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e3d87a0335d0b53598505c2c7bfdaf4f90bf198e86681990ed0209aaca8e20`  
		Last Modified: Wed, 27 Aug 2025 17:12:32 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:03579e42dab4c8c538725fb63fdc69996194041d7baaadd511e82b2dd8f89086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8aa42aac4dcc06e62b2dde25dc5c14119d1f52315181350d7306e6c142a35b`

```dockerfile
```

-	Layers:
	-	`sha256:8571a28cbd628d61724e7ea72c51900f8e636954510199e2ff0c656fea32a2d9`  
		Last Modified: Wed, 27 Aug 2025 20:20:30 GMT  
		Size: 2.3 MB (2312407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a0830961173158d014f9819f35cd7061fd439b0e26553104146b6d60bb5040`  
		Last Modified: Wed, 27 Aug 2025 20:20:31 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:836b684bace36fe0b4949e06d92dd8a128610b172cd05db7f71748b7bcf7c6a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:b4f9c35de188dc1bb4462653afeb09532ed777f8ef2a8a4e09f1de8211e1e5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121175418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5707e1f389aa1d8fad1e509ae59c199f8420eca6c2cd6ed7107a69a68a37d73`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3272ce2eee08ecb6f0369231e760aac7686371309745bd558dcd9069d459fd31`  
		Last Modified: Wed, 27 Aug 2025 17:20:44 GMT  
		Size: 6.7 MB (6665919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9b54db7f1cf80ca69f09dded7e4ba1ae7a5412826a08fec04efd0839aca6e0`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9413c7bf58876e45a7561210d0799857f190304c806684b8ba02618c8232fe`  
		Last Modified: Wed, 27 Aug 2025 17:20:58 GMT  
		Size: 84.8 MB (84782153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0a7808357ee36cccd09ea2bcb39fa6b2a92885c8f226483a81aa708b6fcd09`  
		Last Modified: Wed, 27 Aug 2025 17:02:58 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8387b6e0d8e41d716ae36f06a42f2512ea0473a901551a0b6f0dd9120bcbaee`  
		Last Modified: Wed, 27 Aug 2025 17:03:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:d004ec1867494a91c026a1252fcae00fb109d1a8269c45c674d5e381de9f2991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15f7d58860988ef4d8e44be0e91fd5c114497d551958ced04d5ce34195ba02b`

```dockerfile
```

-	Layers:
	-	`sha256:3645f91cd44dc82ce3651c2d792dc438ed8c23beac0a82b970d08c2585c4169b`  
		Last Modified: Wed, 27 Aug 2025 17:20:37 GMT  
		Size: 2.3 MB (2311373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48f8b4ec384dd47f4f5dffbce59b6310e7a4cbd33c1c520e045e1e643b95c424`  
		Last Modified: Wed, 27 Aug 2025 17:20:38 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f1f251f053c53c148bbb84d7726d719e725986fc886330a00b7fd7e145227d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111853246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8aa50a8435e9832d0e12b02590ac02d0c6409ffc51c3473856a87aa2aa2bc4`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8628ffec9dda4bc049719755d628560ca16ac61364a101ff6c22478848e1806`  
		Last Modified: Wed, 27 Aug 2025 17:02:54 GMT  
		Size: 6.7 MB (6676366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432ca6bd3af57def5016ada52bbb59e768669a06687a6c4b3bed81b95299952d`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abad28f90cfd07ae2a34346f534f0a5afa3f2ba1808ca6e188ac9c1e98be7171`  
		Last Modified: Wed, 27 Aug 2025 17:03:02 GMT  
		Size: 76.3 MB (76312368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab21b027a1b91134863f0d6a8b0280defda9e18b27c6ff7dcfe45b94d481d663`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a834f37dd732c0c9d9c6642f3d91c1d86a731d30bf5daa86ec2c477b3cddf95`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:692d56b80cade7cfac47d3b76427653e6444d222446943f72fe932572b961fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad5d878640e4ee213646beabdbd456adcbd69f0edf5fbfba2f702a98b5349b3`

```dockerfile
```

-	Layers:
	-	`sha256:f0de14be245955e27425063a3aa8640a256813fec0ec831f32483765689df663`  
		Last Modified: Wed, 27 Aug 2025 17:20:42 GMT  
		Size: 2.3 MB (2312455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3826b90ba182cf0fef86bdac9486bff26094964668218dcabc8efa7ca68c2acf`  
		Last Modified: Wed, 27 Aug 2025 17:20:43 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:59fe0181a3b161d36e9ce53001d7e1678762013ab0a284969ec2ebc517b529cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:b53805c0d05ab8d6dfc1443601ad539a1a395da0cb245bc771e487bff51345b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c43ca08192493c2c7a92559ab42c7ba3d7ca8820315d48ec1796a12c4a455`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 30 Jul 2025 00:49:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 30 Jul 2025 00:49:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV GOSU_VER=1.16
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Jul 2025 00:49:58 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d787a2de635a3059a66130180c8fc200a1b06c38135e8cd8092bc7be831ace62`  
		Last Modified: Tue, 12 Aug 2025 23:20:48 GMT  
		Size: 9.8 MB (9795849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3898caa9f81699d8c89fab840780c3e4ad1614949afc5ce26e4f7f4c0aff53d6`  
		Last Modified: Tue, 12 Aug 2025 23:20:48 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a784fc11f9cc8e18ae504d7e632e1939db12d92f983a2f2fa779a6ecca9c1d2`  
		Last Modified: Tue, 12 Aug 2025 22:58:11 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef6cfa01d55151e6bcf217da71c7f68545a5c18d96f9565242c69768b406265`  
		Last Modified: Tue, 12 Aug 2025 22:58:11 GMT  
		Size: 1.0 MB (1012033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0c0f100724b45479445b6b5d7c4a4d81379501181d0bcab57536fd0878359a`  
		Last Modified: Tue, 12 Aug 2025 23:20:51 GMT  
		Size: 100.2 MB (100242976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e3abb7a1c83e8e7d62bf3f915c57ce0c1bc7210cdc92072470a587fbaaced0`  
		Last Modified: Tue, 12 Aug 2025 23:20:49 GMT  
		Size: 11.8 MB (11773671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672405b61b597ccf9c47b82c19804743221a5c728b7283d286ceded23f96a3d7`  
		Last Modified: Tue, 12 Aug 2025 22:58:10 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fb7af7503dcb240d9098512683f3ab6cfe53693042dcfb4ad4791438537855`  
		Last Modified: Tue, 12 Aug 2025 22:58:10 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15b9d9b72b45d2fd3c4b139e6ce2bce52ff022fe54fa1a42d3f3e4161e3e695`  
		Last Modified: Tue, 12 Aug 2025 22:58:11 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:41c53b569e3968e48c2e3fb0bad86c21eaa53afbc1219b275999868e500cb471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870727706d286cdb78d544afb60f0642a9075e7ec604b54f50a428e860f7b4cf`

```dockerfile
```

-	Layers:
	-	`sha256:833fa77c36bca1fe044b59077abcaa17c696946bc525d08f30d929e096b99a01`  
		Last Modified: Tue, 12 Aug 2025 23:20:48 GMT  
		Size: 3.0 MB (2979773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:102e59daf6dad6a14362a76a2df673a1914b76715da79f233ce7b38425351419`  
		Last Modified: Tue, 12 Aug 2025 23:20:49 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2d87899848fdf17168f462257180eba7b9f0af14c8e7e6cf67ac1d62767a1327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151562670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4975da0824c5c96699fda1d1e4182c08b3a58f6b8d2064bfbeeb645bf8ed052d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 30 Jul 2025 00:49:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 30 Jul 2025 00:49:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV GOSU_VER=1.16
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Jul 2025 00:49:58 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxd"]
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Jul 2025 00:49:58 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c026c42412052a849302d1bc1a482c7b98fa2d12405b32c97adec0d9c56e3fe4`  
		Last Modified: Wed, 13 Aug 2025 07:22:09 GMT  
		Size: 9.6 MB (9604087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eee77d755dd2d844b449975406cc1e1c2908f0afcd9324d28c8aa0c70916a2a`  
		Last Modified: Wed, 13 Aug 2025 07:22:08 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab848f6b6270e3c24e7e67135ef9dace2ec1fc33044f6678689a82018cf191bc`  
		Last Modified: Wed, 13 Aug 2025 07:22:07 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9161c401ca944e27ae18c8bcd2dccc2391fb9fd6d1985e1a1e187491dbe0a69a`  
		Last Modified: Wed, 13 Aug 2025 07:22:08 GMT  
		Size: 938.9 KB (938872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ba89214edd2033d506033c5ec7fe54a46c771966ee15c8d6b58f1a36aad21b`  
		Last Modified: Wed, 13 Aug 2025 07:22:24 GMT  
		Size: 96.0 MB (96038357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4ef359ca1b842e78b94aad324b7e730a3b62744e613a42d5da5e722179a50a`  
		Last Modified: Wed, 13 Aug 2025 07:22:13 GMT  
		Size: 11.1 MB (11098980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ada0ae98a5739a0e1048827172476b7ed060163489d15ec64c503b3cf6b55aa`  
		Last Modified: Wed, 13 Aug 2025 07:22:09 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d345df6ce09d782b63b9aaa7ad325cafd46a7ba81ea5b58fd6bb8bc9160e2`  
		Last Modified: Wed, 13 Aug 2025 07:22:09 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4dd95daf0c07d74d01cac8f7a18a40b925e0d72a6e8409c48aa0551fa237c4`  
		Last Modified: Wed, 13 Aug 2025 07:22:10 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:b0da987852dee4a6b78680a77dc096b0600503d1dfaa9dc6d2504604329f04ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bed5658cab02aaa02b5cda753fd3ea271d88c3a0176c025491b327cf88ccc5`

```dockerfile
```

-	Layers:
	-	`sha256:c5a89415627d964a8e85936370549e0229c00c2ddcf2b59848caa52cc76554f4`  
		Last Modified: Wed, 13 Aug 2025 08:20:30 GMT  
		Size: 3.0 MB (2979001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842880aad603ccf0a2fd09aa6e78baec38e0aaf06cc65738fa777df3b6b0088f`  
		Last Modified: Wed, 13 Aug 2025 08:20:31 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json
