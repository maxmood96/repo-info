<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.10-data`](#influxdb110-data)
-	[`influxdb:1.10-data-alpine`](#influxdb110-data-alpine)
-	[`influxdb:1.10-meta`](#influxdb110-meta)
-	[`influxdb:1.10-meta-alpine`](#influxdb110-meta-alpine)
-	[`influxdb:1.10.7-data`](#influxdb1107-data)
-	[`influxdb:1.10.7-data-alpine`](#influxdb1107-data-alpine)
-	[`influxdb:1.10.7-meta`](#influxdb1107-meta)
-	[`influxdb:1.10.7-meta-alpine`](#influxdb1107-meta-alpine)
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
-	[`influxdb:2.7.11`](#influxdb2711)
-	[`influxdb:2.7.11-alpine`](#influxdb2711-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:4ff7100559788c00b96367ead3db353bd96b45d758e78e700decb7f61fa209f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:ff30ba5981d3e4a491534ea7d524001a030346b93b9f6e9ead38fffdc28d5dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110678547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159fea5619b161cb18eb61c5eb7ca26432db646ead561445488f642de8cffdeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Mon, 02 Dec 2024 19:42:18 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185a13fedcd0c1c2cbd6b9487304c57841d74fb94f2797f18de4096dab27a3ad`  
		Last Modified: Tue, 24 Dec 2024 23:21:07 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766a93aef41ac4e85b359bf69bef8c5832f43e7bbd57d092f142202c0bd2777b`  
		Last Modified: Tue, 24 Dec 2024 23:21:08 GMT  
		Size: 41.4 MB (41377751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d03b0a0f2b06872776deac5127e557d885caefb3f974cb06db178e6c13607ed`  
		Last Modified: Tue, 24 Dec 2024 23:21:07 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436ac9e5df7735c6f94f8ad64507daf088f4d3c174b79c51e09fba3585c89ed0`  
		Last Modified: Tue, 24 Dec 2024 23:21:07 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebeb7eab04e83ec5158cc00305fa218f9de3c2596f89b9c0b17b897099e2ea87`  
		Last Modified: Tue, 24 Dec 2024 23:21:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:1ea6c745efb8a767e8fd8feedefd31aef7ccdabc44f424825e3a0c5296dd33a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4654042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c545a6eda73c4548c5d46cc1f41addfe6250ce9468d722bcaec8158b4966ad`

```dockerfile
```

-	Layers:
	-	`sha256:e16094e857aca93bcef8c0c3c4b96b753d44fc4d8521813d8b829e812d6408b6`  
		Last Modified: Tue, 24 Dec 2024 23:21:07 GMT  
		Size: 4.6 MB (4639334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081461df8ada82effb080c5a3a4ef485403f7363a9d853050dc51576d2cc039d`  
		Last Modified: Tue, 24 Dec 2024 23:21:07 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:6a1a6dd0cf1e08cb5be171f5b02f8f0707ed2aa718be46d7232b8d0e7a0fb5fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e5c4fd36d8686754141874564fdfea08d169603674f5f6eb64fd6335b074269f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46176950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd1b001888cb482e596e84d5f470e445649ed720872055021850146216fb4ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5228d614a2d22fb096b42d39e76e958bcb9e27aea385cb3a8ad21bcc8b253aa2`  
		Last Modified: Wed, 08 Jan 2025 18:15:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f238174b581662af6a02981ae9b061c76655d8ab433797f16606b5f1f243c4`  
		Last Modified: Wed, 08 Jan 2025 18:15:11 GMT  
		Size: 1.2 MB (1226283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77033948f847cc19ba493024bd3cf849d78791321864a3956713975977a8bc3`  
		Last Modified: Wed, 08 Jan 2025 18:15:12 GMT  
		Size: 41.3 MB (41322354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209fde2d1243c292900c9f98f32dd3f5cd62a088f0eafa8b694ee03ddb9b8057`  
		Last Modified: Wed, 08 Jan 2025 18:15:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964c1a244a2bb41b8825882c04e8208d29e012832362b1dff0df30bb2c5130c0`  
		Last Modified: Wed, 08 Jan 2025 18:15:12 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cbade9e7895250435f78a129833031d24b53d1203bc45b15e1cf3baa236939`  
		Last Modified: Wed, 08 Jan 2025 18:15:12 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3804e10cb838a6a257263feee42f290081008aabaf9f5a2203939e6bf6bc1923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **772.3 KB (772270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d3c61c5f7cb336be059927e94eefcc2b9854fd23babfb34484ca66e504f9d9`

```dockerfile
```

-	Layers:
	-	`sha256:add9e8719fdca1df967eac3e0148ba830c1d13b81a4d8e88b3af46177778ffb1`  
		Last Modified: Wed, 08 Jan 2025 18:15:11 GMT  
		Size: 755.6 KB (755631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c99a273d09e16407029c039170d199883a2dc567c30c729502d56e9dfd8014e4`  
		Last Modified: Wed, 08 Jan 2025 18:15:11 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:58e353cfe212956d34cf1f218ed428d2cc4005e4608c377869b4e067fcd3365a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:aadb8ab5c267bb1a1ff4edabc76785a94a510e84d62478e32b0d40fb049c2b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89395155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aef868a3d668151e38939d10cf5796e94c03c0a30b0b9ee4d4ae346b93de47a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Mon, 02 Dec 2024 19:42:18 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2aa2b8b33ddfdb4e56a753b8d2fd4010155fff5aa8789f397e25768e252db3`  
		Last Modified: Tue, 24 Dec 2024 23:21:14 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c46b73340ed0234468a01ddd3f55dcff19314170f13e1e24c2b4cf370fa559a`  
		Last Modified: Tue, 24 Dec 2024 23:21:15 GMT  
		Size: 20.1 MB (20095557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0aac2ad8ed17c7af4b0f864db045e05b9ab7808f4ac465ab1db309d31b56356`  
		Last Modified: Tue, 24 Dec 2024 23:21:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0878a84243e73751c539733b3409aa889789041ed2e03000898538f316480ee`  
		Last Modified: Tue, 24 Dec 2024 23:21:14 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:8322f178c18d717f969976590822b1abdd875277cbaaec4fdd535cab377853dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4576129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3905c6e20251872ca3fdfdf67e62cf4b814c137bb490afc242571a037d7ae307`

```dockerfile
```

-	Layers:
	-	`sha256:e26a7e1c8b8d3562896744ff33d3b63a48a70e04f2df41943063a708887455c0`  
		Last Modified: Tue, 24 Dec 2024 23:21:15 GMT  
		Size: 4.6 MB (4563062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aabb442d822c7616405406be4aa6d1dfaf69b8d0882217eb934d562012d678fe`  
		Last Modified: Tue, 24 Dec 2024 23:21:14 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:65288e39c531c4968f94b10c5000af4c59a88e9fcb2dbeb4efce1addfe78936d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b69e3031143f9dee5d168a40b83164f1d9bde4427e915b9a00d652e8d47703ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24895619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616f03a58204e50721af3f1fe8e163434e163ecd08ee4f5f24afbd46ef5f38f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1e4448c602f86086e34b579436bdaca09c57d32401f7fe3a0825a41c5fa74f`  
		Last Modified: Wed, 08 Jan 2025 18:15:02 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e456ce8daa5503e3e775e5bb439f553efedde4132eea10f5964bf01888bf6b0`  
		Last Modified: Wed, 08 Jan 2025 18:15:02 GMT  
		Size: 1.2 MB (1226287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eced2a6458c86c54c23076a71869783a28e847dbc34a238b77d629e1d0a66ce2`  
		Last Modified: Wed, 08 Jan 2025 18:15:02 GMT  
		Size: 20.0 MB (20042226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadb65c8f49ab571b77a0c385b20b98bafed01fdec6d663e69f0f5d1cc39275b`  
		Last Modified: Wed, 08 Jan 2025 18:15:02 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac88dada83f9e61826485b9d34f20d8fce76f0aa94bba4d163da93863a9fee4`  
		Last Modified: Wed, 08 Jan 2025 18:15:03 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f50980ffab4d0fb64f548ccde631c69ef755a63912a596db72ff04d5dbf19301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.5 KB (694524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ae18a7ecf87c75f9bb0cd92b55550a780c561899fac9c0748089b1710b0859`

```dockerfile
```

-	Layers:
	-	`sha256:48f0dcac119c8ac89f90d30574cb55f8eecd22f8666b6dfd1c19ea7d7ee72551`  
		Last Modified: Wed, 08 Jan 2025 18:15:02 GMT  
		Size: 679.5 KB (679515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd71c5c5e0f715b9d5db4f90f65211754734e0e9cc7d86b05419356457dfed1`  
		Last Modified: Wed, 08 Jan 2025 18:15:02 GMT  
		Size: 15.0 KB (15009 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data`

```console
$ docker pull influxdb@sha256:4ff7100559788c00b96367ead3db353bd96b45d758e78e700decb7f61fa209f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:ff30ba5981d3e4a491534ea7d524001a030346b93b9f6e9ead38fffdc28d5dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110678547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159fea5619b161cb18eb61c5eb7ca26432db646ead561445488f642de8cffdeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Mon, 02 Dec 2024 19:42:18 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185a13fedcd0c1c2cbd6b9487304c57841d74fb94f2797f18de4096dab27a3ad`  
		Last Modified: Tue, 24 Dec 2024 23:21:07 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766a93aef41ac4e85b359bf69bef8c5832f43e7bbd57d092f142202c0bd2777b`  
		Last Modified: Tue, 24 Dec 2024 23:21:08 GMT  
		Size: 41.4 MB (41377751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d03b0a0f2b06872776deac5127e557d885caefb3f974cb06db178e6c13607ed`  
		Last Modified: Tue, 24 Dec 2024 23:21:07 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436ac9e5df7735c6f94f8ad64507daf088f4d3c174b79c51e09fba3585c89ed0`  
		Last Modified: Tue, 24 Dec 2024 23:21:07 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebeb7eab04e83ec5158cc00305fa218f9de3c2596f89b9c0b17b897099e2ea87`  
		Last Modified: Tue, 24 Dec 2024 23:21:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:1ea6c745efb8a767e8fd8feedefd31aef7ccdabc44f424825e3a0c5296dd33a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4654042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c545a6eda73c4548c5d46cc1f41addfe6250ce9468d722bcaec8158b4966ad`

```dockerfile
```

-	Layers:
	-	`sha256:e16094e857aca93bcef8c0c3c4b96b753d44fc4d8521813d8b829e812d6408b6`  
		Last Modified: Tue, 24 Dec 2024 23:21:07 GMT  
		Size: 4.6 MB (4639334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081461df8ada82effb080c5a3a4ef485403f7363a9d853050dc51576d2cc039d`  
		Last Modified: Tue, 24 Dec 2024 23:21:07 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data-alpine`

```console
$ docker pull influxdb@sha256:6a1a6dd0cf1e08cb5be171f5b02f8f0707ed2aa718be46d7232b8d0e7a0fb5fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e5c4fd36d8686754141874564fdfea08d169603674f5f6eb64fd6335b074269f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46176950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd1b001888cb482e596e84d5f470e445649ed720872055021850146216fb4ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5228d614a2d22fb096b42d39e76e958bcb9e27aea385cb3a8ad21bcc8b253aa2`  
		Last Modified: Wed, 08 Jan 2025 18:15:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f238174b581662af6a02981ae9b061c76655d8ab433797f16606b5f1f243c4`  
		Last Modified: Wed, 08 Jan 2025 18:15:11 GMT  
		Size: 1.2 MB (1226283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77033948f847cc19ba493024bd3cf849d78791321864a3956713975977a8bc3`  
		Last Modified: Wed, 08 Jan 2025 18:15:12 GMT  
		Size: 41.3 MB (41322354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209fde2d1243c292900c9f98f32dd3f5cd62a088f0eafa8b694ee03ddb9b8057`  
		Last Modified: Wed, 08 Jan 2025 18:15:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964c1a244a2bb41b8825882c04e8208d29e012832362b1dff0df30bb2c5130c0`  
		Last Modified: Wed, 08 Jan 2025 18:15:12 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cbade9e7895250435f78a129833031d24b53d1203bc45b15e1cf3baa236939`  
		Last Modified: Wed, 08 Jan 2025 18:15:12 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3804e10cb838a6a257263feee42f290081008aabaf9f5a2203939e6bf6bc1923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **772.3 KB (772270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d3c61c5f7cb336be059927e94eefcc2b9854fd23babfb34484ca66e504f9d9`

```dockerfile
```

-	Layers:
	-	`sha256:add9e8719fdca1df967eac3e0148ba830c1d13b81a4d8e88b3af46177778ffb1`  
		Last Modified: Wed, 08 Jan 2025 18:15:11 GMT  
		Size: 755.6 KB (755631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c99a273d09e16407029c039170d199883a2dc567c30c729502d56e9dfd8014e4`  
		Last Modified: Wed, 08 Jan 2025 18:15:11 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-meta`

```console
$ docker pull influxdb@sha256:58e353cfe212956d34cf1f218ed428d2cc4005e4608c377869b4e067fcd3365a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:aadb8ab5c267bb1a1ff4edabc76785a94a510e84d62478e32b0d40fb049c2b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89395155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aef868a3d668151e38939d10cf5796e94c03c0a30b0b9ee4d4ae346b93de47a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Mon, 02 Dec 2024 19:42:18 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2aa2b8b33ddfdb4e56a753b8d2fd4010155fff5aa8789f397e25768e252db3`  
		Last Modified: Tue, 24 Dec 2024 23:21:14 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c46b73340ed0234468a01ddd3f55dcff19314170f13e1e24c2b4cf370fa559a`  
		Last Modified: Tue, 24 Dec 2024 23:21:15 GMT  
		Size: 20.1 MB (20095557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0aac2ad8ed17c7af4b0f864db045e05b9ab7808f4ac465ab1db309d31b56356`  
		Last Modified: Tue, 24 Dec 2024 23:21:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0878a84243e73751c539733b3409aa889789041ed2e03000898538f316480ee`  
		Last Modified: Tue, 24 Dec 2024 23:21:14 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:8322f178c18d717f969976590822b1abdd875277cbaaec4fdd535cab377853dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4576129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3905c6e20251872ca3fdfdf67e62cf4b814c137bb490afc242571a037d7ae307`

```dockerfile
```

-	Layers:
	-	`sha256:e26a7e1c8b8d3562896744ff33d3b63a48a70e04f2df41943063a708887455c0`  
		Last Modified: Tue, 24 Dec 2024 23:21:15 GMT  
		Size: 4.6 MB (4563062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aabb442d822c7616405406be4aa6d1dfaf69b8d0882217eb934d562012d678fe`  
		Last Modified: Tue, 24 Dec 2024 23:21:14 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-meta-alpine`

```console
$ docker pull influxdb@sha256:65288e39c531c4968f94b10c5000af4c59a88e9fcb2dbeb4efce1addfe78936d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b69e3031143f9dee5d168a40b83164f1d9bde4427e915b9a00d652e8d47703ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24895619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616f03a58204e50721af3f1fe8e163434e163ecd08ee4f5f24afbd46ef5f38f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1e4448c602f86086e34b579436bdaca09c57d32401f7fe3a0825a41c5fa74f`  
		Last Modified: Wed, 08 Jan 2025 18:15:02 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e456ce8daa5503e3e775e5bb439f553efedde4132eea10f5964bf01888bf6b0`  
		Last Modified: Wed, 08 Jan 2025 18:15:02 GMT  
		Size: 1.2 MB (1226287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eced2a6458c86c54c23076a71869783a28e847dbc34a238b77d629e1d0a66ce2`  
		Last Modified: Wed, 08 Jan 2025 18:15:02 GMT  
		Size: 20.0 MB (20042226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadb65c8f49ab571b77a0c385b20b98bafed01fdec6d663e69f0f5d1cc39275b`  
		Last Modified: Wed, 08 Jan 2025 18:15:02 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac88dada83f9e61826485b9d34f20d8fce76f0aa94bba4d163da93863a9fee4`  
		Last Modified: Wed, 08 Jan 2025 18:15:03 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f50980ffab4d0fb64f548ccde631c69ef755a63912a596db72ff04d5dbf19301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.5 KB (694524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ae18a7ecf87c75f9bb0cd92b55550a780c561899fac9c0748089b1710b0859`

```dockerfile
```

-	Layers:
	-	`sha256:48f0dcac119c8ac89f90d30574cb55f8eecd22f8666b6dfd1c19ea7d7ee72551`  
		Last Modified: Wed, 08 Jan 2025 18:15:02 GMT  
		Size: 679.5 KB (679515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd71c5c5e0f715b9d5db4f90f65211754734e0e9cc7d86b05419356457dfed1`  
		Last Modified: Wed, 08 Jan 2025 18:15:02 GMT  
		Size: 15.0 KB (15009 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11`

```console
$ docker pull influxdb@sha256:6b566556b7bc7144d8d8add59a8e17d884497a3b8224bdda1d4e9e7c8cccd6a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:de7d3cfb8f6f71cd17e75d38c1045eccc4b32e015a4eee9501bf886a4190d77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116015960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25dfd8e05fd831673e26f4303d8584b178db02e2c2971f97ea59468021d18f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ARG INFLUXDB_VERSION=1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
USER influxdb
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cb35a898b8fb733c9c087b14cc953d190e82952d7af5bf3c4d00d2609cdc02`  
		Last Modified: Tue, 24 Dec 2024 23:20:39 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27405189504e87f2b12bb7465392a3a7fa3a23275e6bea0cba9d2169f65dc822`  
		Last Modified: Tue, 24 Dec 2024 23:20:40 GMT  
		Size: 43.7 MB (43650173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeb49027992a5300c5fca0cc9407e56094844a88aace48f4d2e63f27fabf3fc`  
		Last Modified: Tue, 24 Dec 2024 23:20:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c41f12091c26e5ccbf0e0d530a869ce2997ed6bedf0e537a830d39d260f959`  
		Last Modified: Tue, 24 Dec 2024 23:20:39 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda0dcdf9eb820c99905c385c19b685bacf5d9bf39c49fb22608f0d2d41e0717`  
		Last Modified: Tue, 24 Dec 2024 23:20:40 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:21aac3d4a2cc86392fb4828a72ecf9448b2cf3ca5a6bd6161cdd9e5a52504a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4901198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0774dffab4a7190a4cae2bb2e1e46a9b8ab4aa2c12da12a76786906df5e2b3`

```dockerfile
```

-	Layers:
	-	`sha256:fc177df649a60e092a5c28ed37345df5a957308e94c72248a9382cbad03a8045`  
		Last Modified: Tue, 24 Dec 2024 23:20:40 GMT  
		Size: 4.9 MB (4885669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f7a3485f91a733ff2f8ac96e3634d6fa4405a58f6f333aabc498472fe27217e`  
		Last Modified: Tue, 24 Dec 2024 23:20:39 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4be7c0273d6ae8b9fab2965cea871ee13b48cfbdb89b814e944405c8a73d8644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112853008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb10cd05d2af50245f3fc83182b6a0efc64d6faa32b61f530592ec82bbdee4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ARG INFLUXDB_VERSION=1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
USER influxdb
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db46794b40498e832fb8a5dab259bc6385c47b3929373614ec7ac5ec59da5489`  
		Last Modified: Wed, 25 Dec 2024 09:05:51 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b7f11ba952d4196ffa03c2aab6436fc0e43d2ef686f5336067aee7ac6de4cc`  
		Last Modified: Wed, 25 Dec 2024 09:05:52 GMT  
		Size: 41.1 MB (41118848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59da261f14ab67b95be67692cc16020a3e446a31d62dc2030dcaf50cdf4b1f1`  
		Last Modified: Wed, 25 Dec 2024 09:05:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057157a7ea9b0597ed01c7af38cad9011756b515d169c3f076b6bccf96b6cfa6`  
		Last Modified: Wed, 25 Dec 2024 09:05:51 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d107d0fbcb83fcbf134b0554b2743777f36c3957208051afb8730aa2bf1847`  
		Last Modified: Wed, 25 Dec 2024 09:05:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:3ff8884e4be1e8671b382d10a39f9413f3b28ba4c929a7a91afa210efe349a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4900758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85ea7f280d1a38e2a37316e43d076384f0a6459f59a97b65855019093fd470e`

```dockerfile
```

-	Layers:
	-	`sha256:c2042328073955d200c4bb25c5054851817ba3e435950e6447e6e0b4f2405c59`  
		Last Modified: Wed, 25 Dec 2024 09:05:51 GMT  
		Size: 4.9 MB (4885134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2aec4c8ced18e532fbc73d06ad45ee58cf31a0192efc9fc805118509482879e`  
		Last Modified: Wed, 25 Dec 2024 09:05:50 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-alpine`

```console
$ docker pull influxdb@sha256:8b8ad9f837c664af1641c9974388c5894aadadd5dd32eb58f353d6706a88acd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:987a8257fbd56c8e742457b1893be7772ff03f044c353a90258b6d0cc729fa87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42923477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5396a1e10712f12f2a0a7e7df18405741fef808008ed476865f5b899153481e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ARG INFLUXDB_VERSION=1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
USER influxdb
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff62fd140ecc2e2d17f83bbd27600cfe78e013df6e0bea00ce76ecfecc6f56b`  
		Last Modified: Wed, 08 Jan 2025 18:12:04 GMT  
		Size: 1.2 MB (1226309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d00cb79546531c497aa9b5673e4258620226f856b8d87abc315738b8d7d08bc`  
		Last Modified: Wed, 08 Jan 2025 18:12:05 GMT  
		Size: 38.1 MB (38068191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81305db3f9528169002b682474fba1debb258d6ecc863055efe4ec99bf7b902e`  
		Last Modified: Wed, 08 Jan 2025 18:12:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964aa4e3207f9a02954bb6a633b93f4b99fed9d899f2ea9b43ce6ff470068f2c`  
		Last Modified: Wed, 08 Jan 2025 18:12:04 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894f38c870039d61a7e118c3ae5589ff4557ed1423ec69f9b3636de43f2c3b2d`  
		Last Modified: Wed, 08 Jan 2025 18:12:05 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589fcf38227a5dcec2a2be6e3958607e24412871750573d86414b8c084d00a64`  
		Last Modified: Wed, 08 Jan 2025 18:12:05 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:519d82622580d8d718b6a1389c1c54926c74fa1c19f3726bbc06e15496aa70c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **761.2 KB (761198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301928edfe17ab3c111cff49e4faf4d40b29e4a6adc66e5bff330796c1ce19b5`

```dockerfile
```

-	Layers:
	-	`sha256:7eefc35035cc6c97ac98315d159bb5cd6f33b54780a54e8578be70ba6c556a2a`  
		Last Modified: Wed, 08 Jan 2025 18:12:04 GMT  
		Size: 743.3 KB (743321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b177f444d71db7ace90d04f0ed03b4185ee4cab1d376d7f679a30f4318a465d`  
		Last Modified: Wed, 08 Jan 2025 18:12:04 GMT  
		Size: 17.9 KB (17877 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c525bd04add32596115e4228932d993f00e43cef8347192602d7ecdd9e1611d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40926940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738cdd897f71270b21b4d2d1db99e497197f58b638beee787bef8b168db659b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ARG INFLUXDB_VERSION=1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
USER influxdb
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dab2ca2b7535c7524d2614bb862775d367ba5e7c44fe702157769b166abbe9`  
		Last Modified: Tue, 07 Jan 2025 08:37:31 GMT  
		Size: 1.3 MB (1292222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2478aad5f6508590c7c5d56327299d5da505675d1df1cf2151c8af228fcf947f`  
		Last Modified: Tue, 07 Jan 2025 08:37:32 GMT  
		Size: 35.5 MB (35545318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d87f88ee7288bd213ddebae4c4e2886287b30b6f05efd075b8354a5291bbc3`  
		Last Modified: Tue, 07 Jan 2025 08:37:31 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af884c1abdd0a7e65a57eeab83a98c884d3fe62be284091f1f91a401b3cd9751`  
		Last Modified: Tue, 07 Jan 2025 08:37:31 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393cd4b050a53402777aacdeeaf336b93976dc7c62e9138c2ece32ed68822b21`  
		Last Modified: Tue, 07 Jan 2025 08:37:32 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed470a45b4184eba49f540e1fd674182cd3690f3328ca66003cf059fff44d5e6`  
		Last Modified: Tue, 07 Jan 2025 08:37:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:de1f1b0881afcf328d2038555e5b0aa3458a2ac95d01ad58c68b0da732797718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **754.7 KB (754657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f7748baa84f60873cef09a695b99b0e0a3a5d93bbf370798f12b5a502596ce`

```dockerfile
```

-	Layers:
	-	`sha256:1ed2133f67289ca3b683f0543880158eeac7132fe8809729f7ea76f13688bdd9`  
		Last Modified: Tue, 07 Jan 2025 08:37:31 GMT  
		Size: 736.7 KB (736670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fee6866aaa824d25caf695b7dc3c770373697809d647315e6d7f4e2b2e610c5`  
		Last Modified: Tue, 07 Jan 2025 08:37:31 GMT  
		Size: 18.0 KB (17987 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:25f6c0970ac4b37733c4c6b49fc8d8c911322e75ce13a6544a2b826482a43221
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:4de9cef8c8d125e6efae69dc3b3848f273d369aa9cd9a957b607a0191f3f15ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111545772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b0588446365767f14d514c479d7fdb9713368d24968a505cd5936253562ad2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1106e1a8f25c11f955331361e5993cb3273b62a9f55ee6f2e30e1158f7e814`  
		Last Modified: Tue, 24 Dec 2024 23:21:19 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33a182d764a5744bd9f80c0bab8bee58fc44881baf0e63c988ec7217590fbac`  
		Last Modified: Tue, 24 Dec 2024 23:21:20 GMT  
		Size: 39.2 MB (39179332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5b2611e3f7d1a9c9968439242faea2cc7d7d1eff6e661fe4398b593bf62d0`  
		Last Modified: Tue, 24 Dec 2024 23:21:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc89e8a2f659d248395dbe037d1d34c838c6143d32c48ddbfdfed83ade68f573`  
		Last Modified: Tue, 24 Dec 2024 23:21:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42f75be104df39e1e1365c20f13153367e66281da63169d02b747369eba9279`  
		Last Modified: Tue, 24 Dec 2024 23:21:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:3bcadbb6f1e01d62de8678b10491cb7726031d474da3f888e2aa2df17d7c9c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4526289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91078b0d4951723d74e17d384dc52c88252c909785344cf4beaf7b6463f3b5e`

```dockerfile
```

-	Layers:
	-	`sha256:3669900c01119b0c2827f37d61d1f9f0453b766f35881c8754000cde8c114e0b`  
		Last Modified: Tue, 24 Dec 2024 23:21:19 GMT  
		Size: 4.5 MB (4511581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2392f469b3a6296ec37c6227ea28e3a6952f652aa6ed97b36d8acbf191d313d2`  
		Last Modified: Tue, 24 Dec 2024 23:21:19 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:6ef896c44cef61a9e73a93d627418cbfc885b3420f6ab4becd95a25bc7fa78a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6655c663622d21a881f12d9e89c9abd39e0fc3fc7c4a051f180f9478717c050a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43978318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7170ca43320bfc874cc9076334b57d463b4b8c40a5b719dfd73814655f0f2376`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb92ac7301eb1d8a431d21e649728ac813a9810b06306e0816d682ad0be9ca0c`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771edd56630effa49742e70bc4966be27b5b7aac72b4327602e0752540a50e06`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 1.2 MB (1226278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39847ce2aea07dd905ca046d44ab9d7cdd71e10244b02d72c39259394df29af`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 39.1 MB (39123728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0961dbb249094a7b9c8d928d9222603798f8c95bf7e34b275a4b1df25d04fc47`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356734595c256b42960fdae02261aa090f61d515896eb64b7ebbe28463d22f44`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026f74af2126ed5da85d5e44543d4636a42d4a25b8d638c28df28201824503ad`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c95b7495cd4f09a30ad53d79d06aa9190214e3cc6badd6124879f3fc87c2cde6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **770.5 KB (770504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ab783fa72ba4b9ee22d26393f1e8577474826fc8234befbf502ffc278a6fdb`

```dockerfile
```

-	Layers:
	-	`sha256:c8c0460be35fa8313f48636b7ebb24b17e6c47c7b93185c6db53528eab1aa6c6`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 753.9 KB (753866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1eb99722499cff1e90be8fb281cc97ed4ea02271e2dc6033525dc35bcd00646`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 16.6 KB (16638 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:c5d2a19e4fa32902229b106032c076fbad1d13a326259319ea7994363560f44a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:e6716bfc1b7634d11242183ffe7a8884d12d5847199fedb901df24667216b6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90701781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e123f3f81fa1a7758f9f4d0f14557188c5faed6ebc43ae9e8f60782d0ac7997e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934b304b3a280af8457969f466640c2bc6892ec3ac3a1026b088bb7748865d45`  
		Last Modified: Tue, 24 Dec 2024 23:16:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9158a06bc97a328360308f1e8f4531b89aa63ebb46ae3966bed40fb54c4c19f5`  
		Last Modified: Tue, 24 Dec 2024 23:16:21 GMT  
		Size: 18.3 MB (18336557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73b901d3037ed13621ec7d7a5af9d598602ba980eb1290f7c171532a67de393`  
		Last Modified: Tue, 24 Dec 2024 23:16:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1a7df5b79c84d3033cef39b75becd8dc1a19e89f171c16d218ae2a0086bd60`  
		Last Modified: Tue, 24 Dec 2024 23:16:21 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:6347d8448ffc6ae696c5165e64d64d10242ec19fa9584af41ed18b26ee56613e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4449367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7700cff8a425e0c77bb3a77ebb94531191022c70fabc13689e96324a1417ecaa`

```dockerfile
```

-	Layers:
	-	`sha256:4218ccd60559293a04858de4f6175a46f18481b1ef48488fb527ab79a96e6e1c`  
		Last Modified: Tue, 24 Dec 2024 23:16:21 GMT  
		Size: 4.4 MB (4436300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27be4d90d54798d0ce872c89a7666b3363e850a8663350adbe551eea1a989a06`  
		Last Modified: Tue, 24 Dec 2024 23:16:21 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:ffc9e55a00d87ba9a3aa7aa6f8f4e5b54ee293a983a0cc10a69c50b16ee2c250
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:179b60c46d4e2a69518b2630f26dee3b2f345955310f7ec9451b2402554f1cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23143516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e90d379ecf18cfe86d114a1361b78dd5c1899256d8eb86301b71d7a75a5b85d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec886b5104d1736c962d9a26cb1c2e7b74dc122c97ecb74765c6667e2f2f5f57`  
		Last Modified: Wed, 08 Jan 2025 18:15:28 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2556158dac025dc80762bfa364f4f60f01b43fb9242bda2b2c0456867fad22a`  
		Last Modified: Wed, 08 Jan 2025 18:15:29 GMT  
		Size: 1.2 MB (1226283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d825768c9b1e0f7ee83b299d2e8231866534821704df104f5ea584f75db868`  
		Last Modified: Wed, 08 Jan 2025 18:15:29 GMT  
		Size: 18.3 MB (18290127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea5fdd31ba6af7bf28e6c43d6dc6cf9cf8627940b7cf7e1a51537147e1c3fab`  
		Last Modified: Wed, 08 Jan 2025 18:15:28 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597c54582570beeb6c8b1eca604243dde7c98de2e5efbc44fa9bf666e9351f48`  
		Last Modified: Wed, 08 Jan 2025 18:15:30 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c47b353495ece44d6733dea88bf4788774915438005922fbb2e6eb71ad0cd282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.4 KB (694381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97787e2c7aa546925f5e0c1e15e70408fac26f5586395f981f7159a769a8074`

```dockerfile
```

-	Layers:
	-	`sha256:004a8d359505e5e940aeca31e39cd336ea621235cd1db94958a7c1b09e5b63ea`  
		Last Modified: Wed, 08 Jan 2025 18:15:29 GMT  
		Size: 679.4 KB (679371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c435f5dc123d72b7457ccfe44dfde1e72af276a22ec478f218ba7cbf82f556e0`  
		Last Modified: Wed, 08 Jan 2025 18:15:28 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8`

```console
$ docker pull influxdb@sha256:6b566556b7bc7144d8d8add59a8e17d884497a3b8224bdda1d4e9e7c8cccd6a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:de7d3cfb8f6f71cd17e75d38c1045eccc4b32e015a4eee9501bf886a4190d77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116015960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25dfd8e05fd831673e26f4303d8584b178db02e2c2971f97ea59468021d18f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ARG INFLUXDB_VERSION=1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
USER influxdb
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cb35a898b8fb733c9c087b14cc953d190e82952d7af5bf3c4d00d2609cdc02`  
		Last Modified: Tue, 24 Dec 2024 23:20:39 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27405189504e87f2b12bb7465392a3a7fa3a23275e6bea0cba9d2169f65dc822`  
		Last Modified: Tue, 24 Dec 2024 23:20:40 GMT  
		Size: 43.7 MB (43650173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeb49027992a5300c5fca0cc9407e56094844a88aace48f4d2e63f27fabf3fc`  
		Last Modified: Tue, 24 Dec 2024 23:20:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c41f12091c26e5ccbf0e0d530a869ce2997ed6bedf0e537a830d39d260f959`  
		Last Modified: Tue, 24 Dec 2024 23:20:39 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda0dcdf9eb820c99905c385c19b685bacf5d9bf39c49fb22608f0d2d41e0717`  
		Last Modified: Tue, 24 Dec 2024 23:20:40 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:21aac3d4a2cc86392fb4828a72ecf9448b2cf3ca5a6bd6161cdd9e5a52504a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4901198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0774dffab4a7190a4cae2bb2e1e46a9b8ab4aa2c12da12a76786906df5e2b3`

```dockerfile
```

-	Layers:
	-	`sha256:fc177df649a60e092a5c28ed37345df5a957308e94c72248a9382cbad03a8045`  
		Last Modified: Tue, 24 Dec 2024 23:20:40 GMT  
		Size: 4.9 MB (4885669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f7a3485f91a733ff2f8ac96e3634d6fa4405a58f6f333aabc498472fe27217e`  
		Last Modified: Tue, 24 Dec 2024 23:20:39 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4be7c0273d6ae8b9fab2965cea871ee13b48cfbdb89b814e944405c8a73d8644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112853008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb10cd05d2af50245f3fc83182b6a0efc64d6faa32b61f530592ec82bbdee4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ARG INFLUXDB_VERSION=1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
USER influxdb
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db46794b40498e832fb8a5dab259bc6385c47b3929373614ec7ac5ec59da5489`  
		Last Modified: Wed, 25 Dec 2024 09:05:51 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b7f11ba952d4196ffa03c2aab6436fc0e43d2ef686f5336067aee7ac6de4cc`  
		Last Modified: Wed, 25 Dec 2024 09:05:52 GMT  
		Size: 41.1 MB (41118848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59da261f14ab67b95be67692cc16020a3e446a31d62dc2030dcaf50cdf4b1f1`  
		Last Modified: Wed, 25 Dec 2024 09:05:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057157a7ea9b0597ed01c7af38cad9011756b515d169c3f076b6bccf96b6cfa6`  
		Last Modified: Wed, 25 Dec 2024 09:05:51 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d107d0fbcb83fcbf134b0554b2743777f36c3957208051afb8730aa2bf1847`  
		Last Modified: Wed, 25 Dec 2024 09:05:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:3ff8884e4be1e8671b382d10a39f9413f3b28ba4c929a7a91afa210efe349a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4900758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85ea7f280d1a38e2a37316e43d076384f0a6459f59a97b65855019093fd470e`

```dockerfile
```

-	Layers:
	-	`sha256:c2042328073955d200c4bb25c5054851817ba3e435950e6447e6e0b4f2405c59`  
		Last Modified: Wed, 25 Dec 2024 09:05:51 GMT  
		Size: 4.9 MB (4885134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2aec4c8ced18e532fbc73d06ad45ee58cf31a0192efc9fc805118509482879e`  
		Last Modified: Wed, 25 Dec 2024 09:05:50 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-alpine`

```console
$ docker pull influxdb@sha256:8b8ad9f837c664af1641c9974388c5894aadadd5dd32eb58f353d6706a88acd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:987a8257fbd56c8e742457b1893be7772ff03f044c353a90258b6d0cc729fa87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42923477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5396a1e10712f12f2a0a7e7df18405741fef808008ed476865f5b899153481e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ARG INFLUXDB_VERSION=1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
USER influxdb
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff62fd140ecc2e2d17f83bbd27600cfe78e013df6e0bea00ce76ecfecc6f56b`  
		Last Modified: Wed, 08 Jan 2025 18:12:04 GMT  
		Size: 1.2 MB (1226309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d00cb79546531c497aa9b5673e4258620226f856b8d87abc315738b8d7d08bc`  
		Last Modified: Wed, 08 Jan 2025 18:12:05 GMT  
		Size: 38.1 MB (38068191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81305db3f9528169002b682474fba1debb258d6ecc863055efe4ec99bf7b902e`  
		Last Modified: Wed, 08 Jan 2025 18:12:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964aa4e3207f9a02954bb6a633b93f4b99fed9d899f2ea9b43ce6ff470068f2c`  
		Last Modified: Wed, 08 Jan 2025 18:12:04 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894f38c870039d61a7e118c3ae5589ff4557ed1423ec69f9b3636de43f2c3b2d`  
		Last Modified: Wed, 08 Jan 2025 18:12:05 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589fcf38227a5dcec2a2be6e3958607e24412871750573d86414b8c084d00a64`  
		Last Modified: Wed, 08 Jan 2025 18:12:05 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:519d82622580d8d718b6a1389c1c54926c74fa1c19f3726bbc06e15496aa70c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **761.2 KB (761198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301928edfe17ab3c111cff49e4faf4d40b29e4a6adc66e5bff330796c1ce19b5`

```dockerfile
```

-	Layers:
	-	`sha256:7eefc35035cc6c97ac98315d159bb5cd6f33b54780a54e8578be70ba6c556a2a`  
		Last Modified: Wed, 08 Jan 2025 18:12:04 GMT  
		Size: 743.3 KB (743321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b177f444d71db7ace90d04f0ed03b4185ee4cab1d376d7f679a30f4318a465d`  
		Last Modified: Wed, 08 Jan 2025 18:12:04 GMT  
		Size: 17.9 KB (17877 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c525bd04add32596115e4228932d993f00e43cef8347192602d7ecdd9e1611d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40926940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738cdd897f71270b21b4d2d1db99e497197f58b638beee787bef8b168db659b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ARG INFLUXDB_VERSION=1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
USER influxdb
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dab2ca2b7535c7524d2614bb862775d367ba5e7c44fe702157769b166abbe9`  
		Last Modified: Tue, 07 Jan 2025 08:37:31 GMT  
		Size: 1.3 MB (1292222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2478aad5f6508590c7c5d56327299d5da505675d1df1cf2151c8af228fcf947f`  
		Last Modified: Tue, 07 Jan 2025 08:37:32 GMT  
		Size: 35.5 MB (35545318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d87f88ee7288bd213ddebae4c4e2886287b30b6f05efd075b8354a5291bbc3`  
		Last Modified: Tue, 07 Jan 2025 08:37:31 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af884c1abdd0a7e65a57eeab83a98c884d3fe62be284091f1f91a401b3cd9751`  
		Last Modified: Tue, 07 Jan 2025 08:37:31 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393cd4b050a53402777aacdeeaf336b93976dc7c62e9138c2ece32ed68822b21`  
		Last Modified: Tue, 07 Jan 2025 08:37:32 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed470a45b4184eba49f540e1fd674182cd3690f3328ca66003cf059fff44d5e6`  
		Last Modified: Tue, 07 Jan 2025 08:37:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:de1f1b0881afcf328d2038555e5b0aa3458a2ac95d01ad58c68b0da732797718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **754.7 KB (754657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f7748baa84f60873cef09a695b99b0e0a3a5d93bbf370798f12b5a502596ce`

```dockerfile
```

-	Layers:
	-	`sha256:1ed2133f67289ca3b683f0543880158eeac7132fe8809729f7ea76f13688bdd9`  
		Last Modified: Tue, 07 Jan 2025 08:37:31 GMT  
		Size: 736.7 KB (736670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fee6866aaa824d25caf695b7dc3c770373697809d647315e6d7f4e2b2e610c5`  
		Last Modified: Tue, 07 Jan 2025 08:37:31 GMT  
		Size: 18.0 KB (17987 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-data`

```console
$ docker pull influxdb@sha256:25f6c0970ac4b37733c4c6b49fc8d8c911322e75ce13a6544a2b826482a43221
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:4de9cef8c8d125e6efae69dc3b3848f273d369aa9cd9a957b607a0191f3f15ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111545772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b0588446365767f14d514c479d7fdb9713368d24968a505cd5936253562ad2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1106e1a8f25c11f955331361e5993cb3273b62a9f55ee6f2e30e1158f7e814`  
		Last Modified: Tue, 24 Dec 2024 23:21:19 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33a182d764a5744bd9f80c0bab8bee58fc44881baf0e63c988ec7217590fbac`  
		Last Modified: Tue, 24 Dec 2024 23:21:20 GMT  
		Size: 39.2 MB (39179332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5b2611e3f7d1a9c9968439242faea2cc7d7d1eff6e661fe4398b593bf62d0`  
		Last Modified: Tue, 24 Dec 2024 23:21:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc89e8a2f659d248395dbe037d1d34c838c6143d32c48ddbfdfed83ade68f573`  
		Last Modified: Tue, 24 Dec 2024 23:21:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42f75be104df39e1e1365c20f13153367e66281da63169d02b747369eba9279`  
		Last Modified: Tue, 24 Dec 2024 23:21:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:3bcadbb6f1e01d62de8678b10491cb7726031d474da3f888e2aa2df17d7c9c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4526289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91078b0d4951723d74e17d384dc52c88252c909785344cf4beaf7b6463f3b5e`

```dockerfile
```

-	Layers:
	-	`sha256:3669900c01119b0c2827f37d61d1f9f0453b766f35881c8754000cde8c114e0b`  
		Last Modified: Tue, 24 Dec 2024 23:21:19 GMT  
		Size: 4.5 MB (4511581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2392f469b3a6296ec37c6227ea28e3a6952f652aa6ed97b36d8acbf191d313d2`  
		Last Modified: Tue, 24 Dec 2024 23:21:19 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-data-alpine`

```console
$ docker pull influxdb@sha256:6ef896c44cef61a9e73a93d627418cbfc885b3420f6ab4becd95a25bc7fa78a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6655c663622d21a881f12d9e89c9abd39e0fc3fc7c4a051f180f9478717c050a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43978318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7170ca43320bfc874cc9076334b57d463b4b8c40a5b719dfd73814655f0f2376`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb92ac7301eb1d8a431d21e649728ac813a9810b06306e0816d682ad0be9ca0c`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771edd56630effa49742e70bc4966be27b5b7aac72b4327602e0752540a50e06`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 1.2 MB (1226278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39847ce2aea07dd905ca046d44ab9d7cdd71e10244b02d72c39259394df29af`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 39.1 MB (39123728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0961dbb249094a7b9c8d928d9222603798f8c95bf7e34b275a4b1df25d04fc47`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356734595c256b42960fdae02261aa090f61d515896eb64b7ebbe28463d22f44`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026f74af2126ed5da85d5e44543d4636a42d4a25b8d638c28df28201824503ad`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c95b7495cd4f09a30ad53d79d06aa9190214e3cc6badd6124879f3fc87c2cde6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **770.5 KB (770504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ab783fa72ba4b9ee22d26393f1e8577474826fc8234befbf502ffc278a6fdb`

```dockerfile
```

-	Layers:
	-	`sha256:c8c0460be35fa8313f48636b7ebb24b17e6c47c7b93185c6db53528eab1aa6c6`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 753.9 KB (753866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1eb99722499cff1e90be8fb281cc97ed4ea02271e2dc6033525dc35bcd00646`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 16.6 KB (16638 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-meta`

```console
$ docker pull influxdb@sha256:c5d2a19e4fa32902229b106032c076fbad1d13a326259319ea7994363560f44a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:e6716bfc1b7634d11242183ffe7a8884d12d5847199fedb901df24667216b6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90701781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e123f3f81fa1a7758f9f4d0f14557188c5faed6ebc43ae9e8f60782d0ac7997e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934b304b3a280af8457969f466640c2bc6892ec3ac3a1026b088bb7748865d45`  
		Last Modified: Tue, 24 Dec 2024 23:16:21 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9158a06bc97a328360308f1e8f4531b89aa63ebb46ae3966bed40fb54c4c19f5`  
		Last Modified: Tue, 24 Dec 2024 23:16:21 GMT  
		Size: 18.3 MB (18336557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73b901d3037ed13621ec7d7a5af9d598602ba980eb1290f7c171532a67de393`  
		Last Modified: Tue, 24 Dec 2024 23:16:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1a7df5b79c84d3033cef39b75becd8dc1a19e89f171c16d218ae2a0086bd60`  
		Last Modified: Tue, 24 Dec 2024 23:16:21 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:6347d8448ffc6ae696c5165e64d64d10242ec19fa9584af41ed18b26ee56613e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4449367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7700cff8a425e0c77bb3a77ebb94531191022c70fabc13689e96324a1417ecaa`

```dockerfile
```

-	Layers:
	-	`sha256:4218ccd60559293a04858de4f6175a46f18481b1ef48488fb527ab79a96e6e1c`  
		Last Modified: Tue, 24 Dec 2024 23:16:21 GMT  
		Size: 4.4 MB (4436300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27be4d90d54798d0ce872c89a7666b3363e850a8663350adbe551eea1a989a06`  
		Last Modified: Tue, 24 Dec 2024 23:16:21 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-meta-alpine`

```console
$ docker pull influxdb@sha256:ffc9e55a00d87ba9a3aa7aa6f8f4e5b54ee293a983a0cc10a69c50b16ee2c250
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:179b60c46d4e2a69518b2630f26dee3b2f345955310f7ec9451b2402554f1cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23143516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e90d379ecf18cfe86d114a1361b78dd5c1899256d8eb86301b71d7a75a5b85d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Mon, 02 Dec 2024 19:42:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec886b5104d1736c962d9a26cb1c2e7b74dc122c97ecb74765c6667e2f2f5f57`  
		Last Modified: Wed, 08 Jan 2025 18:15:28 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2556158dac025dc80762bfa364f4f60f01b43fb9242bda2b2c0456867fad22a`  
		Last Modified: Wed, 08 Jan 2025 18:15:29 GMT  
		Size: 1.2 MB (1226283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d825768c9b1e0f7ee83b299d2e8231866534821704df104f5ea584f75db868`  
		Last Modified: Wed, 08 Jan 2025 18:15:29 GMT  
		Size: 18.3 MB (18290127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea5fdd31ba6af7bf28e6c43d6dc6cf9cf8627940b7cf7e1a51537147e1c3fab`  
		Last Modified: Wed, 08 Jan 2025 18:15:28 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597c54582570beeb6c8b1eca604243dde7c98de2e5efbc44fa9bf666e9351f48`  
		Last Modified: Wed, 08 Jan 2025 18:15:30 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c47b353495ece44d6733dea88bf4788774915438005922fbb2e6eb71ad0cd282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.4 KB (694381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97787e2c7aa546925f5e0c1e15e70408fac26f5586395f981f7159a769a8074`

```dockerfile
```

-	Layers:
	-	`sha256:004a8d359505e5e940aeca31e39cd336ea621235cd1db94958a7c1b09e5b63ea`  
		Last Modified: Wed, 08 Jan 2025 18:15:29 GMT  
		Size: 679.4 KB (679371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c435f5dc123d72b7457ccfe44dfde1e72af276a22ec478f218ba7cbf82f556e0`  
		Last Modified: Wed, 08 Jan 2025 18:15:28 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:57429ef3f13cf25bbe541a54b2b831c1b339cfcf5bd060934f0a9ee5ed5428ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:813cce36a766ed3e3280b68b806591e64bbe9178c9c0a9b2ed7043aefd51695a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168524805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eaca693d9271123d11dd9b73a52b9c3e17d7c205b2622ca93655a48d5571c8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 19:42:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV GOSU_VER=1.16
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ceb32a7cd49428f5b5a5ecdd1169ca5237a4d72955d6b7133a61840eb79091d`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 9.6 MB (9596628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749e0ee9681ffcf4992ddb24b0513d74c3c5bd6a137f7319242ae00c7a9fb00d`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 5.8 MB (5820921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350078b5827c590786ffa202ff5e7d457f5ce17578e04d1c1e5a86907d8d2e51`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620187628669b47cda0dd9123d6c9ec83be49f919e909674af1b656bd2a4281f`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8498a0a81b137f0f34a91756d025ce39916bc2e1ac403fb93a57e65e68ab25`  
		Last Modified: Tue, 24 Dec 2024 22:27:29 GMT  
		Size: 100.3 MB (100312964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08b3e9f74aa64c19a1b7785476b8b6151394d3ba0fc7a6a2f18c10e2658cbc7`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 23.5 MB (23546387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05be0669f9759b48fa48b2e11d1e297cf54382244baee56db7d1149c70d06ca`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b93f8466c77b915f1de61395ec259eb44b54354c2d53ee034db9f1215f5c420`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d47214fe47b1e82ff5c4c4725fd2842f0155566df5b4abdd087474edf165344`  
		Last Modified: Tue, 24 Dec 2024 22:27:29 GMT  
		Size: 6.3 KB (6288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:af0aa27200123ebaae4036cbfa2c7ac252b56fa97dac7c2b75a045461f7ae17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9a0df5d8a90b8bbf29a9f81606240c49c6150b87fc84e91bf18e76ac7e5f57`

```dockerfile
```

-	Layers:
	-	`sha256:47b57e337cbcd6b24047353607188a10889c6b5f0822d71990b542b9c8a9ace1`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 2.8 MB (2848627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef6de32486cd7c360225f7fab7cc8f77b10dbdc34b79a0efcbd4df782741fa5`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 33.7 KB (33720 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:523c58ef436dff1687abca84e9a54addfb3fcb1fa6aa5f2fd289576a58e6027f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162212047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908a77248b8ad48410d69fd28dc03afab44d78d32ef05bea7c4fe076dc6a9fe4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 19:42:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV GOSU_VER=1.16
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74f53f4e2a360da5abfca2277671a38f9231b23bbf96fe58ded32e590ef860f`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 9.4 MB (9394168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873e4e4c9210bed2334d3c40b9b66323a577a4c23ae188832bca29ae670e0a75`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59454c66a11677c383ffe4680b394e13379bb05cac147fe4b312086e2a43285`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e3dabc2298cafd687c5cbf967781341f2e15cd6f85f115f836a038ab3a9af9`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cc306cb8755c7bae9b3e38280b9a79f104c2358b56f078eae8edbb5be86a1`  
		Last Modified: Wed, 25 Dec 2024 02:13:24 GMT  
		Size: 96.2 MB (96151368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b402f669421624c959471cad9b38c75225b0f0f587a572841a74fe19fc986042`  
		Last Modified: Wed, 25 Dec 2024 02:13:23 GMT  
		Size: 22.2 MB (22197941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e005371217bc51fc0b856c67c9f54f35e1e5758ba292026b01ed894e78c321`  
		Last Modified: Wed, 25 Dec 2024 02:13:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66135171293553a852be765599e3b866511b4cb599b7e57d836e8b10d32b8626`  
		Last Modified: Wed, 25 Dec 2024 02:13:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27705135a6a1dfdefecec1447d44ac97a81ed890397237d000e5a4e8257f0b76`  
		Last Modified: Wed, 25 Dec 2024 02:13:23 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:90b1c95d6993032369f780eced4a90848472245c3535c9d85bc149a4e56c13e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2881758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbe81027ea1eade69ba4df3afe0e9268289b5b4a441133efad4f5f3339715d3`

```dockerfile
```

-	Layers:
	-	`sha256:d4bc2167e531237007711f7480bc1e4253f2e91d05eabd195bd296f765a2d758`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 2.8 MB (2847855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8beb0a5dc5245ffc4a7f1f2db4c923e55fb59fd51625784376f017202f0dae2f`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 33.9 KB (33903 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:6fbb8ff2f014b783ed35d098aac3428448c81f470cbe5fb556719ace943cfa79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b4aae23172008e162b9a084342cdca5d1452ae4a059304da6a6fabd59f76af22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92813970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b3e3f8000016363e0a784f8edcbf98dc4aa46b9bd27ebdeca576ffecece05d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb92ac7301eb1d8a431d21e649728ac813a9810b06306e0816d682ad0be9ca0c`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c097ac5959ac8b7e5ce7e4625284fdc002f278072a8a534bbdea3ecd50e54c`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 9.7 MB (9664086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eb104e3f0244f28d748ea2d7e74df268bfc91d976a040efdd8b6472e202934`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 5.8 MB (5820946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89aa6391ecf05bcbe8b467dbf27ab8a43f13cc250042561a1d506468cb0d2b38`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab10afa0a468cd5771fd77f7f5063bdb5ad4ac335858959ab0bdf509b5ee136f`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 50.1 MB (50148313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33662d6cd32b83879dfbf57d88bbfcc6d967f3f0474808141c15bd937c018575`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 23.5 MB (23546400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c327bb004d758bbb8c21ea739fe8e4121de1461e28a6991b2d79db665075a004`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfda2b82a1866dcc3572daf050a9248464dc689cc9594f1322c28270c497df24`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ee9c3c3ab82c14c13a9355fe8cf4ce6147fb8f665e4d2403e6ec4d55430a70`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e64aa7820f3f75bfb9893c5c68463c206f04d425e64680274067fe3e3453b99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **948.2 KB (948152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101b1bdaf1a4935098a15031b753e4b76bf5700056850d7f9236ecc66b9ddae4`

```dockerfile
```

-	Layers:
	-	`sha256:23cbff2765458f31b583563fa71b23e8c50895a61da97a761de9b33301d22c7d`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 917.2 KB (917204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd3e60aa959b21ee324b6538f5b8a26f77d2fd9e22616fdd3c5271bfccbfc42`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:381be70cf44e73d9e0bc55f8d0cac1f5a08f4c9869dfbbeb2495d227ae98d0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89599718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76114aa77360041ce959a4d707e27c03f02956315bf52b5682e2158368002a88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce83109ec04193e8d1d95cc284000b3744402e6eb3a74774afb3a1dfca37714`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ae5757088c40ba9252bc398341fd4347da11535780149b3b39104b7d2d2c4`  
		Last Modified: Tue, 07 Jan 2025 08:37:57 GMT  
		Size: 9.8 MB (9769732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a0cb131d8295a6731b94e1af752bc44934519b9a440c2a25c516b0a53e121`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef225f1667c91e1c16b29bd860d533e6129d22ddb50151ed69e586ef708d62e9`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2039b5d949f249c870175a599013329b1e6f0631b518c33316e28879fa00b8`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 48.1 MB (48073590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee1236d68432abfbe0e2c1f5421adb5f913cf0c6e86728e51ee487789ab7c09`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 22.2 MB (22197942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a06dab86f6432e6f1830e226513c20fc301cfa593a32cd353fa027bbc15ee9`  
		Last Modified: Tue, 07 Jan 2025 08:37:57 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b9ac155e359247d7cb1f67b3a262378c152bb564e6b81de1a995578ceaed84`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d50c5fc2e43e90151e4bb9904c2501e53b67eb5fc11135d275874c918081cf`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:ba339f2c08a3f1e9f61705b928b793f687fc093875cb670f7b7a03435d26ad64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.7 KB (941719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e02475e9d5775a128692deb8c2d0eabcd35a7c1103dc2929ff31ff6dd1f5685`

```dockerfile
```

-	Layers:
	-	`sha256:a9629ee45cb1140ccd226502c5b6b76a3f67eb352e1f5f21d76b1f64b62249af`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 910.6 KB (910577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0008f6fc76aac14445ccc58ad2278bd6eb76709c39adffe8df99f443d4092d41`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 31.1 KB (31142 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:57429ef3f13cf25bbe541a54b2b831c1b339cfcf5bd060934f0a9ee5ed5428ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:813cce36a766ed3e3280b68b806591e64bbe9178c9c0a9b2ed7043aefd51695a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168524805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eaca693d9271123d11dd9b73a52b9c3e17d7c205b2622ca93655a48d5571c8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 19:42:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV GOSU_VER=1.16
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ceb32a7cd49428f5b5a5ecdd1169ca5237a4d72955d6b7133a61840eb79091d`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 9.6 MB (9596628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749e0ee9681ffcf4992ddb24b0513d74c3c5bd6a137f7319242ae00c7a9fb00d`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 5.8 MB (5820921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350078b5827c590786ffa202ff5e7d457f5ce17578e04d1c1e5a86907d8d2e51`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620187628669b47cda0dd9123d6c9ec83be49f919e909674af1b656bd2a4281f`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8498a0a81b137f0f34a91756d025ce39916bc2e1ac403fb93a57e65e68ab25`  
		Last Modified: Tue, 24 Dec 2024 22:27:29 GMT  
		Size: 100.3 MB (100312964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08b3e9f74aa64c19a1b7785476b8b6151394d3ba0fc7a6a2f18c10e2658cbc7`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 23.5 MB (23546387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05be0669f9759b48fa48b2e11d1e297cf54382244baee56db7d1149c70d06ca`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b93f8466c77b915f1de61395ec259eb44b54354c2d53ee034db9f1215f5c420`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d47214fe47b1e82ff5c4c4725fd2842f0155566df5b4abdd087474edf165344`  
		Last Modified: Tue, 24 Dec 2024 22:27:29 GMT  
		Size: 6.3 KB (6288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:af0aa27200123ebaae4036cbfa2c7ac252b56fa97dac7c2b75a045461f7ae17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9a0df5d8a90b8bbf29a9f81606240c49c6150b87fc84e91bf18e76ac7e5f57`

```dockerfile
```

-	Layers:
	-	`sha256:47b57e337cbcd6b24047353607188a10889c6b5f0822d71990b542b9c8a9ace1`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 2.8 MB (2848627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef6de32486cd7c360225f7fab7cc8f77b10dbdc34b79a0efcbd4df782741fa5`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 33.7 KB (33720 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:523c58ef436dff1687abca84e9a54addfb3fcb1fa6aa5f2fd289576a58e6027f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162212047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908a77248b8ad48410d69fd28dc03afab44d78d32ef05bea7c4fe076dc6a9fe4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 19:42:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV GOSU_VER=1.16
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74f53f4e2a360da5abfca2277671a38f9231b23bbf96fe58ded32e590ef860f`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 9.4 MB (9394168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873e4e4c9210bed2334d3c40b9b66323a577a4c23ae188832bca29ae670e0a75`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59454c66a11677c383ffe4680b394e13379bb05cac147fe4b312086e2a43285`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e3dabc2298cafd687c5cbf967781341f2e15cd6f85f115f836a038ab3a9af9`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cc306cb8755c7bae9b3e38280b9a79f104c2358b56f078eae8edbb5be86a1`  
		Last Modified: Wed, 25 Dec 2024 02:13:24 GMT  
		Size: 96.2 MB (96151368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b402f669421624c959471cad9b38c75225b0f0f587a572841a74fe19fc986042`  
		Last Modified: Wed, 25 Dec 2024 02:13:23 GMT  
		Size: 22.2 MB (22197941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e005371217bc51fc0b856c67c9f54f35e1e5758ba292026b01ed894e78c321`  
		Last Modified: Wed, 25 Dec 2024 02:13:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66135171293553a852be765599e3b866511b4cb599b7e57d836e8b10d32b8626`  
		Last Modified: Wed, 25 Dec 2024 02:13:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27705135a6a1dfdefecec1447d44ac97a81ed890397237d000e5a4e8257f0b76`  
		Last Modified: Wed, 25 Dec 2024 02:13:23 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:90b1c95d6993032369f780eced4a90848472245c3535c9d85bc149a4e56c13e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2881758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbe81027ea1eade69ba4df3afe0e9268289b5b4a441133efad4f5f3339715d3`

```dockerfile
```

-	Layers:
	-	`sha256:d4bc2167e531237007711f7480bc1e4253f2e91d05eabd195bd296f765a2d758`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 2.8 MB (2847855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8beb0a5dc5245ffc4a7f1f2db4c923e55fb59fd51625784376f017202f0dae2f`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 33.9 KB (33903 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:6fbb8ff2f014b783ed35d098aac3428448c81f470cbe5fb556719ace943cfa79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b4aae23172008e162b9a084342cdca5d1452ae4a059304da6a6fabd59f76af22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92813970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b3e3f8000016363e0a784f8edcbf98dc4aa46b9bd27ebdeca576ffecece05d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb92ac7301eb1d8a431d21e649728ac813a9810b06306e0816d682ad0be9ca0c`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c097ac5959ac8b7e5ce7e4625284fdc002f278072a8a534bbdea3ecd50e54c`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 9.7 MB (9664086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eb104e3f0244f28d748ea2d7e74df268bfc91d976a040efdd8b6472e202934`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 5.8 MB (5820946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89aa6391ecf05bcbe8b467dbf27ab8a43f13cc250042561a1d506468cb0d2b38`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab10afa0a468cd5771fd77f7f5063bdb5ad4ac335858959ab0bdf509b5ee136f`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 50.1 MB (50148313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33662d6cd32b83879dfbf57d88bbfcc6d967f3f0474808141c15bd937c018575`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 23.5 MB (23546400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c327bb004d758bbb8c21ea739fe8e4121de1461e28a6991b2d79db665075a004`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfda2b82a1866dcc3572daf050a9248464dc689cc9594f1322c28270c497df24`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ee9c3c3ab82c14c13a9355fe8cf4ce6147fb8f665e4d2403e6ec4d55430a70`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e64aa7820f3f75bfb9893c5c68463c206f04d425e64680274067fe3e3453b99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **948.2 KB (948152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101b1bdaf1a4935098a15031b753e4b76bf5700056850d7f9236ecc66b9ddae4`

```dockerfile
```

-	Layers:
	-	`sha256:23cbff2765458f31b583563fa71b23e8c50895a61da97a761de9b33301d22c7d`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 917.2 KB (917204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd3e60aa959b21ee324b6538f5b8a26f77d2fd9e22616fdd3c5271bfccbfc42`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:381be70cf44e73d9e0bc55f8d0cac1f5a08f4c9869dfbbeb2495d227ae98d0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89599718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76114aa77360041ce959a4d707e27c03f02956315bf52b5682e2158368002a88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce83109ec04193e8d1d95cc284000b3744402e6eb3a74774afb3a1dfca37714`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ae5757088c40ba9252bc398341fd4347da11535780149b3b39104b7d2d2c4`  
		Last Modified: Tue, 07 Jan 2025 08:37:57 GMT  
		Size: 9.8 MB (9769732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a0cb131d8295a6731b94e1af752bc44934519b9a440c2a25c516b0a53e121`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef225f1667c91e1c16b29bd860d533e6129d22ddb50151ed69e586ef708d62e9`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2039b5d949f249c870175a599013329b1e6f0631b518c33316e28879fa00b8`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 48.1 MB (48073590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee1236d68432abfbe0e2c1f5421adb5f913cf0c6e86728e51ee487789ab7c09`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 22.2 MB (22197942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a06dab86f6432e6f1830e226513c20fc301cfa593a32cd353fa027bbc15ee9`  
		Last Modified: Tue, 07 Jan 2025 08:37:57 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b9ac155e359247d7cb1f67b3a262378c152bb564e6b81de1a995578ceaed84`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d50c5fc2e43e90151e4bb9904c2501e53b67eb5fc11135d275874c918081cf`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:ba339f2c08a3f1e9f61705b928b793f687fc093875cb670f7b7a03435d26ad64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.7 KB (941719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e02475e9d5775a128692deb8c2d0eabcd35a7c1103dc2929ff31ff6dd1f5685`

```dockerfile
```

-	Layers:
	-	`sha256:a9629ee45cb1140ccd226502c5b6b76a3f67eb352e1f5f21d76b1f64b62249af`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 910.6 KB (910577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0008f6fc76aac14445ccc58ad2278bd6eb76709c39adffe8df99f443d4092d41`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 31.1 KB (31142 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.11`

```console
$ docker pull influxdb@sha256:57429ef3f13cf25bbe541a54b2b831c1b339cfcf5bd060934f0a9ee5ed5428ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.11` - linux; amd64

```console
$ docker pull influxdb@sha256:813cce36a766ed3e3280b68b806591e64bbe9178c9c0a9b2ed7043aefd51695a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168524805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eaca693d9271123d11dd9b73a52b9c3e17d7c205b2622ca93655a48d5571c8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 19:42:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV GOSU_VER=1.16
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ceb32a7cd49428f5b5a5ecdd1169ca5237a4d72955d6b7133a61840eb79091d`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 9.6 MB (9596628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749e0ee9681ffcf4992ddb24b0513d74c3c5bd6a137f7319242ae00c7a9fb00d`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 5.8 MB (5820921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350078b5827c590786ffa202ff5e7d457f5ce17578e04d1c1e5a86907d8d2e51`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620187628669b47cda0dd9123d6c9ec83be49f919e909674af1b656bd2a4281f`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8498a0a81b137f0f34a91756d025ce39916bc2e1ac403fb93a57e65e68ab25`  
		Last Modified: Tue, 24 Dec 2024 22:27:29 GMT  
		Size: 100.3 MB (100312964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08b3e9f74aa64c19a1b7785476b8b6151394d3ba0fc7a6a2f18c10e2658cbc7`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 23.5 MB (23546387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05be0669f9759b48fa48b2e11d1e297cf54382244baee56db7d1149c70d06ca`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b93f8466c77b915f1de61395ec259eb44b54354c2d53ee034db9f1215f5c420`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d47214fe47b1e82ff5c4c4725fd2842f0155566df5b4abdd087474edf165344`  
		Last Modified: Tue, 24 Dec 2024 22:27:29 GMT  
		Size: 6.3 KB (6288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:af0aa27200123ebaae4036cbfa2c7ac252b56fa97dac7c2b75a045461f7ae17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9a0df5d8a90b8bbf29a9f81606240c49c6150b87fc84e91bf18e76ac7e5f57`

```dockerfile
```

-	Layers:
	-	`sha256:47b57e337cbcd6b24047353607188a10889c6b5f0822d71990b542b9c8a9ace1`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 2.8 MB (2848627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef6de32486cd7c360225f7fab7cc8f77b10dbdc34b79a0efcbd4df782741fa5`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 33.7 KB (33720 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:523c58ef436dff1687abca84e9a54addfb3fcb1fa6aa5f2fd289576a58e6027f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162212047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908a77248b8ad48410d69fd28dc03afab44d78d32ef05bea7c4fe076dc6a9fe4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 19:42:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV GOSU_VER=1.16
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74f53f4e2a360da5abfca2277671a38f9231b23bbf96fe58ded32e590ef860f`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 9.4 MB (9394168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873e4e4c9210bed2334d3c40b9b66323a577a4c23ae188832bca29ae670e0a75`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59454c66a11677c383ffe4680b394e13379bb05cac147fe4b312086e2a43285`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e3dabc2298cafd687c5cbf967781341f2e15cd6f85f115f836a038ab3a9af9`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cc306cb8755c7bae9b3e38280b9a79f104c2358b56f078eae8edbb5be86a1`  
		Last Modified: Wed, 25 Dec 2024 02:13:24 GMT  
		Size: 96.2 MB (96151368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b402f669421624c959471cad9b38c75225b0f0f587a572841a74fe19fc986042`  
		Last Modified: Wed, 25 Dec 2024 02:13:23 GMT  
		Size: 22.2 MB (22197941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e005371217bc51fc0b856c67c9f54f35e1e5758ba292026b01ed894e78c321`  
		Last Modified: Wed, 25 Dec 2024 02:13:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66135171293553a852be765599e3b866511b4cb599b7e57d836e8b10d32b8626`  
		Last Modified: Wed, 25 Dec 2024 02:13:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27705135a6a1dfdefecec1447d44ac97a81ed890397237d000e5a4e8257f0b76`  
		Last Modified: Wed, 25 Dec 2024 02:13:23 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:90b1c95d6993032369f780eced4a90848472245c3535c9d85bc149a4e56c13e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2881758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbe81027ea1eade69ba4df3afe0e9268289b5b4a441133efad4f5f3339715d3`

```dockerfile
```

-	Layers:
	-	`sha256:d4bc2167e531237007711f7480bc1e4253f2e91d05eabd195bd296f765a2d758`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 2.8 MB (2847855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8beb0a5dc5245ffc4a7f1f2db4c923e55fb59fd51625784376f017202f0dae2f`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 33.9 KB (33903 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.11-alpine`

```console
$ docker pull influxdb@sha256:6fbb8ff2f014b783ed35d098aac3428448c81f470cbe5fb556719ace943cfa79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b4aae23172008e162b9a084342cdca5d1452ae4a059304da6a6fabd59f76af22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92813970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b3e3f8000016363e0a784f8edcbf98dc4aa46b9bd27ebdeca576ffecece05d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb92ac7301eb1d8a431d21e649728ac813a9810b06306e0816d682ad0be9ca0c`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c097ac5959ac8b7e5ce7e4625284fdc002f278072a8a534bbdea3ecd50e54c`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 9.7 MB (9664086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eb104e3f0244f28d748ea2d7e74df268bfc91d976a040efdd8b6472e202934`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 5.8 MB (5820946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89aa6391ecf05bcbe8b467dbf27ab8a43f13cc250042561a1d506468cb0d2b38`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab10afa0a468cd5771fd77f7f5063bdb5ad4ac335858959ab0bdf509b5ee136f`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 50.1 MB (50148313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33662d6cd32b83879dfbf57d88bbfcc6d967f3f0474808141c15bd937c018575`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 23.5 MB (23546400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c327bb004d758bbb8c21ea739fe8e4121de1461e28a6991b2d79db665075a004`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfda2b82a1866dcc3572daf050a9248464dc689cc9594f1322c28270c497df24`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ee9c3c3ab82c14c13a9355fe8cf4ce6147fb8f665e4d2403e6ec4d55430a70`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e64aa7820f3f75bfb9893c5c68463c206f04d425e64680274067fe3e3453b99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **948.2 KB (948152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101b1bdaf1a4935098a15031b753e4b76bf5700056850d7f9236ecc66b9ddae4`

```dockerfile
```

-	Layers:
	-	`sha256:23cbff2765458f31b583563fa71b23e8c50895a61da97a761de9b33301d22c7d`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 917.2 KB (917204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd3e60aa959b21ee324b6538f5b8a26f77d2fd9e22616fdd3c5271bfccbfc42`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:381be70cf44e73d9e0bc55f8d0cac1f5a08f4c9869dfbbeb2495d227ae98d0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89599718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76114aa77360041ce959a4d707e27c03f02956315bf52b5682e2158368002a88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce83109ec04193e8d1d95cc284000b3744402e6eb3a74774afb3a1dfca37714`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ae5757088c40ba9252bc398341fd4347da11535780149b3b39104b7d2d2c4`  
		Last Modified: Tue, 07 Jan 2025 08:37:57 GMT  
		Size: 9.8 MB (9769732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a0cb131d8295a6731b94e1af752bc44934519b9a440c2a25c516b0a53e121`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef225f1667c91e1c16b29bd860d533e6129d22ddb50151ed69e586ef708d62e9`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2039b5d949f249c870175a599013329b1e6f0631b518c33316e28879fa00b8`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 48.1 MB (48073590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee1236d68432abfbe0e2c1f5421adb5f913cf0c6e86728e51ee487789ab7c09`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 22.2 MB (22197942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a06dab86f6432e6f1830e226513c20fc301cfa593a32cd353fa027bbc15ee9`  
		Last Modified: Tue, 07 Jan 2025 08:37:57 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b9ac155e359247d7cb1f67b3a262378c152bb564e6b81de1a995578ceaed84`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d50c5fc2e43e90151e4bb9904c2501e53b67eb5fc11135d275874c918081cf`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:ba339f2c08a3f1e9f61705b928b793f687fc093875cb670f7b7a03435d26ad64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.7 KB (941719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e02475e9d5775a128692deb8c2d0eabcd35a7c1103dc2929ff31ff6dd1f5685`

```dockerfile
```

-	Layers:
	-	`sha256:a9629ee45cb1140ccd226502c5b6b76a3f67eb352e1f5f21d76b1f64b62249af`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 910.6 KB (910577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0008f6fc76aac14445ccc58ad2278bd6eb76709c39adffe8df99f443d4092d41`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 31.1 KB (31142 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:6fbb8ff2f014b783ed35d098aac3428448c81f470cbe5fb556719ace943cfa79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b4aae23172008e162b9a084342cdca5d1452ae4a059304da6a6fabd59f76af22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92813970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b3e3f8000016363e0a784f8edcbf98dc4aa46b9bd27ebdeca576ffecece05d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb92ac7301eb1d8a431d21e649728ac813a9810b06306e0816d682ad0be9ca0c`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c097ac5959ac8b7e5ce7e4625284fdc002f278072a8a534bbdea3ecd50e54c`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 9.7 MB (9664086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eb104e3f0244f28d748ea2d7e74df268bfc91d976a040efdd8b6472e202934`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 5.8 MB (5820946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89aa6391ecf05bcbe8b467dbf27ab8a43f13cc250042561a1d506468cb0d2b38`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab10afa0a468cd5771fd77f7f5063bdb5ad4ac335858959ab0bdf509b5ee136f`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 50.1 MB (50148313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33662d6cd32b83879dfbf57d88bbfcc6d967f3f0474808141c15bd937c018575`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 23.5 MB (23546400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c327bb004d758bbb8c21ea739fe8e4121de1461e28a6991b2d79db665075a004`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfda2b82a1866dcc3572daf050a9248464dc689cc9594f1322c28270c497df24`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ee9c3c3ab82c14c13a9355fe8cf4ce6147fb8f665e4d2403e6ec4d55430a70`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e64aa7820f3f75bfb9893c5c68463c206f04d425e64680274067fe3e3453b99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **948.2 KB (948152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101b1bdaf1a4935098a15031b753e4b76bf5700056850d7f9236ecc66b9ddae4`

```dockerfile
```

-	Layers:
	-	`sha256:23cbff2765458f31b583563fa71b23e8c50895a61da97a761de9b33301d22c7d`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 917.2 KB (917204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd3e60aa959b21ee324b6538f5b8a26f77d2fd9e22616fdd3c5271bfccbfc42`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:381be70cf44e73d9e0bc55f8d0cac1f5a08f4c9869dfbbeb2495d227ae98d0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89599718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76114aa77360041ce959a4d707e27c03f02956315bf52b5682e2158368002a88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce83109ec04193e8d1d95cc284000b3744402e6eb3a74774afb3a1dfca37714`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ae5757088c40ba9252bc398341fd4347da11535780149b3b39104b7d2d2c4`  
		Last Modified: Tue, 07 Jan 2025 08:37:57 GMT  
		Size: 9.8 MB (9769732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a0cb131d8295a6731b94e1af752bc44934519b9a440c2a25c516b0a53e121`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef225f1667c91e1c16b29bd860d533e6129d22ddb50151ed69e586ef708d62e9`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2039b5d949f249c870175a599013329b1e6f0631b518c33316e28879fa00b8`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 48.1 MB (48073590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee1236d68432abfbe0e2c1f5421adb5f913cf0c6e86728e51ee487789ab7c09`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 22.2 MB (22197942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a06dab86f6432e6f1830e226513c20fc301cfa593a32cd353fa027bbc15ee9`  
		Last Modified: Tue, 07 Jan 2025 08:37:57 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b9ac155e359247d7cb1f67b3a262378c152bb564e6b81de1a995578ceaed84`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d50c5fc2e43e90151e4bb9904c2501e53b67eb5fc11135d275874c918081cf`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:ba339f2c08a3f1e9f61705b928b793f687fc093875cb670f7b7a03435d26ad64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.7 KB (941719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e02475e9d5775a128692deb8c2d0eabcd35a7c1103dc2929ff31ff6dd1f5685`

```dockerfile
```

-	Layers:
	-	`sha256:a9629ee45cb1140ccd226502c5b6b76a3f67eb352e1f5f21d76b1f64b62249af`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 910.6 KB (910577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0008f6fc76aac14445ccc58ad2278bd6eb76709c39adffe8df99f443d4092d41`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 31.1 KB (31142 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:57429ef3f13cf25bbe541a54b2b831c1b339cfcf5bd060934f0a9ee5ed5428ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:813cce36a766ed3e3280b68b806591e64bbe9178c9c0a9b2ed7043aefd51695a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168524805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eaca693d9271123d11dd9b73a52b9c3e17d7c205b2622ca93655a48d5571c8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 19:42:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV GOSU_VER=1.16
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ceb32a7cd49428f5b5a5ecdd1169ca5237a4d72955d6b7133a61840eb79091d`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 9.6 MB (9596628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749e0ee9681ffcf4992ddb24b0513d74c3c5bd6a137f7319242ae00c7a9fb00d`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 5.8 MB (5820921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350078b5827c590786ffa202ff5e7d457f5ce17578e04d1c1e5a86907d8d2e51`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620187628669b47cda0dd9123d6c9ec83be49f919e909674af1b656bd2a4281f`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8498a0a81b137f0f34a91756d025ce39916bc2e1ac403fb93a57e65e68ab25`  
		Last Modified: Tue, 24 Dec 2024 22:27:29 GMT  
		Size: 100.3 MB (100312964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08b3e9f74aa64c19a1b7785476b8b6151394d3ba0fc7a6a2f18c10e2658cbc7`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 23.5 MB (23546387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05be0669f9759b48fa48b2e11d1e297cf54382244baee56db7d1149c70d06ca`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b93f8466c77b915f1de61395ec259eb44b54354c2d53ee034db9f1215f5c420`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d47214fe47b1e82ff5c4c4725fd2842f0155566df5b4abdd087474edf165344`  
		Last Modified: Tue, 24 Dec 2024 22:27:29 GMT  
		Size: 6.3 KB (6288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:af0aa27200123ebaae4036cbfa2c7ac252b56fa97dac7c2b75a045461f7ae17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9a0df5d8a90b8bbf29a9f81606240c49c6150b87fc84e91bf18e76ac7e5f57`

```dockerfile
```

-	Layers:
	-	`sha256:47b57e337cbcd6b24047353607188a10889c6b5f0822d71990b542b9c8a9ace1`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 2.8 MB (2848627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef6de32486cd7c360225f7fab7cc8f77b10dbdc34b79a0efcbd4df782741fa5`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 33.7 KB (33720 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:523c58ef436dff1687abca84e9a54addfb3fcb1fa6aa5f2fd289576a58e6027f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162212047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908a77248b8ad48410d69fd28dc03afab44d78d32ef05bea7c4fe076dc6a9fe4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 19:42:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV GOSU_VER=1.16
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74f53f4e2a360da5abfca2277671a38f9231b23bbf96fe58ded32e590ef860f`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 9.4 MB (9394168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873e4e4c9210bed2334d3c40b9b66323a577a4c23ae188832bca29ae670e0a75`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59454c66a11677c383ffe4680b394e13379bb05cac147fe4b312086e2a43285`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e3dabc2298cafd687c5cbf967781341f2e15cd6f85f115f836a038ab3a9af9`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 936.1 KB (936105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cc306cb8755c7bae9b3e38280b9a79f104c2358b56f078eae8edbb5be86a1`  
		Last Modified: Wed, 25 Dec 2024 02:13:24 GMT  
		Size: 96.2 MB (96151368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b402f669421624c959471cad9b38c75225b0f0f587a572841a74fe19fc986042`  
		Last Modified: Wed, 25 Dec 2024 02:13:23 GMT  
		Size: 22.2 MB (22197941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e005371217bc51fc0b856c67c9f54f35e1e5758ba292026b01ed894e78c321`  
		Last Modified: Wed, 25 Dec 2024 02:13:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66135171293553a852be765599e3b866511b4cb599b7e57d836e8b10d32b8626`  
		Last Modified: Wed, 25 Dec 2024 02:13:22 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27705135a6a1dfdefecec1447d44ac97a81ed890397237d000e5a4e8257f0b76`  
		Last Modified: Wed, 25 Dec 2024 02:13:23 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:90b1c95d6993032369f780eced4a90848472245c3535c9d85bc149a4e56c13e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2881758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbe81027ea1eade69ba4df3afe0e9268289b5b4a441133efad4f5f3339715d3`

```dockerfile
```

-	Layers:
	-	`sha256:d4bc2167e531237007711f7480bc1e4253f2e91d05eabd195bd296f765a2d758`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 2.8 MB (2847855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8beb0a5dc5245ffc4a7f1f2db4c923e55fb59fd51625784376f017202f0dae2f`  
		Last Modified: Wed, 25 Dec 2024 02:13:21 GMT  
		Size: 33.9 KB (33903 bytes)  
		MIME: application/vnd.in-toto+json
