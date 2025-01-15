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
$ docker pull influxdb@sha256:39870f108eea7b1ed4f84b0261307672d5a259cf1fdcb86f7a8fa4cb099967a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:2507470f3310d94a55624014e86d729ff79d3f98e77f9022a1847dec18f1055f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110678792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59785b5741b9c6404e937bfc5138005139750b84dcc1f99d9d0b2c562847caec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df16681c019573e3211da3a69493c28abc41e22e0cfaaf006fa4e8a20965295`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 15.6 MB (15558362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f843bf4971a19d5de58817bbc7743da0dedf18137454b966df9c08ded4f41d19`  
		Last Modified: Tue, 14 Jan 2025 03:18:24 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd01c84bc74826912c042c2638b4c171fdf0ccb7813ede5a761dc2b652ffd30`  
		Last Modified: Tue, 14 Jan 2025 22:31:55 GMT  
		Size: 41.4 MB (41377719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c5f0adbbc4cfe0632d88ab6b8a23d75fffe3c5cc86b62594630bdd14ee97e0`  
		Last Modified: Tue, 14 Jan 2025 03:18:24 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b4073029c54d14a93d3a6bb656b375964406df18903ae06c6a98a8694c9255`  
		Last Modified: Tue, 14 Jan 2025 03:18:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db57a86280756dde0ea223ed502e65c2d9244d33b047be70a2ef47a28228c74a`  
		Last Modified: Tue, 14 Jan 2025 03:18:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:eb691363742742095e54b12c2ae0dd64b8b344d6a7caca9a6fa78a7837beffe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4654042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecda1bca32b4024ae7aae71919b15d8e695a3bb49bb257c16d8a38c99eed31e1`

```dockerfile
```

-	Layers:
	-	`sha256:a459667215d277bb917787dd7c6917acef4e4a0c98813e634369ac7e7c26b63b`  
		Last Modified: Tue, 14 Jan 2025 03:18:24 GMT  
		Size: 4.6 MB (4639334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68c5cff5716b5e6a510923cf3b222f4ec3d41a931782ee5af13bd36a6028502f`  
		Last Modified: Tue, 14 Jan 2025 03:18:24 GMT  
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
$ docker pull influxdb@sha256:f7a366e5eb874c79121a3099306b3349bdaa11da77255ed345ba9054ece5d7e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:5023900c692f0b0d70e7d31615e340fe6f76a0b74f457d7f9871592a0836f31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89395436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47811169ebe59323d7ec779bd86ae0ca92e6807cfedc51cf54499795610ddd1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df16681c019573e3211da3a69493c28abc41e22e0cfaaf006fa4e8a20965295`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 15.6 MB (15558362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815d58d0ce7d9945424c4031fc2168275bf7c38b14513510be926c8f869ca154`  
		Last Modified: Tue, 14 Jan 2025 03:18:29 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305519f61d517f8f7bac45d466bb531b459c9390a3499f1f62d84d00a42a9aed`  
		Last Modified: Tue, 14 Jan 2025 03:18:29 GMT  
		Size: 20.1 MB (20095559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595910b0aa9a68429fdd0e340856e0bf17d886067c637098fcca3a662f21c3c4`  
		Last Modified: Tue, 14 Jan 2025 03:18:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619b9071116d5eca1cf046c72ef880a9e47e77f03becbee1cdbb137b8f8581e7`  
		Last Modified: Tue, 14 Jan 2025 23:04:13 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:038e7a4a478be4560ca507901c078a17de8eb916f40956f8ebc5c8343a53a238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4576129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280ab6a77cab6898073711897194f4fdce2b2aece01d6b7ffbd469985ec1670a`

```dockerfile
```

