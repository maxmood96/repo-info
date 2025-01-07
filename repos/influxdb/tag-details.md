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
$ docker pull influxdb@sha256:14a5ee7fb0ec07e974217f2f100878ee4e14cf2d7c4e97d179416741cbea4d30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:050c9031fc0431c0dcb8a5a224ab1659f7dd9e40c145d54b91a6288b29f904de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46152240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a041b06152a1c4594a7daf3388813dc02113bacee90359cc8c6c522d869861`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b373194a57402c5b4bba439c0debcc21e50640ca97e8399e26f0876569f14`  
		Last Modified: Tue, 07 Jan 2025 03:32:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa00f9176a652d4d47d66e698dc397ceca638a0535dae8472fb11874ac88e6b`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 1.2 MB (1213446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc177f948be6d7194a170280fc2a1c89bebe49db2d88a0326f4db678ab59407d`  
		Last Modified: Tue, 07 Jan 2025 03:33:00 GMT  
		Size: 41.3 MB (41322745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497c9a6668dbdd6d965ef4273aad18197c69193053bbef099764f57c79cde50e`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334b9287c34456e0fe147fedd17c5e60e360c6fe8529f6b15879721b8e48904e`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647d82685157d5446f4e5d6b91ff9cc9d80e1af073f29f030c5fac374b3c46e5`  
		Last Modified: Tue, 07 Jan 2025 03:33:00 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e525058f8e3a90cc3af09ee74d13ac330fd6ee2369fa45fb85979d448f0ea491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.4 KB (766392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38faf7e2edaa4494d0927d10d5002071c48290b2925edb09705ac785b3a0df8`

```dockerfile
```

-	Layers:
	-	`sha256:b40aa0b31a23694074ee01d056282400ab9d20e63cfc04d56320a4fe4d62362f`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 749.8 KB (749753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530756f1e28a2f0469b0344380496c27fff87a7d38fe4b40ea396e0f66c18193`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
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
$ docker pull influxdb@sha256:afcced27f35cd11afbea23e2bcac1e46fe8caf1ad5fcd77baae4f708505f951f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5e9260bec65e73ba644405cb36c57b8ae986bd09dcb6126e92cdaf96a07f41c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24870255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2ef675945660157dedadb7497d966d39ab58de34d2b83a04d422a991465ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58662015e7c4b8ba5d70bc4c320f14db4f1aac5e30e3e67b5f1c176ee91c367a`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dca27dfa583a091bc23c912f83a1e8b9702a35dfe350822c720b92941931d46`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 1.2 MB (1213455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315df537cb63d80dfb2dd6da6f6d994888611054b2864aa3c1d96d201ec3147d`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 20.0 MB (20041958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b518599c847b9abec9a6b4859ab6eee9ec841a9b37783c58e14e08684e0cd352`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dbe0aa5fcc34b2a642d1d23dcff86622c95f8768a997a01e90932246721fec`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:506f25aec694f3db03bae71da574ac4c2a5d7af58db1427a302d14237ade2cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.6 KB (688647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dbbbeadd30bbed63ccce46faad4032526aa8c5c1c452ff76cb2c1a7ef342afa`

```dockerfile
```

-	Layers:
	-	`sha256:7b88ee96e32e681fd8ecc733c1caa3c4c2661ce2ff911aaf32acdf37859e6d98`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 673.6 KB (673637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd1f66be5e19566522021db5b9f18c2d707de86c0e9af6ecd2d6713e95d3cdcf`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 15.0 KB (15010 bytes)  
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
$ docker pull influxdb@sha256:14a5ee7fb0ec07e974217f2f100878ee4e14cf2d7c4e97d179416741cbea4d30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:050c9031fc0431c0dcb8a5a224ab1659f7dd9e40c145d54b91a6288b29f904de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46152240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a041b06152a1c4594a7daf3388813dc02113bacee90359cc8c6c522d869861`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b373194a57402c5b4bba439c0debcc21e50640ca97e8399e26f0876569f14`  
		Last Modified: Tue, 07 Jan 2025 03:32:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa00f9176a652d4d47d66e698dc397ceca638a0535dae8472fb11874ac88e6b`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 1.2 MB (1213446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc177f948be6d7194a170280fc2a1c89bebe49db2d88a0326f4db678ab59407d`  
		Last Modified: Tue, 07 Jan 2025 03:33:00 GMT  
		Size: 41.3 MB (41322745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497c9a6668dbdd6d965ef4273aad18197c69193053bbef099764f57c79cde50e`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334b9287c34456e0fe147fedd17c5e60e360c6fe8529f6b15879721b8e48904e`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647d82685157d5446f4e5d6b91ff9cc9d80e1af073f29f030c5fac374b3c46e5`  
		Last Modified: Tue, 07 Jan 2025 03:33:00 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e525058f8e3a90cc3af09ee74d13ac330fd6ee2369fa45fb85979d448f0ea491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.4 KB (766392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38faf7e2edaa4494d0927d10d5002071c48290b2925edb09705ac785b3a0df8`

```dockerfile
```

-	Layers:
	-	`sha256:b40aa0b31a23694074ee01d056282400ab9d20e63cfc04d56320a4fe4d62362f`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 749.8 KB (749753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530756f1e28a2f0469b0344380496c27fff87a7d38fe4b40ea396e0f66c18193`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
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
$ docker pull influxdb@sha256:afcced27f35cd11afbea23e2bcac1e46fe8caf1ad5fcd77baae4f708505f951f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5e9260bec65e73ba644405cb36c57b8ae986bd09dcb6126e92cdaf96a07f41c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24870255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d2ef675945660157dedadb7497d966d39ab58de34d2b83a04d422a991465ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58662015e7c4b8ba5d70bc4c320f14db4f1aac5e30e3e67b5f1c176ee91c367a`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dca27dfa583a091bc23c912f83a1e8b9702a35dfe350822c720b92941931d46`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 1.2 MB (1213455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315df537cb63d80dfb2dd6da6f6d994888611054b2864aa3c1d96d201ec3147d`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 20.0 MB (20041958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b518599c847b9abec9a6b4859ab6eee9ec841a9b37783c58e14e08684e0cd352`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dbe0aa5fcc34b2a642d1d23dcff86622c95f8768a997a01e90932246721fec`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:506f25aec694f3db03bae71da574ac4c2a5d7af58db1427a302d14237ade2cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.6 KB (688647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dbbbeadd30bbed63ccce46faad4032526aa8c5c1c452ff76cb2c1a7ef342afa`

```dockerfile
```

-	Layers:
	-	`sha256:7b88ee96e32e681fd8ecc733c1caa3c4c2661ce2ff911aaf32acdf37859e6d98`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 673.6 KB (673637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd1f66be5e19566522021db5b9f18c2d707de86c0e9af6ecd2d6713e95d3cdcf`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 15.0 KB (15010 bytes)  
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
$ docker pull influxdb@sha256:96b31a22619e4cab8c125805ec7676ea61a95266a09de26c89d70020b9e2a631
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:dcd93cd7c3cddc63894db97f4df105869e447c2a694fb5a0a8922f1277e2e384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42898558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bd2570b3f3b798e092f0cd6a74e26e59411f53567432ff0b053d73338af394`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb704351a02cd9d4303f258ff21789db32f07c4d6d7d621b5c53470c53e178`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 1.2 MB (1213463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429d2f618e577c1b047fd60a4fe68c720c6872e716d601fb2ceecb667ae87f8f`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 38.1 MB (38068379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b05ffe315071a4e4104dd8143002d48c058c6145eec17c24eccc8e6676b30e3`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c783ab64781eedc4e5fce921dc9e86874a3732177012134c14e0056a6306dc6f`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 1.0 KB (1004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4592e12cb47fe14a67bf91b17ba917afd375ff12489ccafdb63c2bfa33b26b26`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7577963557b1fd44906c9f91a26f9163efe0c9daa003f29da328cd4cf4109baf`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:afc3672a1e9fd123c45be974918221f81be718f4b10997db79a78014be87887c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **755.3 KB (755320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218d09af958536118eb0bcc5325b2677bc8f5f5a1d244894404209e7a29e5065`

```dockerfile
```

-	Layers:
	-	`sha256:4a92131becb7261773c0a9e05fb743db220d5946869e5d1e37e28e57d3b9a2c5`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 737.4 KB (737443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:617799194c8b1141eac025cd81db4e8b7da73ce2c0836a05d0bbdaa5e2d97483`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 17.9 KB (17877 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:190b720840638bfbd5d3c528cddbed4f95ad31246f2d44c36df5dca148a89125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40939034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b342a55f784f854f3da72a7affc16cff60b51dada18d6981ce25eb3a90efe947`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
USER influxdb
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f9fa33afbb704fe83e860e0ae0055706616de1db8054776ba772bbb2b6ef7f`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 1.3 MB (1303113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b92b2b4f217d6fc6583176acb74b3ba4831b3a7580a8e33232e4b8ecb1615a`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 35.5 MB (35545472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa8fbc7b8e59995519cb14a58f73ae8a2e8df346f77a21d1bf3e4e5ebdfdcff`  
		Last Modified: Wed, 20 Nov 2024 00:27:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579c4c0d23065d326e5fc90cca349de50739cf17e954c489ddb1421125a8a3b2`  
		Last Modified: Wed, 20 Nov 2024 00:27:59 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf86b4f1c9152aa4f4f503a509c56e1b5e0c97a96fc78c80c7d15661101b516`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f121dadcfa53fe0402bab5c0776c909f6768897033c8bbeceb45e729e9ae2a`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3d2e39c8ca4245a1e625ce8ef7279846d806d1b62eb5eb68a8b3c4392eadd596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da139cd58b5bdad8aa305c2e58a685f34b7ec1d76b9ef2f0ff834e62439b8103`

```dockerfile
```

-	Layers:
	-	`sha256:b42326533f84dfafe26ac54cd44920409aff668b578393dd883e14a3bdf05735`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 740.9 KB (740889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05e76b19d9a4e9ffc2575bb31d716bd95844acf2087db6ce50ca2c77f0c5efb`  
		Last Modified: Wed, 20 Nov 2024 00:27:59 GMT  
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
$ docker pull influxdb@sha256:d44a680d0d8e80497bde968bda045132fa1cee67239d71b027f410d3ac4958da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:64d040e46472c2d54b6cd23fd7bd5f986b233fd8df9393413712ccc782b40cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43953070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fde1c79bddef8edb690650a2901f777683c7bf7fbdb3c267210a6d27094852`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d339212a6ef1f140df0b8f4b7520097dd868ed1c0e25262c68c38ca11202aa`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbf87031e87bfe8c4bc8e29793ea4460b9edf0690a9ba8ced5d6d3a5716ea42`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 1.2 MB (1213476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0287c49b7ebdf6f47c524f49d5f8c4e100451ad64c9dd39004d2b013420de4`  
		Last Modified: Tue, 07 Jan 2025 03:32:44 GMT  
		Size: 39.1 MB (39123546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a13d1aebf94c43b05595ed4ac4b24e9aabcb44cce3ba1ee6773840ac5591b3`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc64e4497ac1701f6e9f527c576a7357941b2bd81b7010870c6fd3c1d15f4a5`  
		Last Modified: Tue, 07 Jan 2025 03:32:44 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03db88f4a8307e6cf6aa9553df6cd750a1102a4dfbbb604609b710a05ce2f22`  
		Last Modified: Tue, 07 Jan 2025 03:32:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:41b97a97be8eb0a422a98ecdbd95bfa377f5fb117d4ad045f139fa0a2507f6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.6 KB (764627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02fc6f5f4d8b6b958d2245129c79c8f9c9067c596d91868f41c32f341256a66`

```dockerfile
```

-	Layers:
	-	`sha256:f529b55dfc681f4b6d2a82136defc7c9c707c23225f53adf9523941923d3ff34`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 748.0 KB (747988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4db45725ec19fdca3f9a36e3ffe2ba871aa3ff516fb8e54ba5de980e989d79f`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 16.6 KB (16639 bytes)  
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
$ docker pull influxdb@sha256:8a47ca50986fcd6421c85821d21820c258ca28be0a50cba8286433ee0e14f550
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5ef4a377260d9d4f462687ebb29b601075549b85c3852934ca055eda91c1e0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23117943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7d98d97322798d99538d2a177d76fe5a61d795f2db639d1bae020801f058c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754219635225c96fd0291e9ebfdbb2246603bcdf9c9430d3c9c2e9f88b81fce8`  
		Last Modified: Tue, 07 Jan 2025 03:32:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12045141034464125a5f22efb6bc0dcc1fdbcd250caa19a935ec23f8052e46d`  
		Last Modified: Tue, 07 Jan 2025 03:32:50 GMT  
		Size: 1.2 MB (1213487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4439470706572cf1b8d24e68e870a77d6090bb54b0046a4b653a1c577ec767db`  
		Last Modified: Tue, 07 Jan 2025 03:32:51 GMT  
		Size: 18.3 MB (18289612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da607f898757d76b7f985bbe082047dfb32bacd8ccd84c6b9c890a3189ca3ed`  
		Last Modified: Tue, 07 Jan 2025 03:32:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941712713e8b877a24577a13e461506d839325d0ac9f743271505a4faadc0104`  
		Last Modified: Tue, 07 Jan 2025 03:32:51 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:1974078ba1a6c658d1bcf13adfa98c82fff93e9347bafee9684b24dcee9f8cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.5 KB (688502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d071e625f68f97a193ef65ff043faac5ed42c40f1f7e1775fd790950cb63349`

```dockerfile
```

-	Layers:
	-	`sha256:32a81299bc392bc0dc695bc77a869b6dc739af16f91525769916b3a5ffa4e028`  
		Last Modified: Tue, 07 Jan 2025 03:32:50 GMT  
		Size: 673.5 KB (673493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a182bfa0cb9859a40b7ae9ee402b849763e6d43c77b26f1763acbf127af3f495`  
		Last Modified: Tue, 07 Jan 2025 03:32:50 GMT  
		Size: 15.0 KB (15009 bytes)  
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
$ docker pull influxdb@sha256:96b31a22619e4cab8c125805ec7676ea61a95266a09de26c89d70020b9e2a631
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:dcd93cd7c3cddc63894db97f4df105869e447c2a694fb5a0a8922f1277e2e384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42898558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bd2570b3f3b798e092f0cd6a74e26e59411f53567432ff0b053d73338af394`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb704351a02cd9d4303f258ff21789db32f07c4d6d7d621b5c53470c53e178`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 1.2 MB (1213463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429d2f618e577c1b047fd60a4fe68c720c6872e716d601fb2ceecb667ae87f8f`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 38.1 MB (38068379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b05ffe315071a4e4104dd8143002d48c058c6145eec17c24eccc8e6676b30e3`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c783ab64781eedc4e5fce921dc9e86874a3732177012134c14e0056a6306dc6f`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 1.0 KB (1004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4592e12cb47fe14a67bf91b17ba917afd375ff12489ccafdb63c2bfa33b26b26`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7577963557b1fd44906c9f91a26f9163efe0c9daa003f29da328cd4cf4109baf`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:afc3672a1e9fd123c45be974918221f81be718f4b10997db79a78014be87887c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **755.3 KB (755320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218d09af958536118eb0bcc5325b2677bc8f5f5a1d244894404209e7a29e5065`

```dockerfile
```

-	Layers:
	-	`sha256:4a92131becb7261773c0a9e05fb743db220d5946869e5d1e37e28e57d3b9a2c5`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 737.4 KB (737443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:617799194c8b1141eac025cd81db4e8b7da73ce2c0836a05d0bbdaa5e2d97483`  
		Last Modified: Tue, 07 Jan 2025 03:32:41 GMT  
		Size: 17.9 KB (17877 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:190b720840638bfbd5d3c528cddbed4f95ad31246f2d44c36df5dca148a89125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40939034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b342a55f784f854f3da72a7affc16cff60b51dada18d6981ce25eb3a90efe947`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 Nov 2024 19:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 19 Nov 2024 19:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 19 Nov 2024 19:31:41 GMT
USER influxdb
# Tue, 19 Nov 2024 19:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Nov 2024 19:31:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f9fa33afbb704fe83e860e0ae0055706616de1db8054776ba772bbb2b6ef7f`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 1.3 MB (1303113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b92b2b4f217d6fc6583176acb74b3ba4831b3a7580a8e33232e4b8ecb1615a`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 35.5 MB (35545472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa8fbc7b8e59995519cb14a58f73ae8a2e8df346f77a21d1bf3e4e5ebdfdcff`  
		Last Modified: Wed, 20 Nov 2024 00:27:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579c4c0d23065d326e5fc90cca349de50739cf17e954c489ddb1421125a8a3b2`  
		Last Modified: Wed, 20 Nov 2024 00:27:59 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf86b4f1c9152aa4f4f503a509c56e1b5e0c97a96fc78c80c7d15661101b516`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f121dadcfa53fe0402bab5c0776c909f6768897033c8bbeceb45e729e9ae2a`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3d2e39c8ca4245a1e625ce8ef7279846d806d1b62eb5eb68a8b3c4392eadd596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da139cd58b5bdad8aa305c2e58a685f34b7ec1d76b9ef2f0ff834e62439b8103`

```dockerfile
```

-	Layers:
	-	`sha256:b42326533f84dfafe26ac54cd44920409aff668b578393dd883e14a3bdf05735`  
		Last Modified: Wed, 20 Nov 2024 00:28:00 GMT  
		Size: 740.9 KB (740889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05e76b19d9a4e9ffc2575bb31d716bd95844acf2087db6ce50ca2c77f0c5efb`  
		Last Modified: Wed, 20 Nov 2024 00:27:59 GMT  
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
$ docker pull influxdb@sha256:d44a680d0d8e80497bde968bda045132fa1cee67239d71b027f410d3ac4958da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:64d040e46472c2d54b6cd23fd7bd5f986b233fd8df9393413712ccc782b40cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43953070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fde1c79bddef8edb690650a2901f777683c7bf7fbdb3c267210a6d27094852`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d339212a6ef1f140df0b8f4b7520097dd868ed1c0e25262c68c38ca11202aa`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbf87031e87bfe8c4bc8e29793ea4460b9edf0690a9ba8ced5d6d3a5716ea42`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 1.2 MB (1213476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0287c49b7ebdf6f47c524f49d5f8c4e100451ad64c9dd39004d2b013420de4`  
		Last Modified: Tue, 07 Jan 2025 03:32:44 GMT  
		Size: 39.1 MB (39123546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a13d1aebf94c43b05595ed4ac4b24e9aabcb44cce3ba1ee6773840ac5591b3`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc64e4497ac1701f6e9f527c576a7357941b2bd81b7010870c6fd3c1d15f4a5`  
		Last Modified: Tue, 07 Jan 2025 03:32:44 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03db88f4a8307e6cf6aa9553df6cd750a1102a4dfbbb604609b710a05ce2f22`  
		Last Modified: Tue, 07 Jan 2025 03:32:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:41b97a97be8eb0a422a98ecdbd95bfa377f5fb117d4ad045f139fa0a2507f6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.6 KB (764627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02fc6f5f4d8b6b958d2245129c79c8f9c9067c596d91868f41c32f341256a66`

```dockerfile
```

-	Layers:
	-	`sha256:f529b55dfc681f4b6d2a82136defc7c9c707c23225f53adf9523941923d3ff34`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 748.0 KB (747988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4db45725ec19fdca3f9a36e3ffe2ba871aa3ff516fb8e54ba5de980e989d79f`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 16.6 KB (16639 bytes)  
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
$ docker pull influxdb@sha256:8a47ca50986fcd6421c85821d21820c258ca28be0a50cba8286433ee0e14f550
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5ef4a377260d9d4f462687ebb29b601075549b85c3852934ca055eda91c1e0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23117943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7d98d97322798d99538d2a177d76fe5a61d795f2db639d1bae020801f058c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754219635225c96fd0291e9ebfdbb2246603bcdf9c9430d3c9c2e9f88b81fce8`  
		Last Modified: Tue, 07 Jan 2025 03:32:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12045141034464125a5f22efb6bc0dcc1fdbcd250caa19a935ec23f8052e46d`  
		Last Modified: Tue, 07 Jan 2025 03:32:50 GMT  
		Size: 1.2 MB (1213487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4439470706572cf1b8d24e68e870a77d6090bb54b0046a4b653a1c577ec767db`  
		Last Modified: Tue, 07 Jan 2025 03:32:51 GMT  
		Size: 18.3 MB (18289612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da607f898757d76b7f985bbe082047dfb32bacd8ccd84c6b9c890a3189ca3ed`  
		Last Modified: Tue, 07 Jan 2025 03:32:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941712713e8b877a24577a13e461506d839325d0ac9f743271505a4faadc0104`  
		Last Modified: Tue, 07 Jan 2025 03:32:51 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:1974078ba1a6c658d1bcf13adfa98c82fff93e9347bafee9684b24dcee9f8cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.5 KB (688502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d071e625f68f97a193ef65ff043faac5ed42c40f1f7e1775fd790950cb63349`

```dockerfile
```

-	Layers:
	-	`sha256:32a81299bc392bc0dc695bc77a869b6dc739af16f91525769916b3a5ffa4e028`  
		Last Modified: Tue, 07 Jan 2025 03:32:50 GMT  
		Size: 673.5 KB (673493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a182bfa0cb9859a40b7ae9ee402b849763e6d43c77b26f1763acbf127af3f495`  
		Last Modified: Tue, 07 Jan 2025 03:32:50 GMT  
		Size: 15.0 KB (15009 bytes)  
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
$ docker pull influxdb@sha256:76ab0f67013c3f5e3fa3467b3db23024cbe4d50a33d7f16b3d5be7aa4ebd742d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:65cf1943c14ccab5d336d6b59415e7ad26cf4b6744ca6f00feb4741fec7f2307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92779944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21e08a2e38cb8824ac6b62ac292a2702ed94faca0c7219558e4374ea994b953`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b373194a57402c5b4bba439c0debcc21e50640ca97e8399e26f0876569f14`  
		Last Modified: Tue, 07 Jan 2025 03:32:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061a33113abb88563b3ca4a1cbbe9414e262161926b31684de0c0152272983bd`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 9.6 MB (9642320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1ffa749e13fdb6fc29c353eb66441610718728517e29f8289129d083eae3b5`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636417211ffa93e8d533b3f63da642d55948a9b18b80779626fc03f980552398`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc15dd98b0fcf10e85067250b6411a832ec7b4b1aebd1a9e955e77349cb2e877`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 50.1 MB (50148321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f415e6f58dcfffdfcf3a4122050b14136b5ac6d85de6fd64be9587702d812bef`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 23.5 MB (23546401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd9c206d494b31c8ba6b65c88780f4198a0544de1f537a0014107045ab92026`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a80fb26169c3e8bd145519b90eab71e5adddef5d17352afd92674f17c94697`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf3569fe526407b71dea95c5f31134f9c913733f02ece6afe8e7f7af76630e2`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c489832e97fed6a8c174c6fcee31df53712c9d88f30be71032ed393debbd4c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.3 KB (942275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbc4e25f36a7ca0482a7125b601a2d17dc65bc564bed684b7b9bf768fe9b61d`

```dockerfile
```

-	Layers:
	-	`sha256:2116dae99c98c083cc71c4f50984d41491a780e7dca92621741b895dc0dcabf1`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 911.3 KB (911326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fa68b5e9ec2aae472e56e53a0940569d6aff634c0cb972a3aa20e969c2ec067`  
		Last Modified: Tue, 07 Jan 2025 03:32:57 GMT  
		Size: 30.9 KB (30949 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bfbc2aa91de7e3c7264f9295620d8f603138bb97d1a53e83e7d2f4957f45db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89610878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95fbb8910695b56b3104ce76adf0bffd42f1cb3f697501b623e105027abf94c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2136f9e7feb99945e2787587daa3284c73e45adf2e22f99ad169fe2df7417c`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718d7af5f34af6fc2687e6c5cf198fdacb37225bdb375807fbe0ea44bbd6450`  
		Last Modified: Tue, 03 Dec 2024 00:31:59 GMT  
		Size: 9.8 MB (9779881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fcfab0657e0e0d9481ed7da1f556551043c7c82c74242566999e258d0907c1`  
		Last Modified: Tue, 03 Dec 2024 00:31:59 GMT  
		Size: 5.5 MB (5463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4f1051b394f46f3d3001f9461e1d64e65914ef5ed15d7fdc12b65aeccc9d4b`  
		Last Modified: Tue, 03 Dec 2024 00:31:58 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90bfa1e935dd0355d0fcfa331bb0eac10c1880b82f09ca72d859bf5df4426fd`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 48.1 MB (48073558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4733eb9ef3e5c6fc9d62bb6c6894099fd056ee3878c339fa4728ae3ca59bafe`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 22.2 MB (22197937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd02c14330814cce99a3419796480489d904ced932b14464355aadf124301d5`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff488ec6d0a178cd05f7a4cb4591794b6c695e9838ced285909949f7f86ec4f`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4782f397461732c414fb673e5db708b93a434f931f9ae03da8c02fb3566609`  
		Last Modified: Tue, 03 Dec 2024 00:32:01 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:73a6f66ab05daf238b1e993c8e11f3eb7653d9475415c87dd3b83d300c40bbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.0 KB (945027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19047d89c12d0dea39d11f969f4778a072493d770c25fc6e046f5783247ce5d1`

```dockerfile
```

-	Layers:
	-	`sha256:3530efeec1e6500c5a5d348f35a0c1df45a5e8eefe3caedf3d5b71b75746a58a`  
		Last Modified: Tue, 03 Dec 2024 00:31:59 GMT  
		Size: 913.9 KB (913884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3757c7a10e35f6eb48e918dacd06ec2a39035d8ca26c80e0043ebaa070045f`  
		Last Modified: Tue, 03 Dec 2024 00:31:58 GMT  
		Size: 31.1 KB (31143 bytes)  
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
$ docker pull influxdb@sha256:76ab0f67013c3f5e3fa3467b3db23024cbe4d50a33d7f16b3d5be7aa4ebd742d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:65cf1943c14ccab5d336d6b59415e7ad26cf4b6744ca6f00feb4741fec7f2307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92779944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21e08a2e38cb8824ac6b62ac292a2702ed94faca0c7219558e4374ea994b953`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b373194a57402c5b4bba439c0debcc21e50640ca97e8399e26f0876569f14`  
		Last Modified: Tue, 07 Jan 2025 03:32:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061a33113abb88563b3ca4a1cbbe9414e262161926b31684de0c0152272983bd`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 9.6 MB (9642320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1ffa749e13fdb6fc29c353eb66441610718728517e29f8289129d083eae3b5`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636417211ffa93e8d533b3f63da642d55948a9b18b80779626fc03f980552398`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc15dd98b0fcf10e85067250b6411a832ec7b4b1aebd1a9e955e77349cb2e877`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 50.1 MB (50148321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f415e6f58dcfffdfcf3a4122050b14136b5ac6d85de6fd64be9587702d812bef`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 23.5 MB (23546401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd9c206d494b31c8ba6b65c88780f4198a0544de1f537a0014107045ab92026`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a80fb26169c3e8bd145519b90eab71e5adddef5d17352afd92674f17c94697`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf3569fe526407b71dea95c5f31134f9c913733f02ece6afe8e7f7af76630e2`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c489832e97fed6a8c174c6fcee31df53712c9d88f30be71032ed393debbd4c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.3 KB (942275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbc4e25f36a7ca0482a7125b601a2d17dc65bc564bed684b7b9bf768fe9b61d`

```dockerfile
```

-	Layers:
	-	`sha256:2116dae99c98c083cc71c4f50984d41491a780e7dca92621741b895dc0dcabf1`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 911.3 KB (911326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fa68b5e9ec2aae472e56e53a0940569d6aff634c0cb972a3aa20e969c2ec067`  
		Last Modified: Tue, 07 Jan 2025 03:32:57 GMT  
		Size: 30.9 KB (30949 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bfbc2aa91de7e3c7264f9295620d8f603138bb97d1a53e83e7d2f4957f45db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89610878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95fbb8910695b56b3104ce76adf0bffd42f1cb3f697501b623e105027abf94c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2136f9e7feb99945e2787587daa3284c73e45adf2e22f99ad169fe2df7417c`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718d7af5f34af6fc2687e6c5cf198fdacb37225bdb375807fbe0ea44bbd6450`  
		Last Modified: Tue, 03 Dec 2024 00:31:59 GMT  
		Size: 9.8 MB (9779881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fcfab0657e0e0d9481ed7da1f556551043c7c82c74242566999e258d0907c1`  
		Last Modified: Tue, 03 Dec 2024 00:31:59 GMT  
		Size: 5.5 MB (5463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4f1051b394f46f3d3001f9461e1d64e65914ef5ed15d7fdc12b65aeccc9d4b`  
		Last Modified: Tue, 03 Dec 2024 00:31:58 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90bfa1e935dd0355d0fcfa331bb0eac10c1880b82f09ca72d859bf5df4426fd`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 48.1 MB (48073558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4733eb9ef3e5c6fc9d62bb6c6894099fd056ee3878c339fa4728ae3ca59bafe`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 22.2 MB (22197937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd02c14330814cce99a3419796480489d904ced932b14464355aadf124301d5`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff488ec6d0a178cd05f7a4cb4591794b6c695e9838ced285909949f7f86ec4f`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4782f397461732c414fb673e5db708b93a434f931f9ae03da8c02fb3566609`  
		Last Modified: Tue, 03 Dec 2024 00:32:01 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:73a6f66ab05daf238b1e993c8e11f3eb7653d9475415c87dd3b83d300c40bbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.0 KB (945027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19047d89c12d0dea39d11f969f4778a072493d770c25fc6e046f5783247ce5d1`

```dockerfile
```

-	Layers:
	-	`sha256:3530efeec1e6500c5a5d348f35a0c1df45a5e8eefe3caedf3d5b71b75746a58a`  
		Last Modified: Tue, 03 Dec 2024 00:31:59 GMT  
		Size: 913.9 KB (913884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3757c7a10e35f6eb48e918dacd06ec2a39035d8ca26c80e0043ebaa070045f`  
		Last Modified: Tue, 03 Dec 2024 00:31:58 GMT  
		Size: 31.1 KB (31143 bytes)  
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
$ docker pull influxdb@sha256:76ab0f67013c3f5e3fa3467b3db23024cbe4d50a33d7f16b3d5be7aa4ebd742d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:65cf1943c14ccab5d336d6b59415e7ad26cf4b6744ca6f00feb4741fec7f2307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92779944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21e08a2e38cb8824ac6b62ac292a2702ed94faca0c7219558e4374ea994b953`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b373194a57402c5b4bba439c0debcc21e50640ca97e8399e26f0876569f14`  
		Last Modified: Tue, 07 Jan 2025 03:32:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061a33113abb88563b3ca4a1cbbe9414e262161926b31684de0c0152272983bd`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 9.6 MB (9642320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1ffa749e13fdb6fc29c353eb66441610718728517e29f8289129d083eae3b5`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636417211ffa93e8d533b3f63da642d55948a9b18b80779626fc03f980552398`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc15dd98b0fcf10e85067250b6411a832ec7b4b1aebd1a9e955e77349cb2e877`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 50.1 MB (50148321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f415e6f58dcfffdfcf3a4122050b14136b5ac6d85de6fd64be9587702d812bef`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 23.5 MB (23546401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd9c206d494b31c8ba6b65c88780f4198a0544de1f537a0014107045ab92026`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a80fb26169c3e8bd145519b90eab71e5adddef5d17352afd92674f17c94697`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf3569fe526407b71dea95c5f31134f9c913733f02ece6afe8e7f7af76630e2`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c489832e97fed6a8c174c6fcee31df53712c9d88f30be71032ed393debbd4c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.3 KB (942275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbc4e25f36a7ca0482a7125b601a2d17dc65bc564bed684b7b9bf768fe9b61d`

```dockerfile
```

-	Layers:
	-	`sha256:2116dae99c98c083cc71c4f50984d41491a780e7dca92621741b895dc0dcabf1`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 911.3 KB (911326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fa68b5e9ec2aae472e56e53a0940569d6aff634c0cb972a3aa20e969c2ec067`  
		Last Modified: Tue, 07 Jan 2025 03:32:57 GMT  
		Size: 30.9 KB (30949 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bfbc2aa91de7e3c7264f9295620d8f603138bb97d1a53e83e7d2f4957f45db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89610878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95fbb8910695b56b3104ce76adf0bffd42f1cb3f697501b623e105027abf94c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2136f9e7feb99945e2787587daa3284c73e45adf2e22f99ad169fe2df7417c`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718d7af5f34af6fc2687e6c5cf198fdacb37225bdb375807fbe0ea44bbd6450`  
		Last Modified: Tue, 03 Dec 2024 00:31:59 GMT  
		Size: 9.8 MB (9779881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fcfab0657e0e0d9481ed7da1f556551043c7c82c74242566999e258d0907c1`  
		Last Modified: Tue, 03 Dec 2024 00:31:59 GMT  
		Size: 5.5 MB (5463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4f1051b394f46f3d3001f9461e1d64e65914ef5ed15d7fdc12b65aeccc9d4b`  
		Last Modified: Tue, 03 Dec 2024 00:31:58 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90bfa1e935dd0355d0fcfa331bb0eac10c1880b82f09ca72d859bf5df4426fd`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 48.1 MB (48073558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4733eb9ef3e5c6fc9d62bb6c6894099fd056ee3878c339fa4728ae3ca59bafe`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 22.2 MB (22197937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd02c14330814cce99a3419796480489d904ced932b14464355aadf124301d5`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff488ec6d0a178cd05f7a4cb4591794b6c695e9838ced285909949f7f86ec4f`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4782f397461732c414fb673e5db708b93a434f931f9ae03da8c02fb3566609`  
		Last Modified: Tue, 03 Dec 2024 00:32:01 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:73a6f66ab05daf238b1e993c8e11f3eb7653d9475415c87dd3b83d300c40bbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.0 KB (945027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19047d89c12d0dea39d11f969f4778a072493d770c25fc6e046f5783247ce5d1`

```dockerfile
```

-	Layers:
	-	`sha256:3530efeec1e6500c5a5d348f35a0c1df45a5e8eefe3caedf3d5b71b75746a58a`  
		Last Modified: Tue, 03 Dec 2024 00:31:59 GMT  
		Size: 913.9 KB (913884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3757c7a10e35f6eb48e918dacd06ec2a39035d8ca26c80e0043ebaa070045f`  
		Last Modified: Tue, 03 Dec 2024 00:31:58 GMT  
		Size: 31.1 KB (31143 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:76ab0f67013c3f5e3fa3467b3db23024cbe4d50a33d7f16b3d5be7aa4ebd742d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:65cf1943c14ccab5d336d6b59415e7ad26cf4b6744ca6f00feb4741fec7f2307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92779944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21e08a2e38cb8824ac6b62ac292a2702ed94faca0c7219558e4374ea994b953`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2b373194a57402c5b4bba439c0debcc21e50640ca97e8399e26f0876569f14`  
		Last Modified: Tue, 07 Jan 2025 03:32:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061a33113abb88563b3ca4a1cbbe9414e262161926b31684de0c0152272983bd`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 9.6 MB (9642320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1ffa749e13fdb6fc29c353eb66441610718728517e29f8289129d083eae3b5`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636417211ffa93e8d533b3f63da642d55948a9b18b80779626fc03f980552398`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc15dd98b0fcf10e85067250b6411a832ec7b4b1aebd1a9e955e77349cb2e877`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 50.1 MB (50148321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f415e6f58dcfffdfcf3a4122050b14136b5ac6d85de6fd64be9587702d812bef`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 23.5 MB (23546401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd9c206d494b31c8ba6b65c88780f4198a0544de1f537a0014107045ab92026`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a80fb26169c3e8bd145519b90eab71e5adddef5d17352afd92674f17c94697`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf3569fe526407b71dea95c5f31134f9c913733f02ece6afe8e7f7af76630e2`  
		Last Modified: Tue, 07 Jan 2025 03:32:59 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c489832e97fed6a8c174c6fcee31df53712c9d88f30be71032ed393debbd4c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.3 KB (942275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbc4e25f36a7ca0482a7125b601a2d17dc65bc564bed684b7b9bf768fe9b61d`

```dockerfile
```

-	Layers:
	-	`sha256:2116dae99c98c083cc71c4f50984d41491a780e7dca92621741b895dc0dcabf1`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 911.3 KB (911326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fa68b5e9ec2aae472e56e53a0940569d6aff634c0cb972a3aa20e969c2ec067`  
		Last Modified: Tue, 07 Jan 2025 03:32:57 GMT  
		Size: 30.9 KB (30949 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bfbc2aa91de7e3c7264f9295620d8f603138bb97d1a53e83e7d2f4957f45db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89610878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95fbb8910695b56b3104ce76adf0bffd42f1cb3f697501b623e105027abf94c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2136f9e7feb99945e2787587daa3284c73e45adf2e22f99ad169fe2df7417c`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718d7af5f34af6fc2687e6c5cf198fdacb37225bdb375807fbe0ea44bbd6450`  
		Last Modified: Tue, 03 Dec 2024 00:31:59 GMT  
		Size: 9.8 MB (9779881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fcfab0657e0e0d9481ed7da1f556551043c7c82c74242566999e258d0907c1`  
		Last Modified: Tue, 03 Dec 2024 00:31:59 GMT  
		Size: 5.5 MB (5463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4f1051b394f46f3d3001f9461e1d64e65914ef5ed15d7fdc12b65aeccc9d4b`  
		Last Modified: Tue, 03 Dec 2024 00:31:58 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90bfa1e935dd0355d0fcfa331bb0eac10c1880b82f09ca72d859bf5df4426fd`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 48.1 MB (48073558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4733eb9ef3e5c6fc9d62bb6c6894099fd056ee3878c339fa4728ae3ca59bafe`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 22.2 MB (22197937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd02c14330814cce99a3419796480489d904ced932b14464355aadf124301d5`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff488ec6d0a178cd05f7a4cb4591794b6c695e9838ced285909949f7f86ec4f`  
		Last Modified: Tue, 03 Dec 2024 00:32:00 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4782f397461732c414fb673e5db708b93a434f931f9ae03da8c02fb3566609`  
		Last Modified: Tue, 03 Dec 2024 00:32:01 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:73a6f66ab05daf238b1e993c8e11f3eb7653d9475415c87dd3b83d300c40bbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.0 KB (945027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19047d89c12d0dea39d11f969f4778a072493d770c25fc6e046f5783247ce5d1`

```dockerfile
```

-	Layers:
	-	`sha256:3530efeec1e6500c5a5d348f35a0c1df45a5e8eefe3caedf3d5b71b75746a58a`  
		Last Modified: Tue, 03 Dec 2024 00:31:59 GMT  
		Size: 913.9 KB (913884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3757c7a10e35f6eb48e918dacd06ec2a39035d8ca26c80e0043ebaa070045f`  
		Last Modified: Tue, 03 Dec 2024 00:31:58 GMT  
		Size: 31.1 KB (31143 bytes)  
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