-	Layers:
	-	`sha256:3d7efcb1ccd44fca2cbcbaf317b1983a3b9891656a5502a6a241b4a802099cda`  
		Last Modified: Tue, 14 Jan 2025 03:18:29 GMT  
		Size: 4.6 MB (4563062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:404e7cf7225aeb91ae53e23a956753ca161c0271fdc958ad0d32094a33b15d30`  
		Last Modified: Tue, 14 Jan 2025 03:18:29 GMT  
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
$ docker pull influxdb@sha256:39870f108eea7b1ed4f84b0261307672d5a259cf1fdcb86f7a8fa4cb099967a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:2507470f3310d94a55624014e86d729ff79d3f98e77f9022a1847dec18f1055f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110678792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59785b5741b9c6404e937bfc5138005139750b84dcc1f99d9d0b2c562847caec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df16681c019573e3211da3a69493c28abc41e22e0cfaaf006fa4e8a20965295`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 15.6 MB (15558362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f843bf4971a19d5de58817bbc7743da0dedf18137454b966df9c08ded4f41d19`  
		Last Modified: Tue, 14 Jan 2025 03:18:24 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd01c84bc74826912c042c2638b4c171fdf0ccb7813ede5a761dc2b652ffd30`  
		Last Modified: Tue, 14 Jan 2025 22:31:55 GMT  
		Size: 41.4 MB (41377719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c5f0adbbc4cfe0632d88ab6b8a23d75fffe3c5cc86b62594630bdd14ee97e0`  
		Last Modified: Tue, 14 Jan 2025 03:18:24 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b4073029c54d14a93d3a6bb656b375964406df18903ae06c6a98a8694c9255`  
		Last Modified: Tue, 14 Jan 2025 03:18:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db57a86280756dde0ea223ed502e65c2d9244d33b047be70a2ef47a28228c74a`  
		Last Modified: Tue, 14 Jan 2025 03:18:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:eb691363742742095e54b12c2ae0dd64b8b344d6a7caca9a6fa78a7837beffe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4654042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecda1bca32b4024ae7aae71919b15d8e695a3bb49bb257c16d8a38c99eed31e1`

```dockerfile
```

-	Layers:
	-	`sha256:a459667215d277bb917787dd7c6917acef4e4a0c98813e634369ac7e7c26b63b`  
		Last Modified: Tue, 14 Jan 2025 03:18:24 GMT  
		Size: 4.6 MB (4639334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68c5cff5716b5e6a510923cf3b222f4ec3d41a931782ee5af13bd36a6028502f`  
		Last Modified: Tue, 14 Jan 2025 03:18:24 GMT  
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
$ docker pull influxdb@sha256:f7a366e5eb874c79121a3099306b3349bdaa11da77255ed345ba9054ece5d7e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:5023900c692f0b0d70e7d31615e340fe6f76a0b74f457d7f9871592a0836f31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89395436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47811169ebe59323d7ec779bd86ae0ca92e6807cfedc51cf54499795610ddd1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df16681c019573e3211da3a69493c28abc41e22e0cfaaf006fa4e8a20965295`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 15.6 MB (15558362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815d58d0ce7d9945424c4031fc2168275bf7c38b14513510be926c8f869ca154`  
		Last Modified: Tue, 14 Jan 2025 03:18:29 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305519f61d517f8f7bac45d466bb531b459c9390a3499f1f62d84d00a42a9aed`  
		Last Modified: Tue, 14 Jan 2025 03:18:29 GMT  
		Size: 20.1 MB (20095559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595910b0aa9a68429fdd0e340856e0bf17d886067c637098fcca3a662f21c3c4`  
		Last Modified: Tue, 14 Jan 2025 03:18:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619b9071116d5eca1cf046c72ef880a9e47e77f03becbee1cdbb137b8f8581e7`  
		Last Modified: Tue, 14 Jan 2025 23:04:13 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:038e7a4a478be4560ca507901c078a17de8eb916f40956f8ebc5c8343a53a238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4576129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280ab6a77cab6898073711897194f4fdce2b2aece01d6b7ffbd469985ec1670a`

```dockerfile
```

-	Layers:
	-	`sha256:3d7efcb1ccd44fca2cbcbaf317b1983a3b9891656a5502a6a241b4a802099cda`  
		Last Modified: Tue, 14 Jan 2025 03:18:29 GMT  
		Size: 4.6 MB (4563062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:404e7cf7225aeb91ae53e23a956753ca161c0271fdc958ad0d32094a33b15d30`  
		Last Modified: Tue, 14 Jan 2025 03:18:29 GMT  
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
$ docker pull influxdb@sha256:1bca0bba0f9cced0dbe51010adb6990191ddad8b2637732d4b73b232bd52a1d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:a6714b6cfc5772f8cece1a5a13f8cbf1bbe8f43ac3bb17448259b876da3839d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116191572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ee7b2b141688817cee7d93981fcb4042bf539e1f612ee33949d6623d807a9e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac5ef82637710357b1bd479867f6a3cfe19cc66bb329812267313f8a18599ac`  
		Last Modified: Tue, 14 Jan 2025 21:59:49 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf3fd955fd2d52478a323c82775173e4d728b23505a0d1ca25f3ad804825848`  
		Last Modified: Tue, 14 Jan 2025 20:58:35 GMT  
		Size: 43.7 MB (43650057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436b1cff4229edc765e30c4d61bf037a3737931fde40f606cbbe26f41b1abb86`  
		Last Modified: Tue, 14 Jan 2025 20:58:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb056dd6b6abfc892ec2dc1b63502397f8af8141755b4b8fe49cacea12661df`  
		Last Modified: Tue, 14 Jan 2025 20:50:05 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6579b304e8f3cc09e488a9a1ef6f441117a86c7bd276e59f1473506c819d1d4`  
		Last Modified: Tue, 14 Jan 2025 03:22:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:41f0eef1fdba8551a5b89a86221795674f65b31de7119b9190d77b8a1064b2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4901198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c705a261e2123979604a0330270cdeeed6a71128f4031b342ea753bbd30572`

```dockerfile
```

-	Layers:
	-	`sha256:2b1dd6de6dbf63cd673204161482fe479ab2ed39ac73fb4a84f4f63e680b0359`  
		Last Modified: Tue, 14 Jan 2025 03:22:18 GMT  
		Size: 4.9 MB (4885669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14a4feddcc4fc3625f8b3cd463e2d2e0a767df31be5d8f8995af53287ee3dc96`  
		Last Modified: Tue, 14 Jan 2025 03:22:18 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c2756556b0ee84f888041284d8cee574f70ed945ae7c2ce264d082a7e17c342c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113026919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2694772a56b8a91aa5e49715afc298f9a4cf4390ef5b8f7320052e3f5dab6b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612589b99cd4e395b49feed63a4d6ebf4d4d6221bc5ff24b10981018ca42a538`  
		Last Modified: Tue, 14 Jan 2025 14:18:16 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c217212f689d768b2c47c3c131485c26ecfe79a5c4f8334491ec71b0d6fcf`  
		Last Modified: Tue, 14 Jan 2025 14:18:18 GMT  
		Size: 41.1 MB (41118890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d380c88ca3ab72b0f7faca1a4c8557d096cd4925469c62c5d2079457ddccd0a`  
		Last Modified: Wed, 15 Jan 2025 00:57:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd7ea6f8cec865b5e3292a1ee6dc0d10a1299451cbce42154a6dac59d1a04b5`  
		Last Modified: Tue, 14 Jan 2025 22:08:49 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc762261c5183c2ec4b7ecc6c87cb5d9dbc063b0a5304b7a1034f3e733877bc`  
		Last Modified: Tue, 14 Jan 2025 14:18:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:c4b02cac774688a7007a61570346ecfb3694925d6ee8834eeef064e286a53016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4900758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93759512d969e299a749b056ecba4d5da429b788bb3161d101ac58f2b49e12b7`

```dockerfile
```

-	Layers:
	-	`sha256:fd34b92a05dafa7fcc66e4a40a6c81be625e72fd87bf6a3ae43fa09bf65fbd95`  
		Last Modified: Tue, 14 Jan 2025 14:18:16 GMT  
		Size: 4.9 MB (4885134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b5994c8322f2c601f1cacdadf44d07f3c4182097b0ab0c64b80350acc55f4e6`  
		Last Modified: Wed, 15 Jan 2025 00:57:58 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-alpine`

```console
$ docker pull influxdb@sha256:3487962145165318a5d0fea062f5a6da428eb08cae252722c133d29c7771fec8
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
		Last Modified: Tue, 14 Jan 2025 21:01:00 GMT  
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
		Last Modified: Tue, 14 Jan 2025 21:00:59 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589fcf38227a5dcec2a2be6e3958607e24412871750573d86414b8c084d00a64`  
		Last Modified: Tue, 14 Jan 2025 20:57:58 GMT  
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
$ docker pull influxdb@sha256:f33ee19d94b2f15c650e7f7e5beeac8093f58fb5e2f0944efb6a360f3de0421e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40946189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623ab937f829e91a4579539cb408b46fe75653a38b61b4f1345676d282952c5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59967a70201a307f2756194a4e3808889a095471a935132f3c8676f54a30c372`  
		Last Modified: Wed, 15 Jan 2025 00:33:17 GMT  
		Size: 1.3 MB (1307200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449059cddf29a2e6c10fe3fe8bfa9f9256d2065d36e5bb8b6e10da2a02e44516`  
		Last Modified: Wed, 08 Jan 2025 23:33:09 GMT  
		Size: 35.5 MB (35545503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c9187bdc07865d322a8d030ccfed300cd01570304843fa1b7b1ec6ac68867b`  
		Last Modified: Wed, 08 Jan 2025 23:33:08 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3636da9a842f162008334a7e878f1413fcdb2092ec1639396928e3354a5eb1a`  
		Last Modified: Wed, 08 Jan 2025 23:33:08 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4715c870454a08fa860d453ffaee304c8f262275829d266566a688d215688f72`  
		Last Modified: Wed, 15 Jan 2025 00:33:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780a0a2f70876e851b20c48fde069851b1721e1e95d375bfa487638d88fcb957`  
		Last Modified: Wed, 15 Jan 2025 00:33:18 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:8e2d4324188f09deb37bed8d3c9ad2b7fa77db77de29fb9ba2699c040778f3ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.5 KB (760535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ecd23ee6923cc3a71c178833f386d047e0b03389806f698eb37bc956914e3a`

```dockerfile
```

-	Layers:
	-	`sha256:df80b63c84ce4412b20ce650e226de12a3b4815d852e7c88ad14ec50c4cd2ecb`  
		Last Modified: Wed, 08 Jan 2025 23:33:08 GMT  
		Size: 742.5 KB (742548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f9a6319cc4554d90e05f7013af6229fc5164a828b7d1796b3e951ab923b652`  
		Last Modified: Wed, 08 Jan 2025 23:33:08 GMT  
		Size: 18.0 KB (17987 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:69bad1ef220a8e894fcbf0a0d1867c5036c4ac41831e4888c5b4a9374a87571d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:8310320a9bd6bba9425eac468bef9612c37b2f70219c0c31a3e4eef1ae4d69f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111721463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e486fd782e522e0297cad6dda5c1cc35d03c75c2395d607daa9779ebfe6304c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d71040886da717e67344a94801e2a8f09fe448f700806175ce96c0dd1f39311`  
		Last Modified: Tue, 14 Jan 2025 03:18:23 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db8c73b2bf7148a891d1f66c6704ec105f5f95f7f4f9e8bcf7760b9c42b3bd6`  
		Last Modified: Tue, 14 Jan 2025 22:35:30 GMT  
		Size: 39.2 MB (39179311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95eb91c1db7f4e5f747c1cd73f98d672c866c97c53d495edf5a7a28f083fca00`  
		Last Modified: Tue, 14 Jan 2025 22:35:24 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b4073029c54d14a93d3a6bb656b375964406df18903ae06c6a98a8694c9255`  
		Last Modified: Tue, 14 Jan 2025 03:18:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db57a86280756dde0ea223ed502e65c2d9244d33b047be70a2ef47a28228c74a`  
		Last Modified: Tue, 14 Jan 2025 03:18:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:4aa709cc3b2ce16ca710599b538603144fdf04b8e27ddaf588d0da223f215d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4526289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0ff1953414558edc9106ff4ae73254e940be4924af867de9cb4b7d9343a0ff`

```dockerfile
```

-	Layers:
	-	`sha256:91ad23689de82038d1c5aeaeb4367d9c438cd5fe71e4ec2475d9af5c3d00693e`  
		Last Modified: Tue, 14 Jan 2025 03:18:23 GMT  
		Size: 4.5 MB (4511581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3488c2af65c36b8d2efe32f545bc7928af94df4269cde24d123719b203d0187`  
		Last Modified: Tue, 14 Jan 2025 03:18:23 GMT  
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
$ docker pull influxdb@sha256:a1ff6f236f6b9a70d91a2c6c94dc51025e3c73dc6fffbf9d52515b7c725c6ef2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c8c389672dabbe1f4b625a668ece23a6176e5f8ef401344ebf1adc697e21f631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90877531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725ffb36b1dffea5e2cd9ce722703c79d3cbe78155624b3a399a1722577eeb4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc99d27fb005036624db521bc491c474af38f42ef438d3aed59a127160100534`  
		Last Modified: Tue, 14 Jan 2025 03:18:27 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7720ca594cbb5bae7bfebb72a9bbd0f909dbc4ad683e4ab8d8c550a82dc25037`  
		Last Modified: Tue, 14 Jan 2025 21:47:24 GMT  
		Size: 18.3 MB (18336574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc855ad0237b0991ccca68a014de3e8311e0965a4e31b138467e5eff7e2e3cf2`  
		Last Modified: Tue, 14 Jan 2025 22:37:22 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c77492d9c52583d7a8fabe49e6fab7760d25cef8a39d0cb8b0a464c35a4877e`  
		Last Modified: Tue, 14 Jan 2025 03:18:27 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:b9bdc2aba4001b6d308423ed5c1a9fbe81a8d71c68fc3aa47be51291bda014b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4449367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6131c49096e12377185104f20d988352770c7147904a374fca53cf4809fb43b1`

```dockerfile
```

-	Layers:
	-	`sha256:7f507a5a445aa57c663266b8731b2d6f55a77be611ad56c200ef8719bc0f5ca1`  
		Last Modified: Tue, 14 Jan 2025 03:18:28 GMT  
		Size: 4.4 MB (4436300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b5faa5f782608737cfdd538e756c176c135162ce7d37e984c95ba7c1a8df97`  
		Last Modified: Tue, 14 Jan 2025 03:18:27 GMT  
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
$ docker pull influxdb@sha256:1bca0bba0f9cced0dbe51010adb6990191ddad8b2637732d4b73b232bd52a1d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:a6714b6cfc5772f8cece1a5a13f8cbf1bbe8f43ac3bb17448259b876da3839d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116191572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ee7b2b141688817cee7d93981fcb4042bf539e1f612ee33949d6623d807a9e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac5ef82637710357b1bd479867f6a3cfe19cc66bb329812267313f8a18599ac`  
		Last Modified: Tue, 14 Jan 2025 21:59:49 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf3fd955fd2d52478a323c82775173e4d728b23505a0d1ca25f3ad804825848`  
		Last Modified: Tue, 14 Jan 2025 20:58:35 GMT  
		Size: 43.7 MB (43650057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436b1cff4229edc765e30c4d61bf037a3737931fde40f606cbbe26f41b1abb86`  
		Last Modified: Tue, 14 Jan 2025 20:58:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb056dd6b6abfc892ec2dc1b63502397f8af8141755b4b8fe49cacea12661df`  
		Last Modified: Tue, 14 Jan 2025 20:50:05 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6579b304e8f3cc09e488a9a1ef6f441117a86c7bd276e59f1473506c819d1d4`  
		Last Modified: Tue, 14 Jan 2025 03:22:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:41f0eef1fdba8551a5b89a86221795674f65b31de7119b9190d77b8a1064b2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4901198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c705a261e2123979604a0330270cdeeed6a71128f4031b342ea753bbd30572`

```dockerfile
```

-	Layers:
	-	`sha256:2b1dd6de6dbf63cd673204161482fe479ab2ed39ac73fb4a84f4f63e680b0359`  
		Last Modified: Tue, 14 Jan 2025 03:22:18 GMT  
		Size: 4.9 MB (4885669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14a4feddcc4fc3625f8b3cd463e2d2e0a767df31be5d8f8995af53287ee3dc96`  
		Last Modified: Tue, 14 Jan 2025 03:22:18 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c2756556b0ee84f888041284d8cee574f70ed945ae7c2ce264d082a7e17c342c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113026919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2694772a56b8a91aa5e49715afc298f9a4cf4390ef5b8f7320052e3f5dab6b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612589b99cd4e395b49feed63a4d6ebf4d4d6221bc5ff24b10981018ca42a538`  
		Last Modified: Tue, 14 Jan 2025 14:18:16 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c217212f689d768b2c47c3c131485c26ecfe79a5c4f8334491ec71b0d6fcf`  
		Last Modified: Tue, 14 Jan 2025 14:18:18 GMT  
		Size: 41.1 MB (41118890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d380c88ca3ab72b0f7faca1a4c8557d096cd4925469c62c5d2079457ddccd0a`  
		Last Modified: Wed, 15 Jan 2025 00:57:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd7ea6f8cec865b5e3292a1ee6dc0d10a1299451cbce42154a6dac59d1a04b5`  
		Last Modified: Tue, 14 Jan 2025 22:08:49 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc762261c5183c2ec4b7ecc6c87cb5d9dbc063b0a5304b7a1034f3e733877bc`  
		Last Modified: Tue, 14 Jan 2025 14:18:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:c4b02cac774688a7007a61570346ecfb3694925d6ee8834eeef064e286a53016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4900758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93759512d969e299a749b056ecba4d5da429b788bb3161d101ac58f2b49e12b7`

```dockerfile
```

-	Layers:
	-	`sha256:fd34b92a05dafa7fcc66e4a40a6c81be625e72fd87bf6a3ae43fa09bf65fbd95`  
		Last Modified: Tue, 14 Jan 2025 14:18:16 GMT  
		Size: 4.9 MB (4885134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b5994c8322f2c601f1cacdadf44d07f3c4182097b0ab0c64b80350acc55f4e6`  
		Last Modified: Wed, 15 Jan 2025 00:57:58 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-alpine`

```console
$ docker pull influxdb@sha256:3487962145165318a5d0fea062f5a6da428eb08cae252722c133d29c7771fec8
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
		Last Modified: Tue, 14 Jan 2025 21:01:00 GMT  
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
		Last Modified: Tue, 14 Jan 2025 21:00:59 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589fcf38227a5dcec2a2be6e3958607e24412871750573d86414b8c084d00a64`  
		Last Modified: Tue, 14 Jan 2025 20:57:58 GMT  
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
$ docker pull influxdb@sha256:f33ee19d94b2f15c650e7f7e5beeac8093f58fb5e2f0944efb6a360f3de0421e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40946189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623ab937f829e91a4579539cb408b46fe75653a38b61b4f1345676d282952c5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59967a70201a307f2756194a4e3808889a095471a935132f3c8676f54a30c372`  
		Last Modified: Wed, 15 Jan 2025 00:33:17 GMT  
		Size: 1.3 MB (1307200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449059cddf29a2e6c10fe3fe8bfa9f9256d2065d36e5bb8b6e10da2a02e44516`  
		Last Modified: Wed, 08 Jan 2025 23:33:09 GMT  
		Size: 35.5 MB (35545503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c9187bdc07865d322a8d030ccfed300cd01570304843fa1b7b1ec6ac68867b`  
		Last Modified: Wed, 08 Jan 2025 23:33:08 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3636da9a842f162008334a7e878f1413fcdb2092ec1639396928e3354a5eb1a`  
		Last Modified: Wed, 08 Jan 2025 23:33:08 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4715c870454a08fa860d453ffaee304c8f262275829d266566a688d215688f72`  
		Last Modified: Wed, 15 Jan 2025 00:33:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780a0a2f70876e851b20c48fde069851b1721e1e95d375bfa487638d88fcb957`  
		Last Modified: Wed, 15 Jan 2025 00:33:18 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:8e2d4324188f09deb37bed8d3c9ad2b7fa77db77de29fb9ba2699c040778f3ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.5 KB (760535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ecd23ee6923cc3a71c178833f386d047e0b03389806f698eb37bc956914e3a`

```dockerfile
```

-	Layers:
	-	`sha256:df80b63c84ce4412b20ce650e226de12a3b4815d852e7c88ad14ec50c4cd2ecb`  
		Last Modified: Wed, 08 Jan 2025 23:33:08 GMT  
		Size: 742.5 KB (742548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f9a6319cc4554d90e05f7013af6229fc5164a828b7d1796b3e951ab923b652`  
		Last Modified: Wed, 08 Jan 2025 23:33:08 GMT  
		Size: 18.0 KB (17987 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-data`

```console
$ docker pull influxdb@sha256:69bad1ef220a8e894fcbf0a0d1867c5036c4ac41831e4888c5b4a9374a87571d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:8310320a9bd6bba9425eac468bef9612c37b2f70219c0c31a3e4eef1ae4d69f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111721463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e486fd782e522e0297cad6dda5c1cc35d03c75c2395d607daa9779ebfe6304c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d71040886da717e67344a94801e2a8f09fe448f700806175ce96c0dd1f39311`  
		Last Modified: Tue, 14 Jan 2025 03:18:23 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db8c73b2bf7148a891d1f66c6704ec105f5f95f7f4f9e8bcf7760b9c42b3bd6`  
		Last Modified: Tue, 14 Jan 2025 22:35:30 GMT  
		Size: 39.2 MB (39179311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95eb91c1db7f4e5f747c1cd73f98d672c866c97c53d495edf5a7a28f083fca00`  
		Last Modified: Tue, 14 Jan 2025 22:35:24 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b4073029c54d14a93d3a6bb656b375964406df18903ae06c6a98a8694c9255`  
		Last Modified: Tue, 14 Jan 2025 03:18:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db57a86280756dde0ea223ed502e65c2d9244d33b047be70a2ef47a28228c74a`  
		Last Modified: Tue, 14 Jan 2025 03:18:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:4aa709cc3b2ce16ca710599b538603144fdf04b8e27ddaf588d0da223f215d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4526289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0ff1953414558edc9106ff4ae73254e940be4924af867de9cb4b7d9343a0ff`

```dockerfile
```

-	Layers:
	-	`sha256:91ad23689de82038d1c5aeaeb4367d9c438cd5fe71e4ec2475d9af5c3d00693e`  
		Last Modified: Tue, 14 Jan 2025 03:18:23 GMT  
		Size: 4.5 MB (4511581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3488c2af65c36b8d2efe32f545bc7928af94df4269cde24d123719b203d0187`  
		Last Modified: Tue, 14 Jan 2025 03:18:23 GMT  
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
$ docker pull influxdb@sha256:a1ff6f236f6b9a70d91a2c6c94dc51025e3c73dc6fffbf9d52515b7c725c6ef2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c8c389672dabbe1f4b625a668ece23a6176e5f8ef401344ebf1adc697e21f631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90877531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725ffb36b1dffea5e2cd9ce722703c79d3cbe78155624b3a399a1722577eeb4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc99d27fb005036624db521bc491c474af38f42ef438d3aed59a127160100534`  
		Last Modified: Tue, 14 Jan 2025 03:18:27 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7720ca594cbb5bae7bfebb72a9bbd0f909dbc4ad683e4ab8d8c550a82dc25037`  
		Last Modified: Tue, 14 Jan 2025 21:47:24 GMT  
		Size: 18.3 MB (18336574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc855ad0237b0991ccca68a014de3e8311e0965a4e31b138467e5eff7e2e3cf2`  
		Last Modified: Tue, 14 Jan 2025 22:37:22 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c77492d9c52583d7a8fabe49e6fab7760d25cef8a39d0cb8b0a464c35a4877e`  
		Last Modified: Tue, 14 Jan 2025 03:18:27 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:b9bdc2aba4001b6d308423ed5c1a9fbe81a8d71c68fc3aa47be51291bda014b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4449367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6131c49096e12377185104f20d988352770c7147904a374fca53cf4809fb43b1`

```dockerfile
```

-	Layers:
	-	`sha256:7f507a5a445aa57c663266b8731b2d6f55a77be611ad56c200ef8719bc0f5ca1`  
		Last Modified: Tue, 14 Jan 2025 03:18:28 GMT  
		Size: 4.4 MB (4436300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b5faa5f782608737cfdd538e756c176c135162ce7d37e984c95ba7c1a8df97`  
		Last Modified: Tue, 14 Jan 2025 03:18:27 GMT  
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
$ docker pull influxdb@sha256:e9fc35b36536bfdeb3defe5a59c3a2e21465daea3902a577f0e5b752118a2e51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:6fb91c63e3e0106229d8cc9e6a437269bfd345bf2b6d4da4ce18b2ceed2eb293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168699095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762afe4bc6cf8930c1773cbf37dd6dd8af169093b56113bb60cdb51fca1c97b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab40758896b65a4bb3ecc6b0714efc0d4e173fd91a5f7b3ff93a25c5c0933e39`  
		Last Modified: Tue, 14 Jan 2025 02:34:36 GMT  
		Size: 9.8 MB (9790077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a38212e5b040080b41465e28d7fec7d8c3460bab9113cc22ccba62256d591e`  
		Last Modified: Tue, 14 Jan 2025 02:34:36 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d579e8989044770546dd3a4c57acae66413db8a1165bd38f03c1f8e5e8359e41`  
		Last Modified: Tue, 14 Jan 2025 02:34:35 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c53dd9bd71de0ae46e6bb0614682e00a57fef88b7ff18ac6b573bf80c4673d`  
		Last Modified: Tue, 14 Jan 2025 02:34:36 GMT  
		Size: 1.0 MB (1006368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a805a4428ab388207d8b9390ce109b35289509383eb313269128b291de2067fc`  
		Last Modified: Tue, 14 Jan 2025 02:34:38 GMT  
		Size: 100.3 MB (100312930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b94cb7724f533cdf21ec0c7c3bddadd853fbee31f2228bf59187adfebc411a`  
		Last Modified: Tue, 14 Jan 2025 02:34:37 GMT  
		Size: 23.5 MB (23546410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12b7823fa53078a98ebd2bf76a476558a236bb4b29471cffcdfc8d7358f9da8`  
		Last Modified: Tue, 14 Jan 2025 20:33:12 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f44532ba7abe4af6ee25a1d9f6f7af98640a98f144f23df14a06bd2b32d6b7`  
		Last Modified: Tue, 14 Jan 2025 02:34:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20762f0e055147938113d79964ba71d000b9d5db7d726df9bb046433b3fc167`  
		Last Modified: Tue, 14 Jan 2025 20:33:20 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:eeda7fdc817783ae62c9ab8296274e5be37e96828b3c9d24aaf3eecdebd153d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e06a90a1d26723c375027f886c402833ab03e6cfadbab9a178e9ef6aefd8fa`

```dockerfile
```

-	Layers:
	-	`sha256:ab07f397ef4ff3ca4bd09847db03b5be8dff55b56d1bfcc7775a6fea9023fd6d`  
		Last Modified: Tue, 14 Jan 2025 22:04:34 GMT  
		Size: 2.8 MB (2848627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccdf399dde11679520acf0d1e70bdc544cee80f0cca0270bf0f45064434bf945`  
		Last Modified: Tue, 14 Jan 2025 22:04:36 GMT  
		Size: 33.7 KB (33719 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4f674ba91d974cc8fd9fca55df891e89b9fc4ed70589ae274a876b2d3fee3814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162387572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a0fae1e3e393bd81064a5a47039c9fec27a2f77c8be95795a3dc1466ad81ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0519160658aa38aa8ec1a9223db51f24ef66cec37c87e5d3252a5b1636bf481`  
		Last Modified: Tue, 14 Jan 2025 07:23:55 GMT  
		Size: 9.6 MB (9587362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a8b4761500ec9c11b5fdbefce98c329f2d5853652b2434b1f174b192974be0`  
		Last Modified: Tue, 14 Jan 2025 07:23:54 GMT  
		Size: 5.5 MB (5463786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6470a1080b2858907cf5c6754c4f40e5a95cd979fd29fff60cfdbb7ebb55dee1`  
		Last Modified: Tue, 14 Jan 2025 07:23:54 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fcbe061689e52b7c5b7929a1aceb8ec5d535130bed1d5acffbfdc7eff569dd`  
		Last Modified: Tue, 14 Jan 2025 07:23:54 GMT  
		Size: 936.1 KB (936104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6484dfd2b5865354d6aee22d73005c5ab86111bbdfd94d57c132d963b06c3`  
		Last Modified: Tue, 14 Jan 2025 07:23:58 GMT  
		Size: 96.2 MB (96151392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45f168297634a1e2c074e189b69dc1ab2be83fec68ef455e38b51176c537c66`  
		Last Modified: Tue, 14 Jan 2025 07:23:56 GMT  
		Size: 22.2 MB (22197942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0470c74fd97d622094d009fac154789ef2980d85506e607abc3cb8b6c8e8565`  
		Last Modified: Tue, 14 Jan 2025 20:36:12 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d253f731479a5ca137c2c54178b12c934a42e48ff4291854e0cd1c204d00ebb6`  
		Last Modified: Tue, 14 Jan 2025 20:36:18 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef753136aa92703545b2667815093321a19c5789fcd04c5dd4856dea68a6c057`  
		Last Modified: Tue, 14 Jan 2025 20:33:48 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:6009930905c9627c0d9d66b0c42932b69c39a1ba551d0b15f0b246302d5f769f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2881758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a094fa8745410e40423d0f9f4341a941cf34e40c450ca4468f7eb6d24fddbd`

```dockerfile
```

-	Layers:
	-	`sha256:20efc527a51d42a77be3f33e586725bb27964134cfe6f4e9426ee9b7d4758eec`  
		Last Modified: Tue, 14 Jan 2025 22:06:58 GMT  
		Size: 2.8 MB (2847855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a6b56548878df25c8f32a7dad31954a8b257013a5a225a66d2cfc4ceb9804e`  
		Last Modified: Wed, 15 Jan 2025 01:05:28 GMT  
		Size: 33.9 KB (33903 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:21e7caba25c83e7f05898f08b65e0cd843e7c5c3233a909574d3004e82d6a92a
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
		Last Modified: Tue, 14 Jan 2025 20:44:28 GMT  
		Size: 9.7 MB (9664086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eb104e3f0244f28d748ea2d7e74df268bfc91d976a040efdd8b6472e202934`  
		Last Modified: Tue, 14 Jan 2025 20:55:50 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:44:11 GMT  
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
		Last Modified: Wed, 15 Jan 2025 00:38:14 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:de8426562aae77d38978d64e05d0c3add2e8c49fff02eb6de6559b1d2ddeff21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89615883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5218ff2e3e43bebb55215894df96d326d54024bd5bedb8bcb3f695250ce6bee9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057a2e931604572012bfcfa32ff63d57c7e13b9484567fe86dea4678aa846576`  
		Last Modified: Wed, 08 Jan 2025 23:33:36 GMT  
		Size: 9.8 MB (9781847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40885a465df33fe6876f229a70e6e1f9d06f2e74a23dad03a739070e643f3f47`  
		Last Modified: Wed, 08 Jan 2025 23:33:35 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6593c403f08774a7b9b796fdb1f27730dde47c815cc79db25725134a0f0cb18`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0b8fa25bb2615a503c1807079fe1bac004ab1894073f1b4193761e7c27e328`  
		Last Modified: Wed, 08 Jan 2025 23:33:37 GMT  
		Size: 48.1 MB (48073560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eebc18de04e5c4e869da58da450854697b3a123aad83cbdc5544b062949fa0c`  
		Last Modified: Tue, 14 Jan 2025 22:07:40 GMT  
		Size: 22.2 MB (22197938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb157672269c8c03b1fd14c4ac2c6469970c7f7a51981c5ff08918c45c8d2aca`  
		Last Modified: Tue, 14 Jan 2025 21:02:02 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b407da3bbc26403fa957f2b202523c5fe99a199ef6a9bde6bca0e758d2541302`  
		Last Modified: Tue, 14 Jan 2025 23:45:16 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3edc6c59b2526c18e1658ce630e4c188730c211df9346aebc821c0028dbccbc`  
		Last Modified: Wed, 08 Jan 2025 23:33:37 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fe1bf94d7c78e453275d88beed4f073b9eb60f5f02d02da46e6a724ea40a9a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **947.6 KB (947598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d314bcb026bee756f637d82de95c5659a19518bb3c21816288760843eefa4802`

```dockerfile
```

-	Layers:
	-	`sha256:42ddaf62cf072af2e72f0e7652d389b1ab5c1436daec72fc92f10298ab02021a`  
		Last Modified: Wed, 15 Jan 2025 01:05:47 GMT  
		Size: 916.5 KB (916455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad1c5238ca3bbd3719b1a695f0d7b9de62192037bd8be847833ad60b6b375b6`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 31.1 KB (31143 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:e9fc35b36536bfdeb3defe5a59c3a2e21465daea3902a577f0e5b752118a2e51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:6fb91c63e3e0106229d8cc9e6a437269bfd345bf2b6d4da4ce18b2ceed2eb293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168699095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762afe4bc6cf8930c1773cbf37dd6dd8af169093b56113bb60cdb51fca1c97b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab40758896b65a4bb3ecc6b0714efc0d4e173fd91a5f7b3ff93a25c5c0933e39`  
		Last Modified: Tue, 14 Jan 2025 02:34:36 GMT  
		Size: 9.8 MB (9790077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a38212e5b040080b41465e28d7fec7d8c3460bab9113cc22ccba62256d591e`  
		Last Modified: Tue, 14 Jan 2025 02:34:36 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d579e8989044770546dd3a4c57acae66413db8a1165bd38f03c1f8e5e8359e41`  
		Last Modified: Tue, 14 Jan 2025 02:34:35 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c53dd9bd71de0ae46e6bb0614682e00a57fef88b7ff18ac6b573bf80c4673d`  
		Last Modified: Tue, 14 Jan 2025 02:34:36 GMT  
		Size: 1.0 MB (1006368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a805a4428ab388207d8b9390ce109b35289509383eb313269128b291de2067fc`  
		Last Modified: Tue, 14 Jan 2025 02:34:38 GMT  
		Size: 100.3 MB (100312930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b94cb7724f533cdf21ec0c7c3bddadd853fbee31f2228bf59187adfebc411a`  
		Last Modified: Tue, 14 Jan 2025 02:34:37 GMT  
		Size: 23.5 MB (23546410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12b7823fa53078a98ebd2bf76a476558a236bb4b29471cffcdfc8d7358f9da8`  
		Last Modified: Tue, 14 Jan 2025 20:33:12 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f44532ba7abe4af6ee25a1d9f6f7af98640a98f144f23df14a06bd2b32d6b7`  
		Last Modified: Tue, 14 Jan 2025 02:34:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20762f0e055147938113d79964ba71d000b9d5db7d726df9bb046433b3fc167`  
		Last Modified: Tue, 14 Jan 2025 20:33:20 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:eeda7fdc817783ae62c9ab8296274e5be37e96828b3c9d24aaf3eecdebd153d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e06a90a1d26723c375027f886c402833ab03e6cfadbab9a178e9ef6aefd8fa`

```dockerfile
```

-	Layers:
	-	`sha256:ab07f397ef4ff3ca4bd09847db03b5be8dff55b56d1bfcc7775a6fea9023fd6d`  
		Last Modified: Tue, 14 Jan 2025 22:04:34 GMT  
		Size: 2.8 MB (2848627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccdf399dde11679520acf0d1e70bdc544cee80f0cca0270bf0f45064434bf945`  
		Last Modified: Tue, 14 Jan 2025 22:04:36 GMT  
		Size: 33.7 KB (33719 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4f674ba91d974cc8fd9fca55df891e89b9fc4ed70589ae274a876b2d3fee3814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162387572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a0fae1e3e393bd81064a5a47039c9fec27a2f77c8be95795a3dc1466ad81ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0519160658aa38aa8ec1a9223db51f24ef66cec37c87e5d3252a5b1636bf481`  
		Last Modified: Tue, 14 Jan 2025 07:23:55 GMT  
		Size: 9.6 MB (9587362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a8b4761500ec9c11b5fdbefce98c329f2d5853652b2434b1f174b192974be0`  
		Last Modified: Tue, 14 Jan 2025 07:23:54 GMT  
		Size: 5.5 MB (5463786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6470a1080b2858907cf5c6754c4f40e5a95cd979fd29fff60cfdbb7ebb55dee1`  
		Last Modified: Tue, 14 Jan 2025 07:23:54 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fcbe061689e52b7c5b7929a1aceb8ec5d535130bed1d5acffbfdc7eff569dd`  
		Last Modified: Tue, 14 Jan 2025 07:23:54 GMT  
		Size: 936.1 KB (936104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6484dfd2b5865354d6aee22d73005c5ab86111bbdfd94d57c132d963b06c3`  
		Last Modified: Tue, 14 Jan 2025 07:23:58 GMT  
		Size: 96.2 MB (96151392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45f168297634a1e2c074e189b69dc1ab2be83fec68ef455e38b51176c537c66`  
		Last Modified: Tue, 14 Jan 2025 07:23:56 GMT  
		Size: 22.2 MB (22197942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0470c74fd97d622094d009fac154789ef2980d85506e607abc3cb8b6c8e8565`  
		Last Modified: Tue, 14 Jan 2025 20:36:12 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d253f731479a5ca137c2c54178b12c934a42e48ff4291854e0cd1c204d00ebb6`  
		Last Modified: Tue, 14 Jan 2025 20:36:18 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef753136aa92703545b2667815093321a19c5789fcd04c5dd4856dea68a6c057`  
		Last Modified: Tue, 14 Jan 2025 20:33:48 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:6009930905c9627c0d9d66b0c42932b69c39a1ba551d0b15f0b246302d5f769f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2881758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a094fa8745410e40423d0f9f4341a941cf34e40c450ca4468f7eb6d24fddbd`

```dockerfile
```

-	Layers:
	-	`sha256:20efc527a51d42a77be3f33e586725bb27964134cfe6f4e9426ee9b7d4758eec`  
		Last Modified: Tue, 14 Jan 2025 22:06:58 GMT  
		Size: 2.8 MB (2847855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a6b56548878df25c8f32a7dad31954a8b257013a5a225a66d2cfc4ceb9804e`  
		Last Modified: Wed, 15 Jan 2025 01:05:28 GMT  
		Size: 33.9 KB (33903 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:21e7caba25c83e7f05898f08b65e0cd843e7c5c3233a909574d3004e82d6a92a
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
		Last Modified: Tue, 14 Jan 2025 20:44:28 GMT  
		Size: 9.7 MB (9664086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eb104e3f0244f28d748ea2d7e74df268bfc91d976a040efdd8b6472e202934`  
		Last Modified: Tue, 14 Jan 2025 20:55:50 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:44:11 GMT  
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
		Last Modified: Wed, 15 Jan 2025 00:38:14 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:de8426562aae77d38978d64e05d0c3add2e8c49fff02eb6de6559b1d2ddeff21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89615883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5218ff2e3e43bebb55215894df96d326d54024bd5bedb8bcb3f695250ce6bee9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057a2e931604572012bfcfa32ff63d57c7e13b9484567fe86dea4678aa846576`  
		Last Modified: Wed, 08 Jan 2025 23:33:36 GMT  
		Size: 9.8 MB (9781847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40885a465df33fe6876f229a70e6e1f9d06f2e74a23dad03a739070e643f3f47`  
		Last Modified: Wed, 08 Jan 2025 23:33:35 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6593c403f08774a7b9b796fdb1f27730dde47c815cc79db25725134a0f0cb18`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0b8fa25bb2615a503c1807079fe1bac004ab1894073f1b4193761e7c27e328`  
		Last Modified: Wed, 08 Jan 2025 23:33:37 GMT  
		Size: 48.1 MB (48073560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eebc18de04e5c4e869da58da450854697b3a123aad83cbdc5544b062949fa0c`  
		Last Modified: Tue, 14 Jan 2025 22:07:40 GMT  
		Size: 22.2 MB (22197938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb157672269c8c03b1fd14c4ac2c6469970c7f7a51981c5ff08918c45c8d2aca`  
		Last Modified: Tue, 14 Jan 2025 21:02:02 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b407da3bbc26403fa957f2b202523c5fe99a199ef6a9bde6bca0e758d2541302`  
		Last Modified: Tue, 14 Jan 2025 23:45:16 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3edc6c59b2526c18e1658ce630e4c188730c211df9346aebc821c0028dbccbc`  
		Last Modified: Wed, 08 Jan 2025 23:33:37 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fe1bf94d7c78e453275d88beed4f073b9eb60f5f02d02da46e6a724ea40a9a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **947.6 KB (947598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d314bcb026bee756f637d82de95c5659a19518bb3c21816288760843eefa4802`

```dockerfile
```

-	Layers:
	-	`sha256:42ddaf62cf072af2e72f0e7652d389b1ab5c1436daec72fc92f10298ab02021a`  
		Last Modified: Wed, 15 Jan 2025 01:05:47 GMT  
		Size: 916.5 KB (916455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad1c5238ca3bbd3719b1a695f0d7b9de62192037bd8be847833ad60b6b375b6`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 31.1 KB (31143 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.11`

```console
$ docker pull influxdb@sha256:e9fc35b36536bfdeb3defe5a59c3a2e21465daea3902a577f0e5b752118a2e51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.11` - linux; amd64

```console
$ docker pull influxdb@sha256:6fb91c63e3e0106229d8cc9e6a437269bfd345bf2b6d4da4ce18b2ceed2eb293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168699095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762afe4bc6cf8930c1773cbf37dd6dd8af169093b56113bb60cdb51fca1c97b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab40758896b65a4bb3ecc6b0714efc0d4e173fd91a5f7b3ff93a25c5c0933e39`  
		Last Modified: Tue, 14 Jan 2025 02:34:36 GMT  
		Size: 9.8 MB (9790077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a38212e5b040080b41465e28d7fec7d8c3460bab9113cc22ccba62256d591e`  
		Last Modified: Tue, 14 Jan 2025 02:34:36 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d579e8989044770546dd3a4c57acae66413db8a1165bd38f03c1f8e5e8359e41`  
		Last Modified: Tue, 14 Jan 2025 02:34:35 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c53dd9bd71de0ae46e6bb0614682e00a57fef88b7ff18ac6b573bf80c4673d`  
		Last Modified: Tue, 14 Jan 2025 02:34:36 GMT  
		Size: 1.0 MB (1006368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a805a4428ab388207d8b9390ce109b35289509383eb313269128b291de2067fc`  
		Last Modified: Tue, 14 Jan 2025 02:34:38 GMT  
		Size: 100.3 MB (100312930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b94cb7724f533cdf21ec0c7c3bddadd853fbee31f2228bf59187adfebc411a`  
		Last Modified: Tue, 14 Jan 2025 02:34:37 GMT  
		Size: 23.5 MB (23546410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12b7823fa53078a98ebd2bf76a476558a236bb4b29471cffcdfc8d7358f9da8`  
		Last Modified: Tue, 14 Jan 2025 20:33:12 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f44532ba7abe4af6ee25a1d9f6f7af98640a98f144f23df14a06bd2b32d6b7`  
		Last Modified: Tue, 14 Jan 2025 02:34:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20762f0e055147938113d79964ba71d000b9d5db7d726df9bb046433b3fc167`  
		Last Modified: Tue, 14 Jan 2025 20:33:20 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:eeda7fdc817783ae62c9ab8296274e5be37e96828b3c9d24aaf3eecdebd153d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e06a90a1d26723c375027f886c402833ab03e6cfadbab9a178e9ef6aefd8fa`

```dockerfile
```

-	Layers:
	-	`sha256:ab07f397ef4ff3ca4bd09847db03b5be8dff55b56d1bfcc7775a6fea9023fd6d`  
		Last Modified: Tue, 14 Jan 2025 22:04:34 GMT  
		Size: 2.8 MB (2848627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccdf399dde11679520acf0d1e70bdc544cee80f0cca0270bf0f45064434bf945`  
		Last Modified: Tue, 14 Jan 2025 22:04:36 GMT  
		Size: 33.7 KB (33719 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4f674ba91d974cc8fd9fca55df891e89b9fc4ed70589ae274a876b2d3fee3814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162387572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a0fae1e3e393bd81064a5a47039c9fec27a2f77c8be95795a3dc1466ad81ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0519160658aa38aa8ec1a9223db51f24ef66cec37c87e5d3252a5b1636bf481`  
		Last Modified: Tue, 14 Jan 2025 07:23:55 GMT  
		Size: 9.6 MB (9587362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a8b4761500ec9c11b5fdbefce98c329f2d5853652b2434b1f174b192974be0`  
		Last Modified: Tue, 14 Jan 2025 07:23:54 GMT  
		Size: 5.5 MB (5463786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6470a1080b2858907cf5c6754c4f40e5a95cd979fd29fff60cfdbb7ebb55dee1`  
		Last Modified: Tue, 14 Jan 2025 07:23:54 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fcbe061689e52b7c5b7929a1aceb8ec5d535130bed1d5acffbfdc7eff569dd`  
		Last Modified: Tue, 14 Jan 2025 07:23:54 GMT  
		Size: 936.1 KB (936104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6484dfd2b5865354d6aee22d73005c5ab86111bbdfd94d57c132d963b06c3`  
		Last Modified: Tue, 14 Jan 2025 07:23:58 GMT  
		Size: 96.2 MB (96151392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45f168297634a1e2c074e189b69dc1ab2be83fec68ef455e38b51176c537c66`  
		Last Modified: Tue, 14 Jan 2025 07:23:56 GMT  
		Size: 22.2 MB (22197942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0470c74fd97d622094d009fac154789ef2980d85506e607abc3cb8b6c8e8565`  
		Last Modified: Tue, 14 Jan 2025 20:36:12 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d253f731479a5ca137c2c54178b12c934a42e48ff4291854e0cd1c204d00ebb6`  
		Last Modified: Tue, 14 Jan 2025 20:36:18 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef753136aa92703545b2667815093321a19c5789fcd04c5dd4856dea68a6c057`  
		Last Modified: Tue, 14 Jan 2025 20:33:48 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:6009930905c9627c0d9d66b0c42932b69c39a1ba551d0b15f0b246302d5f769f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2881758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a094fa8745410e40423d0f9f4341a941cf34e40c450ca4468f7eb6d24fddbd`

```dockerfile
```

-	Layers:
	-	`sha256:20efc527a51d42a77be3f33e586725bb27964134cfe6f4e9426ee9b7d4758eec`  
		Last Modified: Tue, 14 Jan 2025 22:06:58 GMT  
		Size: 2.8 MB (2847855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a6b56548878df25c8f32a7dad31954a8b257013a5a225a66d2cfc4ceb9804e`  
		Last Modified: Wed, 15 Jan 2025 01:05:28 GMT  
		Size: 33.9 KB (33903 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.11-alpine`

```console
$ docker pull influxdb@sha256:21e7caba25c83e7f05898f08b65e0cd843e7c5c3233a909574d3004e82d6a92a
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
		Last Modified: Tue, 14 Jan 2025 20:44:28 GMT  
		Size: 9.7 MB (9664086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eb104e3f0244f28d748ea2d7e74df268bfc91d976a040efdd8b6472e202934`  
		Last Modified: Tue, 14 Jan 2025 20:55:50 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:44:11 GMT  
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
		Last Modified: Wed, 15 Jan 2025 00:38:14 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:de8426562aae77d38978d64e05d0c3add2e8c49fff02eb6de6559b1d2ddeff21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89615883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5218ff2e3e43bebb55215894df96d326d54024bd5bedb8bcb3f695250ce6bee9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057a2e931604572012bfcfa32ff63d57c7e13b9484567fe86dea4678aa846576`  
		Last Modified: Wed, 08 Jan 2025 23:33:36 GMT  
		Size: 9.8 MB (9781847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40885a465df33fe6876f229a70e6e1f9d06f2e74a23dad03a739070e643f3f47`  
		Last Modified: Wed, 08 Jan 2025 23:33:35 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6593c403f08774a7b9b796fdb1f27730dde47c815cc79db25725134a0f0cb18`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0b8fa25bb2615a503c1807079fe1bac004ab1894073f1b4193761e7c27e328`  
		Last Modified: Wed, 08 Jan 2025 23:33:37 GMT  
		Size: 48.1 MB (48073560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eebc18de04e5c4e869da58da450854697b3a123aad83cbdc5544b062949fa0c`  
		Last Modified: Tue, 14 Jan 2025 22:07:40 GMT  
		Size: 22.2 MB (22197938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb157672269c8c03b1fd14c4ac2c6469970c7f7a51981c5ff08918c45c8d2aca`  
		Last Modified: Tue, 14 Jan 2025 21:02:02 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b407da3bbc26403fa957f2b202523c5fe99a199ef6a9bde6bca0e758d2541302`  
		Last Modified: Tue, 14 Jan 2025 23:45:16 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3edc6c59b2526c18e1658ce630e4c188730c211df9346aebc821c0028dbccbc`  
		Last Modified: Wed, 08 Jan 2025 23:33:37 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fe1bf94d7c78e453275d88beed4f073b9eb60f5f02d02da46e6a724ea40a9a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **947.6 KB (947598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d314bcb026bee756f637d82de95c5659a19518bb3c21816288760843eefa4802`

```dockerfile
```

-	Layers:
	-	`sha256:42ddaf62cf072af2e72f0e7652d389b1ab5c1436daec72fc92f10298ab02021a`  
		Last Modified: Wed, 15 Jan 2025 01:05:47 GMT  
		Size: 916.5 KB (916455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad1c5238ca3bbd3719b1a695f0d7b9de62192037bd8be847833ad60b6b375b6`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 31.1 KB (31143 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:21e7caba25c83e7f05898f08b65e0cd843e7c5c3233a909574d3004e82d6a92a
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
		Last Modified: Tue, 14 Jan 2025 20:44:28 GMT  
		Size: 9.7 MB (9664086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eb104e3f0244f28d748ea2d7e74df268bfc91d976a040efdd8b6472e202934`  
		Last Modified: Tue, 14 Jan 2025 20:55:50 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:44:11 GMT  
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
		Last Modified: Wed, 15 Jan 2025 00:38:14 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:de8426562aae77d38978d64e05d0c3add2e8c49fff02eb6de6559b1d2ddeff21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89615883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5218ff2e3e43bebb55215894df96d326d54024bd5bedb8bcb3f695250ce6bee9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5c7dafdb703875c4326b5e1c619a600f0cc7fe2b730986902401f7db9071f7`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057a2e931604572012bfcfa32ff63d57c7e13b9484567fe86dea4678aa846576`  
		Last Modified: Wed, 08 Jan 2025 23:33:36 GMT  
		Size: 9.8 MB (9781847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40885a465df33fe6876f229a70e6e1f9d06f2e74a23dad03a739070e643f3f47`  
		Last Modified: Wed, 08 Jan 2025 23:33:35 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6593c403f08774a7b9b796fdb1f27730dde47c815cc79db25725134a0f0cb18`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0b8fa25bb2615a503c1807079fe1bac004ab1894073f1b4193761e7c27e328`  
		Last Modified: Wed, 08 Jan 2025 23:33:37 GMT  
		Size: 48.1 MB (48073560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eebc18de04e5c4e869da58da450854697b3a123aad83cbdc5544b062949fa0c`  
		Last Modified: Tue, 14 Jan 2025 22:07:40 GMT  
		Size: 22.2 MB (22197938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb157672269c8c03b1fd14c4ac2c6469970c7f7a51981c5ff08918c45c8d2aca`  
		Last Modified: Tue, 14 Jan 2025 21:02:02 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b407da3bbc26403fa957f2b202523c5fe99a199ef6a9bde6bca0e758d2541302`  
		Last Modified: Tue, 14 Jan 2025 23:45:16 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3edc6c59b2526c18e1658ce630e4c188730c211df9346aebc821c0028dbccbc`  
		Last Modified: Wed, 08 Jan 2025 23:33:37 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fe1bf94d7c78e453275d88beed4f073b9eb60f5f02d02da46e6a724ea40a9a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **947.6 KB (947598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d314bcb026bee756f637d82de95c5659a19518bb3c21816288760843eefa4802`

```dockerfile
```

-	Layers:
	-	`sha256:42ddaf62cf072af2e72f0e7652d389b1ab5c1436daec72fc92f10298ab02021a`  
		Last Modified: Wed, 15 Jan 2025 01:05:47 GMT  
		Size: 916.5 KB (916455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad1c5238ca3bbd3719b1a695f0d7b9de62192037bd8be847833ad60b6b375b6`  
		Last Modified: Wed, 08 Jan 2025 23:33:34 GMT  
		Size: 31.1 KB (31143 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:e9fc35b36536bfdeb3defe5a59c3a2e21465daea3902a577f0e5b752118a2e51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:6fb91c63e3e0106229d8cc9e6a437269bfd345bf2b6d4da4ce18b2ceed2eb293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168699095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762afe4bc6cf8930c1773cbf37dd6dd8af169093b56113bb60cdb51fca1c97b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab40758896b65a4bb3ecc6b0714efc0d4e173fd91a5f7b3ff93a25c5c0933e39`  
		Last Modified: Tue, 14 Jan 2025 02:34:36 GMT  
		Size: 9.8 MB (9790077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a38212e5b040080b41465e28d7fec7d8c3460bab9113cc22ccba62256d591e`  
		Last Modified: Tue, 14 Jan 2025 02:34:36 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d579e8989044770546dd3a4c57acae66413db8a1165bd38f03c1f8e5e8359e41`  
		Last Modified: Tue, 14 Jan 2025 02:34:35 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c53dd9bd71de0ae46e6bb0614682e00a57fef88b7ff18ac6b573bf80c4673d`  
		Last Modified: Tue, 14 Jan 2025 02:34:36 GMT  
		Size: 1.0 MB (1006368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a805a4428ab388207d8b9390ce109b35289509383eb313269128b291de2067fc`  
		Last Modified: Tue, 14 Jan 2025 02:34:38 GMT  
		Size: 100.3 MB (100312930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b94cb7724f533cdf21ec0c7c3bddadd853fbee31f2228bf59187adfebc411a`  
		Last Modified: Tue, 14 Jan 2025 02:34:37 GMT  
		Size: 23.5 MB (23546410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12b7823fa53078a98ebd2bf76a476558a236bb4b29471cffcdfc8d7358f9da8`  
		Last Modified: Tue, 14 Jan 2025 20:33:12 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f44532ba7abe4af6ee25a1d9f6f7af98640a98f144f23df14a06bd2b32d6b7`  
		Last Modified: Tue, 14 Jan 2025 02:34:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20762f0e055147938113d79964ba71d000b9d5db7d726df9bb046433b3fc167`  
		Last Modified: Tue, 14 Jan 2025 20:33:20 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:eeda7fdc817783ae62c9ab8296274e5be37e96828b3c9d24aaf3eecdebd153d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e06a90a1d26723c375027f886c402833ab03e6cfadbab9a178e9ef6aefd8fa`

```dockerfile
```

-	Layers:
	-	`sha256:ab07f397ef4ff3ca4bd09847db03b5be8dff55b56d1bfcc7775a6fea9023fd6d`  
		Last Modified: Tue, 14 Jan 2025 22:04:34 GMT  
		Size: 2.8 MB (2848627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccdf399dde11679520acf0d1e70bdc544cee80f0cca0270bf0f45064434bf945`  
		Last Modified: Tue, 14 Jan 2025 22:04:36 GMT  
		Size: 33.7 KB (33719 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4f674ba91d974cc8fd9fca55df891e89b9fc4ed70589ae274a876b2d3fee3814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162387572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a0fae1e3e393bd81064a5a47039c9fec27a2f77c8be95795a3dc1466ad81ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0519160658aa38aa8ec1a9223db51f24ef66cec37c87e5d3252a5b1636bf481`  
		Last Modified: Tue, 14 Jan 2025 07:23:55 GMT  
		Size: 9.6 MB (9587362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a8b4761500ec9c11b5fdbefce98c329f2d5853652b2434b1f174b192974be0`  
		Last Modified: Tue, 14 Jan 2025 07:23:54 GMT  
		Size: 5.5 MB (5463786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6470a1080b2858907cf5c6754c4f40e5a95cd979fd29fff60cfdbb7ebb55dee1`  
		Last Modified: Tue, 14 Jan 2025 07:23:54 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fcbe061689e52b7c5b7929a1aceb8ec5d535130bed1d5acffbfdc7eff569dd`  
		Last Modified: Tue, 14 Jan 2025 07:23:54 GMT  
		Size: 936.1 KB (936104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6484dfd2b5865354d6aee22d73005c5ab86111bbdfd94d57c132d963b06c3`  
		Last Modified: Tue, 14 Jan 2025 07:23:58 GMT  
		Size: 96.2 MB (96151392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45f168297634a1e2c074e189b69dc1ab2be83fec68ef455e38b51176c537c66`  
		Last Modified: Tue, 14 Jan 2025 07:23:56 GMT  
		Size: 22.2 MB (22197942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0470c74fd97d622094d009fac154789ef2980d85506e607abc3cb8b6c8e8565`  
		Last Modified: Tue, 14 Jan 2025 20:36:12 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d253f731479a5ca137c2c54178b12c934a42e48ff4291854e0cd1c204d00ebb6`  
		Last Modified: Tue, 14 Jan 2025 20:36:18 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef753136aa92703545b2667815093321a19c5789fcd04c5dd4856dea68a6c057`  
		Last Modified: Tue, 14 Jan 2025 20:33:48 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:6009930905c9627c0d9d66b0c42932b69c39a1ba551d0b15f0b246302d5f769f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2881758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a094fa8745410e40423d0f9f4341a941cf34e40c450ca4468f7eb6d24fddbd`

```dockerfile
```

-	Layers:
	-	`sha256:20efc527a51d42a77be3f33e586725bb27964134cfe6f4e9426ee9b7d4758eec`  
		Last Modified: Tue, 14 Jan 2025 22:06:58 GMT  
		Size: 2.8 MB (2847855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a6b56548878df25c8f32a7dad31954a8b257013a5a225a66d2cfc4ceb9804e`  
		Last Modified: Wed, 15 Jan 2025 01:05:28 GMT  
		Size: 33.9 KB (33903 bytes)  
		MIME: application/vnd.in-toto+json
