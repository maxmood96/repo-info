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
-	[`influxdb:1.11.7`](#influxdb1117)
-	[`influxdb:1.11.7-alpine`](#influxdb1117-alpine)
-	[`influxdb:1.11.7-data`](#influxdb1117-data)
-	[`influxdb:1.11.7-data-alpine`](#influxdb1117-data-alpine)
-	[`influxdb:1.11.7-meta`](#influxdb1117-meta)
-	[`influxdb:1.11.7-meta-alpine`](#influxdb1117-meta-alpine)
-	[`influxdb:2`](#influxdb2)
-	[`influxdb:2-alpine`](#influxdb2-alpine)
-	[`influxdb:2.7`](#influxdb27)
-	[`influxdb:2.7-alpine`](#influxdb27-alpine)
-	[`influxdb:2.7.10`](#influxdb2710)
-	[`influxdb:2.7.10-alpine`](#influxdb2710-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:0350f7eb8277127340bbe7edfe752f6260d5944b8d1f35e59c35e89c4ea323b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:6e30122329518e8ace91cd9747e7b0084d36443c22c2e1506ae7f16d0008f279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112224210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754fa0397c9b3007af43f8f965869e143e9ce33b6bdcfa3f90ab1841250ae41c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1c6ed56ea7c844956d34126990b109797cf13c2518bab01ae5817c2c812d92`  
		Last Modified: Sat, 19 Oct 2024 02:09:03 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de914bfaa75a7e07dcae267f7777db29af6c32267ec09a1ca15435e84424281`  
		Last Modified: Sat, 19 Oct 2024 02:09:04 GMT  
		Size: 41.4 MB (41377734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b42587b558dd363c3ac20962c0fea42aeb3b8aae210b77b1724501ea72885e9`  
		Last Modified: Sat, 19 Oct 2024 02:09:03 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84706a6d84ed8fe40b22fee708ae5bdc870d3b2f6753e6a11a151008c9c4a6a`  
		Last Modified: Sat, 19 Oct 2024 02:09:03 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101c797a91c3de8fd7881bae6edef0c0c1f5994c749c53b4c87694da0279dcbf`  
		Last Modified: Sat, 19 Oct 2024 02:09:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:07b42e8a67a1dab4f7400f257c074db405edfb428a650d29cf51bf7839efe8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4659029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09020f0616df080bf8af89939db6ddb8ab03c9e3d332416b5e8e6ecc4a4c535f`

```dockerfile
```

-	Layers:
	-	`sha256:28d8d36bda740bb236d90b38c08847f3cb5384417f1eb2527e6ffbbf0956125c`  
		Last Modified: Sat, 19 Oct 2024 02:09:03 GMT  
		Size: 4.6 MB (4644321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cc0d554dc63ed6f6725193e40283df2c4fc33cbd55c88e8a4259e8a3706de9a`  
		Last Modified: Sat, 19 Oct 2024 02:09:03 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:370d944030462279c3189799e5c3a9d15220d6e487ca03af94a1f8788a4da9f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:653874d25b1383462b359d675210b3cd438173fb871ed520b1cdc0dbdb517b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46172232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c04e5c493c1f404d57e8d8bcd8afe95a301d364b74a83e9177e62b4bedcd1b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18613db354a55d6bb85cd76fb0f3e831e6591ad95c34b88f90658be65f7116d`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e59caec40e984bfa16a5e7147968ab7a9269dd4b26c967e537a1f2501ed3ad`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 1.2 MB (1223703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0757cceaa7ec332ca815a4d90b3f46ded79411250ca9f1889fb270327c0173`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 41.3 MB (41322669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14ee22e9d502bd5298b3848671c5557c53049eb7f60df36ec4f2f758a67b3c9`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4be3d77ac7975178bcbbc3155b75b76f8923053f65fa7663f3a5af12c53ec52`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fdf656cf90fdf1b8f8f48b71a53775179b0b60ae49f34b8acc0b7153d19a41`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:6d05144fbccc788aaccf6d1dc2007869d0da21c50e5f9e736bea204ad9359559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.8 KB (769822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f819c61fc69d757bc44998f0fdba45add017b7d4237cb95072f25a6cd43e6fb3`

```dockerfile
```

-	Layers:
	-	`sha256:c4a3a4d77fa125bb5220f97544befc1b5519f459c8192d57f7c18b73abb78f26`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 753.4 KB (753398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:830ea66b76032518b0106771dfbc761eb4d76f6dd29fe1f3fe5182d0ca1bd055`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:d4ffb22b36f794d428d933e97a1faede288ffa90abbd80e771301ddbc5e2612a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:5dc69bbbb2f8ce7cbabdb22add0dc79a4e82df3b28f9fc3dc934eb0b278f058f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90940823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74ebd282f986f28dc5901fef8b24a7f673b07948c4a789e965210c99322210f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa03d139b5b8d55255649074e18e0356915d1d3cd37f61b06888da31056519d8`  
		Last Modified: Sat, 19 Oct 2024 02:09:12 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab583c30458bd0f3a2212f09fae65a9bb0269f029487bfd1236d132e8755139`  
		Last Modified: Sat, 19 Oct 2024 02:09:13 GMT  
		Size: 20.1 MB (20095556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349b865c82f9e38a608c4fad06064a25ff893670949803caa0b03cc43d1dab26`  
		Last Modified: Sat, 19 Oct 2024 02:09:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9015644a0c987d47808ebd4b27662faac2fd814b235a8826d877e29066af7f`  
		Last Modified: Sat, 19 Oct 2024 02:09:06 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:289800a0b4d1835d171704e47bf2d61affabf79e11ae86363e1d9031065c7fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4581975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f832430fbbe4f33c6b4e12a398af524ffbf00b2534b00facec51b0ad1f3403be`

```dockerfile
```

-	Layers:
	-	`sha256:20c94958f95f6acd40f6d4ff9b98ba0f7f7fc53e41d5d322ab993e016d0ae6e3`  
		Last Modified: Sat, 19 Oct 2024 02:09:13 GMT  
		Size: 4.6 MB (4568908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e2dcf6797fec304f5aa0ad38a2b2c81700b2f1c016da14ea8440c38b3b6112d`  
		Last Modified: Sat, 19 Oct 2024 02:09:12 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:67adfea4d46a3f7184cb062485f23b1a8e47fd5784741dd2a33d267f376e86af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:bf763c0bcb054bc0918be70c7d67966b574dab590dfd3d3d8272aa5819112dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24890434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049d73c8ab49415eb2b21665604553ab378cd72545e8f274d895c11927af5730`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03dd48d2c5535d4eea4020d819b1c2b0614d8341047cf5641226da18956a050`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38aa5ba473028136559f78cd4be4fbc2d308adc5e1a5b8ca6025a8bbd55bc14f`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 1.2 MB (1223696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6ebc99cde426570222ae63c2e8e75b500db24c701aba4ddc9229103f38f73`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 20.0 MB (20042088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c061eb560cf799acbda3a5059aeb5c12617459ebc4e38b3f7d08b3c260f27940`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1615cdb4622a98fc159240966cfd0a445043128fbdc8809aba87498e565b2363`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:895aac1fbc74f937fcc6a6cdd1af858062f0e38a93dca57ba46a81ba91d834c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (693036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ff6674d0a004b9c79820b00b6131411dfea7b092bec38adb7e659755c18100`

```dockerfile
```

-	Layers:
	-	`sha256:55fdeb6f675534ee479e135766703a171beb48fe4353e726089a3ccd9a9a1551`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 678.2 KB (678247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed4aae58d0b14a616bd7f18d98c46612d64c769948b0b9230b62aa54a91074c`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 14.8 KB (14789 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data`

```console
$ docker pull influxdb@sha256:0350f7eb8277127340bbe7edfe752f6260d5944b8d1f35e59c35e89c4ea323b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:6e30122329518e8ace91cd9747e7b0084d36443c22c2e1506ae7f16d0008f279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112224210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754fa0397c9b3007af43f8f965869e143e9ce33b6bdcfa3f90ab1841250ae41c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1c6ed56ea7c844956d34126990b109797cf13c2518bab01ae5817c2c812d92`  
		Last Modified: Sat, 19 Oct 2024 02:09:03 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de914bfaa75a7e07dcae267f7777db29af6c32267ec09a1ca15435e84424281`  
		Last Modified: Sat, 19 Oct 2024 02:09:04 GMT  
		Size: 41.4 MB (41377734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b42587b558dd363c3ac20962c0fea42aeb3b8aae210b77b1724501ea72885e9`  
		Last Modified: Sat, 19 Oct 2024 02:09:03 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84706a6d84ed8fe40b22fee708ae5bdc870d3b2f6753e6a11a151008c9c4a6a`  
		Last Modified: Sat, 19 Oct 2024 02:09:03 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101c797a91c3de8fd7881bae6edef0c0c1f5994c749c53b4c87694da0279dcbf`  
		Last Modified: Sat, 19 Oct 2024 02:09:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:07b42e8a67a1dab4f7400f257c074db405edfb428a650d29cf51bf7839efe8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4659029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09020f0616df080bf8af89939db6ddb8ab03c9e3d332416b5e8e6ecc4a4c535f`

```dockerfile
```

-	Layers:
	-	`sha256:28d8d36bda740bb236d90b38c08847f3cb5384417f1eb2527e6ffbbf0956125c`  
		Last Modified: Sat, 19 Oct 2024 02:09:03 GMT  
		Size: 4.6 MB (4644321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cc0d554dc63ed6f6725193e40283df2c4fc33cbd55c88e8a4259e8a3706de9a`  
		Last Modified: Sat, 19 Oct 2024 02:09:03 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-data-alpine`

```console
$ docker pull influxdb@sha256:370d944030462279c3189799e5c3a9d15220d6e487ca03af94a1f8788a4da9f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:653874d25b1383462b359d675210b3cd438173fb871ed520b1cdc0dbdb517b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46172232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c04e5c493c1f404d57e8d8bcd8afe95a301d364b74a83e9177e62b4bedcd1b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18613db354a55d6bb85cd76fb0f3e831e6591ad95c34b88f90658be65f7116d`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e59caec40e984bfa16a5e7147968ab7a9269dd4b26c967e537a1f2501ed3ad`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 1.2 MB (1223703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0757cceaa7ec332ca815a4d90b3f46ded79411250ca9f1889fb270327c0173`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 41.3 MB (41322669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14ee22e9d502bd5298b3848671c5557c53049eb7f60df36ec4f2f758a67b3c9`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4be3d77ac7975178bcbbc3155b75b76f8923053f65fa7663f3a5af12c53ec52`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fdf656cf90fdf1b8f8f48b71a53775179b0b60ae49f34b8acc0b7153d19a41`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:6d05144fbccc788aaccf6d1dc2007869d0da21c50e5f9e736bea204ad9359559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.8 KB (769822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f819c61fc69d757bc44998f0fdba45add017b7d4237cb95072f25a6cd43e6fb3`

```dockerfile
```

-	Layers:
	-	`sha256:c4a3a4d77fa125bb5220f97544befc1b5519f459c8192d57f7c18b73abb78f26`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 753.4 KB (753398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:830ea66b76032518b0106771dfbc761eb4d76f6dd29fe1f3fe5182d0ca1bd055`  
		Last Modified: Fri, 06 Sep 2024 23:21:24 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-meta`

```console
$ docker pull influxdb@sha256:d4ffb22b36f794d428d933e97a1faede288ffa90abbd80e771301ddbc5e2612a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:5dc69bbbb2f8ce7cbabdb22add0dc79a4e82df3b28f9fc3dc934eb0b278f058f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90940823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74ebd282f986f28dc5901fef8b24a7f673b07948c4a789e965210c99322210f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa03d139b5b8d55255649074e18e0356915d1d3cd37f61b06888da31056519d8`  
		Last Modified: Sat, 19 Oct 2024 02:09:12 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab583c30458bd0f3a2212f09fae65a9bb0269f029487bfd1236d132e8755139`  
		Last Modified: Sat, 19 Oct 2024 02:09:13 GMT  
		Size: 20.1 MB (20095556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349b865c82f9e38a608c4fad06064a25ff893670949803caa0b03cc43d1dab26`  
		Last Modified: Sat, 19 Oct 2024 02:09:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9015644a0c987d47808ebd4b27662faac2fd814b235a8826d877e29066af7f`  
		Last Modified: Sat, 19 Oct 2024 02:09:06 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:289800a0b4d1835d171704e47bf2d61affabf79e11ae86363e1d9031065c7fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4581975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f832430fbbe4f33c6b4e12a398af524ffbf00b2534b00facec51b0ad1f3403be`

```dockerfile
```

-	Layers:
	-	`sha256:20c94958f95f6acd40f6d4ff9b98ba0f7f7fc53e41d5d322ab993e016d0ae6e3`  
		Last Modified: Sat, 19 Oct 2024 02:09:13 GMT  
		Size: 4.6 MB (4568908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e2dcf6797fec304f5aa0ad38a2b2c81700b2f1c016da14ea8440c38b3b6112d`  
		Last Modified: Sat, 19 Oct 2024 02:09:12 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.7-meta-alpine`

```console
$ docker pull influxdb@sha256:67adfea4d46a3f7184cb062485f23b1a8e47fd5784741dd2a33d267f376e86af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:bf763c0bcb054bc0918be70c7d67966b574dab590dfd3d3d8272aa5819112dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24890434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049d73c8ab49415eb2b21665604553ab378cd72545e8f274d895c11927af5730`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.10.7-c1.10.7
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03dd48d2c5535d4eea4020d819b1c2b0614d8341047cf5641226da18956a050`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38aa5ba473028136559f78cd4be4fbc2d308adc5e1a5b8ca6025a8bbd55bc14f`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 1.2 MB (1223696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6ebc99cde426570222ae63c2e8e75b500db24c701aba4ddc9229103f38f73`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 20.0 MB (20042088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c061eb560cf799acbda3a5059aeb5c12617459ebc4e38b3f7d08b3c260f27940`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1615cdb4622a98fc159240966cfd0a445043128fbdc8809aba87498e565b2363`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.7-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:895aac1fbc74f937fcc6a6cdd1af858062f0e38a93dca57ba46a81ba91d834c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (693036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ff6674d0a004b9c79820b00b6131411dfea7b092bec38adb7e659755c18100`

```dockerfile
```

-	Layers:
	-	`sha256:55fdeb6f675534ee479e135766703a171beb48fe4353e726089a3ccd9a9a1551`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 678.2 KB (678247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed4aae58d0b14a616bd7f18d98c46612d64c769948b0b9230b62aa54a91074c`  
		Last Modified: Fri, 06 Sep 2024 23:21:29 GMT  
		Size: 14.8 KB (14789 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11`

```console
$ docker pull influxdb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `influxdb:1.11-alpine`

```console
$ docker pull influxdb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:dc79677b4aa1c6cf1b5bfb555b7111054d42877c1d5f91442dd4e3fa421db973
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:df8f2f86f7e62271034a8444b07a6c18102b134fe18747cb1e352ea3f9d9c9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112791299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d411a777905130acf248b1380160710f1ec6183e0a9c1ee7040039c5e92dec6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
# Tue, 22 Oct 2024 18:38:37 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cb73c1f25d997018b9cc28846ea84fe57e4a4c5883da4623abe7e123f4b97d`  
		Last Modified: Tue, 22 Oct 2024 19:55:39 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cf73fd7f87029bec4da74334e55d57ba58a270261a48ee5575af38ad3eb646`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 39.2 MB (39181334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865a2f2131a89c679bd245a568d5fb5664daac7f5fd75f5c491aa31855dc1941`  
		Last Modified: Tue, 22 Oct 2024 19:55:39 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1da84fd8ed5fc42a1eda4653a38c0fc191027a108825f669b2965ba64ceb5bc`  
		Last Modified: Tue, 22 Oct 2024 19:55:39 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858987bbb8646a367e1667562ea1979ab8243521544827054725527bac68cfc0`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:9c4f3faa33dcdb07d8d9ed8f1526f91d9f15fc830d0d07631dcf9f31ff1a7041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4530791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6be2d0e317be22ae371dc0851f4e29ab6cebd017b105666e90823cade6002b`

```dockerfile
```

-	Layers:
	-	`sha256:fae2fbd239a0b425952458ce90e8907587447c0005c83e3e834330f49daf4afc`  
		Last Modified: Tue, 22 Oct 2024 19:55:39 GMT  
		Size: 4.5 MB (4516083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a29f2456ed2f579cf549ae1c2a3457d7ff176929f14c9becd427cf8e23d1042e`  
		Last Modified: Tue, 22 Oct 2024 19:55:39 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:ad49e5dc28123617c3e12edddda289c1530784a4849b69c04e606eb093a61507
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2bf58c568b897e69fc5658773843fff04374675297c457dfc68fd6c2097d3d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43973807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec2735b002971e7e01ca23471420052c0e10c6e3c0c6e6ccf0fe5a05dd190b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
# Tue, 22 Oct 2024 18:38:37 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a185138e686e1a1d9f3b53b2f2a6abd64528a85a8eb922cdf189ed8b223347a4`  
		Last Modified: Tue, 22 Oct 2024 19:55:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d36c799fdd7e669e0fe48c8eb90e54306dee6f127c40ff929ad6cf35a4529c9`  
		Last Modified: Tue, 22 Oct 2024 19:55:28 GMT  
		Size: 1.2 MB (1223719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e641724bb4058f188eaa7d4d383a863b72ff39dcef2d464cde520c7c32b490`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 39.1 MB (39124227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ea097cd402766e6b3554e6976cde456348ff788b9db91477aa34684fd5f57`  
		Last Modified: Tue, 22 Oct 2024 19:55:28 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a1167bd862c49733bf143c75fc4dd6c80411dce107edd4be118ab0d9ce91fb`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c129121d0e9601e0fb07b807bdc9aae1c68ae775ba77ed5add2146eb0b0842`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3603705e2897e20955af8dddd779b728e9a169452731d30265f37614643d7180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.6 KB (768583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4c22a5676679b4621db7b3f42d7bc70d3e006ddc2aafc25f5af56bea6847e5`

```dockerfile
```

-	Layers:
	-	`sha256:513f56d3aaecf3a74e2b7d8eb3b4b0bac609769478e710828030d0efdcb3d8a5`  
		Last Modified: Tue, 22 Oct 2024 19:55:28 GMT  
		Size: 752.1 KB (752127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2eb359300864052a569a29f5819ed2d35a57b08fa21d60bc3a43074ee0c0fa1`  
		Last Modified: Tue, 22 Oct 2024 19:55:28 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:324dc7ccb37043f3fbd6bfbb41639c1bdb5c3d87149345da84ff70cffacbbb8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:bd51f6c79dc707f60835c270d148fe09441a3c11d760f0f2676508e421f7c9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91947183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae65b6c179f4a8bae9b5d336ffdbe13a1cc2f19ce6e35d82b2697fdc4a69fdbb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
# Tue, 22 Oct 2024 18:38:37 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4271041c992e1b29e1311dcc5a0f359777850d4e00f9c9fecc0b3db2396ec753`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd319d196194fb4d7532ddff4a18a84af8c5c274c494d9cf58ecb846d6d379db`  
		Last Modified: Tue, 22 Oct 2024 19:55:30 GMT  
		Size: 18.3 MB (18338436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9cf0395500cbe1eb73aaa758f79d62f40774aff7e8bdf89734af8767575e20`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cefe9e010247bfd5d559332fd05cc724989d5b5dbbf966369cf1880b7acc19`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:31a31b2f2e39563a646c1bc5543c4cf8eb0800e9e669ff99a9b32c10a3c046c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4454716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618e2f8be16bf50bba2842964c6f66263206a6ed670693caccfbeb0510f4240a`

```dockerfile
```

-	Layers:
	-	`sha256:fa665579b229821172233002da0c67f1e677503741138a167fd7d48d55762166`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 4.4 MB (4441650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1535556d0192f9c23afb8c689003667b096d84876078998f413219f8abb8ed87`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 13.1 KB (13066 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:54390249fd16d3dd5d3ae5532e4f5e4947d3699c7cf9f86cf01969701af933f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5519e6f392b9b6bac8fe0692736e932e88e562be182fccc68d4f29306ff1294e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23140384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1761175d53d338eeb8ae6cae7a084bbf910e77514f95288b169a35c0c4cfeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
# Tue, 22 Oct 2024 18:38:37 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026096a9cfda2bbaf343f6e4243a510194993c33eb3749d697db62a689c36973`  
		Last Modified: Tue, 22 Oct 2024 19:55:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78a94b3eb42ef271eb9bca16e4945cea2e859e6e8b67b82a4ed9df9c70c5f56`  
		Last Modified: Tue, 22 Oct 2024 19:55:26 GMT  
		Size: 1.2 MB (1223724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c106916356d7da9b937f12cbd6ce5fc3265a1848fff00627eac970ea712e9ad`  
		Last Modified: Tue, 22 Oct 2024 19:55:26 GMT  
		Size: 18.3 MB (18292007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6553874a16bdce65ae37e4bf96ba7cfbec96a0754022972ffbcbac01fbb38e`  
		Last Modified: Tue, 22 Oct 2024 19:55:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589872db2dbf75cfcd25b08536b500adfc53d2edb53be80dfe1c323f3e52f92f`  
		Last Modified: Tue, 22 Oct 2024 19:55:27 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bcb0ab42cd2772afc07d037b222f8d1f1e8f691241e38f502f3c34e765bf3e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.3 KB (693304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc215c44b49e3cab35b25383e39a6a238c66cc434334151e869c90253669275`

```dockerfile
```

-	Layers:
	-	`sha256:0a6a2541a572b3b8d3f52689dbc39e1a45bda03d6e403994d1a048458a0672dc`  
		Last Modified: Tue, 22 Oct 2024 19:55:26 GMT  
		Size: 678.5 KB (678481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb2c1ffe68267c74f74c5bd7a6dc573538b06b5c5dea6a97e7803c2ee7b0329`  
		Last Modified: Tue, 22 Oct 2024 19:55:26 GMT  
		Size: 14.8 KB (14823 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.7`

```console
$ docker pull influxdb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `influxdb:1.11.7-alpine`

```console
$ docker pull influxdb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `influxdb:1.11.7-data`

```console
$ docker pull influxdb@sha256:dc79677b4aa1c6cf1b5bfb555b7111054d42877c1d5f91442dd4e3fa421db973
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:df8f2f86f7e62271034a8444b07a6c18102b134fe18747cb1e352ea3f9d9c9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112791299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d411a777905130acf248b1380160710f1ec6183e0a9c1ee7040039c5e92dec6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
# Tue, 22 Oct 2024 18:38:37 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cb73c1f25d997018b9cc28846ea84fe57e4a4c5883da4623abe7e123f4b97d`  
		Last Modified: Tue, 22 Oct 2024 19:55:39 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cf73fd7f87029bec4da74334e55d57ba58a270261a48ee5575af38ad3eb646`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 39.2 MB (39181334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865a2f2131a89c679bd245a568d5fb5664daac7f5fd75f5c491aa31855dc1941`  
		Last Modified: Tue, 22 Oct 2024 19:55:39 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1da84fd8ed5fc42a1eda4653a38c0fc191027a108825f669b2965ba64ceb5bc`  
		Last Modified: Tue, 22 Oct 2024 19:55:39 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858987bbb8646a367e1667562ea1979ab8243521544827054725527bac68cfc0`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.7-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:9c4f3faa33dcdb07d8d9ed8f1526f91d9f15fc830d0d07631dcf9f31ff1a7041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4530791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6be2d0e317be22ae371dc0851f4e29ab6cebd017b105666e90823cade6002b`

```dockerfile
```

-	Layers:
	-	`sha256:fae2fbd239a0b425952458ce90e8907587447c0005c83e3e834330f49daf4afc`  
		Last Modified: Tue, 22 Oct 2024 19:55:39 GMT  
		Size: 4.5 MB (4516083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a29f2456ed2f579cf549ae1c2a3457d7ff176929f14c9becd427cf8e23d1042e`  
		Last Modified: Tue, 22 Oct 2024 19:55:39 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.7-data-alpine`

```console
$ docker pull influxdb@sha256:ad49e5dc28123617c3e12edddda289c1530784a4849b69c04e606eb093a61507
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2bf58c568b897e69fc5658773843fff04374675297c457dfc68fd6c2097d3d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43973807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec2735b002971e7e01ca23471420052c0e10c6e3c0c6e6ccf0fe5a05dd190b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
# Tue, 22 Oct 2024 18:38:37 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a185138e686e1a1d9f3b53b2f2a6abd64528a85a8eb922cdf189ed8b223347a4`  
		Last Modified: Tue, 22 Oct 2024 19:55:28 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d36c799fdd7e669e0fe48c8eb90e54306dee6f127c40ff929ad6cf35a4529c9`  
		Last Modified: Tue, 22 Oct 2024 19:55:28 GMT  
		Size: 1.2 MB (1223719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e641724bb4058f188eaa7d4d383a863b72ff39dcef2d464cde520c7c32b490`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 39.1 MB (39124227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ea097cd402766e6b3554e6976cde456348ff788b9db91477aa34684fd5f57`  
		Last Modified: Tue, 22 Oct 2024 19:55:28 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a1167bd862c49733bf143c75fc4dd6c80411dce107edd4be118ab0d9ce91fb`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c129121d0e9601e0fb07b807bdc9aae1c68ae775ba77ed5add2146eb0b0842`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.7-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3603705e2897e20955af8dddd779b728e9a169452731d30265f37614643d7180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.6 KB (768583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4c22a5676679b4621db7b3f42d7bc70d3e006ddc2aafc25f5af56bea6847e5`

```dockerfile
```

-	Layers:
	-	`sha256:513f56d3aaecf3a74e2b7d8eb3b4b0bac609769478e710828030d0efdcb3d8a5`  
		Last Modified: Tue, 22 Oct 2024 19:55:28 GMT  
		Size: 752.1 KB (752127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2eb359300864052a569a29f5819ed2d35a57b08fa21d60bc3a43074ee0c0fa1`  
		Last Modified: Tue, 22 Oct 2024 19:55:28 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.7-meta`

```console
$ docker pull influxdb@sha256:324dc7ccb37043f3fbd6bfbb41639c1bdb5c3d87149345da84ff70cffacbbb8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:bd51f6c79dc707f60835c270d148fe09441a3c11d760f0f2676508e421f7c9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91947183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae65b6c179f4a8bae9b5d336ffdbe13a1cc2f19ce6e35d82b2697fdc4a69fdbb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
# Tue, 22 Oct 2024 18:38:37 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4271041c992e1b29e1311dcc5a0f359777850d4e00f9c9fecc0b3db2396ec753`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd319d196194fb4d7532ddff4a18a84af8c5c274c494d9cf58ecb846d6d379db`  
		Last Modified: Tue, 22 Oct 2024 19:55:30 GMT  
		Size: 18.3 MB (18338436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9cf0395500cbe1eb73aaa758f79d62f40774aff7e8bdf89734af8767575e20`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cefe9e010247bfd5d559332fd05cc724989d5b5dbbf966369cf1880b7acc19`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.7-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:31a31b2f2e39563a646c1bc5543c4cf8eb0800e9e669ff99a9b32c10a3c046c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4454716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618e2f8be16bf50bba2842964c6f66263206a6ed670693caccfbeb0510f4240a`

```dockerfile
```

-	Layers:
	-	`sha256:fa665579b229821172233002da0c67f1e677503741138a167fd7d48d55762166`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 4.4 MB (4441650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1535556d0192f9c23afb8c689003667b096d84876078998f413219f8abb8ed87`  
		Last Modified: Tue, 22 Oct 2024 19:55:29 GMT  
		Size: 13.1 KB (13066 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.7-meta-alpine`

```console
$ docker pull influxdb@sha256:54390249fd16d3dd5d3ae5532e4f5e4947d3699c7cf9f86cf01969701af933f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5519e6f392b9b6bac8fe0692736e932e88e562be182fccc68d4f29306ff1294e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23140384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1761175d53d338eeb8ae6cae7a084bbf910e77514f95288b169a35c0c4cfeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=1.11.7-c1.11.7
# Tue, 22 Oct 2024 18:38:37 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026096a9cfda2bbaf343f6e4243a510194993c33eb3749d697db62a689c36973`  
		Last Modified: Tue, 22 Oct 2024 19:55:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78a94b3eb42ef271eb9bca16e4945cea2e859e6e8b67b82a4ed9df9c70c5f56`  
		Last Modified: Tue, 22 Oct 2024 19:55:26 GMT  
		Size: 1.2 MB (1223724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c106916356d7da9b937f12cbd6ce5fc3265a1848fff00627eac970ea712e9ad`  
		Last Modified: Tue, 22 Oct 2024 19:55:26 GMT  
		Size: 18.3 MB (18292007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6553874a16bdce65ae37e4bf96ba7cfbec96a0754022972ffbcbac01fbb38e`  
		Last Modified: Tue, 22 Oct 2024 19:55:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589872db2dbf75cfcd25b08536b500adfc53d2edb53be80dfe1c323f3e52f92f`  
		Last Modified: Tue, 22 Oct 2024 19:55:27 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.7-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bcb0ab42cd2772afc07d037b222f8d1f1e8f691241e38f502f3c34e765bf3e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.3 KB (693304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc215c44b49e3cab35b25383e39a6a238c66cc434334151e869c90253669275`

```dockerfile
```

-	Layers:
	-	`sha256:0a6a2541a572b3b8d3f52689dbc39e1a45bda03d6e403994d1a048458a0672dc`  
		Last Modified: Tue, 22 Oct 2024 19:55:26 GMT  
		Size: 678.5 KB (678481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb2c1ffe68267c74f74c5bd7a6dc573538b06b5c5dea6a97e7803c2ee7b0329`  
		Last Modified: Tue, 22 Oct 2024 19:55:26 GMT  
		Size: 14.8 KB (14823 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:32418efff9e2e2efb99f0c93c78f2a2cd4f5316ec8c2983a64c9a53925f96fcc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:f5d5196210d9fb9acf485f18bdba66a0146b4ea1565005a6dc222e54c73f1390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168893012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903cf06eba30eddc4f08a676144fd3b03d2d0ac76bcdc42911bfad8bcca01b56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV GOSU_VER=1.16
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aafd1fd27c9676f57cb06374aa92c43541fcf93e2720bf3fa5d5bf45a284109`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 9.8 MB (9789031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61735b6533a48feec22deeb5e11cfc795f344ddd91e8cda094b5fbbfd789c6f2`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 5.8 MB (5820924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f27f427a2ce3808d8d9a09b50c52ff0933efa417b0bb9d281ec378def2d968`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf90975e867fab7ff0862159e12b24232ccebe662618746db3dc2d820506fbb`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 1.0 MB (1006363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55253b104f96a5e5ab0e9190cdbbf891d973155a6bd43a3e0f7dfe665e9b84b6`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 99.6 MB (99594050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b1de93c35668207e140c849313b99d49006c6f8fcc9cb1623a3a3915f10590`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 23.5 MB (23546404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd940528b08fc4347e306e9ba4c6be5cca185b598a9545f915c09fc97c2727a8`  
		Last Modified: Tue, 22 Oct 2024 19:55:48 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d55333cb59d840ce4b040a27abe0d24b5e44c9ec76107ad85193b5b3a086606`  
		Last Modified: Tue, 22 Oct 2024 19:55:48 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff84a72bb18b35058f8c116017714f3b4a543263aa2aa29ecddfca1b2519479`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:9cde691a07e51f352cc9ee6307c46b4a793741ba7a49f418037bba33d7ab9fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b20c55a4f47fd0d3aec51ead07b507cd683ae9693d265dd7e85159462b6d3df`

```dockerfile
```

-	Layers:
	-	`sha256:25056c70fdda68055fcfffd672a27976cc63407c18987e45e009d739d4e06e9c`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 2.8 MB (2849661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3057611b4133f25ca576be26bf2380aba98ff5136f48e234f51188f477b24de2`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 33.5 KB (33519 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:53c9749a685778bacdae9243980b8e5d0d0ef1ceb947ae41f91f50f621bdd595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162779131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bba075abbdb7b751d98b8f4ea79668db114d755eeb1e92bc60f42cb0086c961`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV GOSU_VER=1.16
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07320876b49207ad14955b1a31e4206a2a4153727413f4e8fcda5fd99916b4d4`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 9.6 MB (9587112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270e2f52b84341a01fd4a919bc929d7490c2caa4e34017d8376c18acf47acab0`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 5.5 MB (5463796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8837b8381563c809d09e25282b246ced163daf23d4c3c348813468b2323ad3a8`  
		Last Modified: Tue, 22 Oct 2024 19:55:08 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054534f2dd1b04e74b7e15809341ecf0eaf97c8736f86600f77b8e29157eb2ec`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d35e35d48ef6197e613fc0a0ff0dcc745084aa9439077bd2fc66add3b7885c6`  
		Last Modified: Tue, 22 Oct 2024 19:55:11 GMT  
		Size: 95.4 MB (95427909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb1b21f57ab00e3ecc4e16f96efeb63f8475fef567e59e85331bfb428ecf23f`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 22.2 MB (22197911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b88297b74f1c1c8700a853a735372741aadc94d4467ea21b2373a36ed465bf4`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37363f631d39bc3f49ae72bacaad18758d54157dbf4308a1a3f1b7aaa3eb4b89`  
		Last Modified: Tue, 22 Oct 2024 19:55:10 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013632725e99110127ab8f36dca492a8346ea517875e282a611b494b519e33d9`  
		Last Modified: Tue, 22 Oct 2024 19:55:10 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:684e07d361a121efaffb0611b94bb5bd45e4fbfd743f323029d3a52f633bd3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d6ca703457d4c565f9d48a20f346d8cfeaa0d9d18d394c948b0017c3e323fc`

```dockerfile
```

-	Layers:
	-	`sha256:f8b67510dcce1fc81e9b513aa534ce749c701750b139696527cbb54bb78e320f`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 2.8 MB (2848898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:514acbd511f7db84016cde5cc9c611926cde97d7b7733a7fa188ca8993a6d91b`  
		Last Modified: Tue, 22 Oct 2024 19:55:08 GMT  
		Size: 33.8 KB (33761 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:407ed49d0b3e32362bbf9ee21740240893e62b9249a02397613a229652f64947
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:08d9e62b3e25b4ce5f55622654cd9979b9924aa0998a6c99923b75ae9fdda5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92442213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3badb18d31efb02e2268ff147fdea982e5dc8ee37b91e9010f5cf9488902a80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b052686eee98bc6eac2c55cdfc21b65703f40675b7e9a5ca8e363d4a8ab9db5a`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706bb39608a9fcc40a7863636b565e99300c14ebc8b01f8bee1bff576c3e346`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 9.7 MB (9652593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ba18c78730dca1ca920a72c5726b025a65089135c61e1e7a620d2b8471aaf4`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 5.8 MB (5820948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9991745f19f0cd45fc9ebc1c6befa3e94edb8a86cbe904216c1587e181bd2744`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd348b19e68ff1bdb0996ccae6df22753a67375d9593bf21fd727a06e11ec287`  
		Last Modified: Tue, 22 Oct 2024 19:55:32 GMT  
		Size: 49.8 MB (49790480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd1a635dcb59a7467f149e2c219346dc61ed6b816f1f0c8c50cde8c93b6b906`  
		Last Modified: Tue, 22 Oct 2024 19:55:32 GMT  
		Size: 23.5 MB (23546418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df577e715b6522db1f03aaf9c81977e416c84780057c41fb1eba468d8ec89224`  
		Last Modified: Tue, 22 Oct 2024 19:55:32 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aecd514cd25e9280e55610db5fc320bf07e9126415afe525e6f4d175627504`  
		Last Modified: Tue, 22 Oct 2024 19:55:33 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0853b6e6870bd74b624b56f40a38c3969af280d53dcac93cbc17ca967616e5fd`  
		Last Modified: Tue, 22 Oct 2024 19:55:33 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:874d5ec3cadb36a32bb07237b420a1f7dae1dc6b415d21edfca911a927fe74ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.4 KB (945413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878e61de24e216371cac057fae352502997f57115a18b176576275a51ad1fe16`

```dockerfile
```

-	Layers:
	-	`sha256:4c65636c7d529fd8d5be516ddf758b354823b8e602754c591ade112e0be41164`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 914.6 KB (914627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f494aa2572ef03fc09cba49db7a2ad4aa6a765e47a796f64ca5b1fc653c8d75`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:01d0fcd91674b394d26ef8f1eec9c475b7f403cf10257ebaed77ec26145856ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89244002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb389848654e8f0ea7f36e3dfb29bf5e97ff8c54e33400209ee70a5fb81ded1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deeb5bb87a9b047197ab047408d669771534ddd651ad86d0935717add352c29`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad71f843ccedd874c5468e97b4b7c17395262d7353e4ed6006aba08e18fae887`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 9.8 MB (9777142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a3e38e2ffb00f3e4786fdd01dd079eda34b3f65d8a05db74836f3739c0c8d1`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2def60e9aeb441cfc22ae4a5c007f86e41791863e6784828ec74390badf73a`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ea43a5fa5d50a03fbdbb5319d38071b43fd93879cfbb15f62721f491a347e4`  
		Last Modified: Tue, 22 Oct 2024 19:55:43 GMT  
		Size: 47.7 MB (47709532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047065b1bd569a1dee11f1813ce0051a11c7472c7d35e711609ecc2cbe7ad5d`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 22.2 MB (22197917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f9468215c53e8a896f9b934d83b0d0768f4e0e81441f0d8c5add921b1174d2`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a140ff0494c018fe34ddb0023fba7f95c40cf6201e1696fcec6901da350da6f0`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae45bb58db1b991a86bfe2c36cc8a55c4a9edcfbff715ebbab68907c6fc408`  
		Last Modified: Tue, 22 Oct 2024 19:55:43 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:5557d1011f8db6c8306114ebdb7f1caf2d969f06efc2b66ee34bb61b1fbb78a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.9 KB (944862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed25776500d61570cd6a6deb6a7b8e1855d3e69d44483c688c9a45185ca50ac6`

```dockerfile
```

-	Layers:
	-	`sha256:3af9a32ee0668a6af608337bcddbecc855029efd69933e9046f36682e84a2ad9`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 913.9 KB (913888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3370bfe3452a6e94532bb5823680a91661f51f027ee384f8ab7db7f969d8ea`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:32418efff9e2e2efb99f0c93c78f2a2cd4f5316ec8c2983a64c9a53925f96fcc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:f5d5196210d9fb9acf485f18bdba66a0146b4ea1565005a6dc222e54c73f1390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168893012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903cf06eba30eddc4f08a676144fd3b03d2d0ac76bcdc42911bfad8bcca01b56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV GOSU_VER=1.16
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aafd1fd27c9676f57cb06374aa92c43541fcf93e2720bf3fa5d5bf45a284109`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 9.8 MB (9789031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61735b6533a48feec22deeb5e11cfc795f344ddd91e8cda094b5fbbfd789c6f2`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 5.8 MB (5820924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f27f427a2ce3808d8d9a09b50c52ff0933efa417b0bb9d281ec378def2d968`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf90975e867fab7ff0862159e12b24232ccebe662618746db3dc2d820506fbb`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 1.0 MB (1006363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55253b104f96a5e5ab0e9190cdbbf891d973155a6bd43a3e0f7dfe665e9b84b6`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 99.6 MB (99594050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b1de93c35668207e140c849313b99d49006c6f8fcc9cb1623a3a3915f10590`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 23.5 MB (23546404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd940528b08fc4347e306e9ba4c6be5cca185b598a9545f915c09fc97c2727a8`  
		Last Modified: Tue, 22 Oct 2024 19:55:48 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d55333cb59d840ce4b040a27abe0d24b5e44c9ec76107ad85193b5b3a086606`  
		Last Modified: Tue, 22 Oct 2024 19:55:48 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff84a72bb18b35058f8c116017714f3b4a543263aa2aa29ecddfca1b2519479`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:9cde691a07e51f352cc9ee6307c46b4a793741ba7a49f418037bba33d7ab9fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b20c55a4f47fd0d3aec51ead07b507cd683ae9693d265dd7e85159462b6d3df`

```dockerfile
```

-	Layers:
	-	`sha256:25056c70fdda68055fcfffd672a27976cc63407c18987e45e009d739d4e06e9c`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 2.8 MB (2849661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3057611b4133f25ca576be26bf2380aba98ff5136f48e234f51188f477b24de2`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 33.5 KB (33519 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:53c9749a685778bacdae9243980b8e5d0d0ef1ceb947ae41f91f50f621bdd595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162779131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bba075abbdb7b751d98b8f4ea79668db114d755eeb1e92bc60f42cb0086c961`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV GOSU_VER=1.16
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07320876b49207ad14955b1a31e4206a2a4153727413f4e8fcda5fd99916b4d4`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 9.6 MB (9587112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270e2f52b84341a01fd4a919bc929d7490c2caa4e34017d8376c18acf47acab0`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 5.5 MB (5463796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8837b8381563c809d09e25282b246ced163daf23d4c3c348813468b2323ad3a8`  
		Last Modified: Tue, 22 Oct 2024 19:55:08 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054534f2dd1b04e74b7e15809341ecf0eaf97c8736f86600f77b8e29157eb2ec`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d35e35d48ef6197e613fc0a0ff0dcc745084aa9439077bd2fc66add3b7885c6`  
		Last Modified: Tue, 22 Oct 2024 19:55:11 GMT  
		Size: 95.4 MB (95427909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb1b21f57ab00e3ecc4e16f96efeb63f8475fef567e59e85331bfb428ecf23f`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 22.2 MB (22197911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b88297b74f1c1c8700a853a735372741aadc94d4467ea21b2373a36ed465bf4`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37363f631d39bc3f49ae72bacaad18758d54157dbf4308a1a3f1b7aaa3eb4b89`  
		Last Modified: Tue, 22 Oct 2024 19:55:10 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013632725e99110127ab8f36dca492a8346ea517875e282a611b494b519e33d9`  
		Last Modified: Tue, 22 Oct 2024 19:55:10 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:684e07d361a121efaffb0611b94bb5bd45e4fbfd743f323029d3a52f633bd3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d6ca703457d4c565f9d48a20f346d8cfeaa0d9d18d394c948b0017c3e323fc`

```dockerfile
```

-	Layers:
	-	`sha256:f8b67510dcce1fc81e9b513aa534ce749c701750b139696527cbb54bb78e320f`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 2.8 MB (2848898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:514acbd511f7db84016cde5cc9c611926cde97d7b7733a7fa188ca8993a6d91b`  
		Last Modified: Tue, 22 Oct 2024 19:55:08 GMT  
		Size: 33.8 KB (33761 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:407ed49d0b3e32362bbf9ee21740240893e62b9249a02397613a229652f64947
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:08d9e62b3e25b4ce5f55622654cd9979b9924aa0998a6c99923b75ae9fdda5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92442213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3badb18d31efb02e2268ff147fdea982e5dc8ee37b91e9010f5cf9488902a80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b052686eee98bc6eac2c55cdfc21b65703f40675b7e9a5ca8e363d4a8ab9db5a`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706bb39608a9fcc40a7863636b565e99300c14ebc8b01f8bee1bff576c3e346`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 9.7 MB (9652593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ba18c78730dca1ca920a72c5726b025a65089135c61e1e7a620d2b8471aaf4`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 5.8 MB (5820948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9991745f19f0cd45fc9ebc1c6befa3e94edb8a86cbe904216c1587e181bd2744`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd348b19e68ff1bdb0996ccae6df22753a67375d9593bf21fd727a06e11ec287`  
		Last Modified: Tue, 22 Oct 2024 19:55:32 GMT  
		Size: 49.8 MB (49790480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd1a635dcb59a7467f149e2c219346dc61ed6b816f1f0c8c50cde8c93b6b906`  
		Last Modified: Tue, 22 Oct 2024 19:55:32 GMT  
		Size: 23.5 MB (23546418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df577e715b6522db1f03aaf9c81977e416c84780057c41fb1eba468d8ec89224`  
		Last Modified: Tue, 22 Oct 2024 19:55:32 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aecd514cd25e9280e55610db5fc320bf07e9126415afe525e6f4d175627504`  
		Last Modified: Tue, 22 Oct 2024 19:55:33 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0853b6e6870bd74b624b56f40a38c3969af280d53dcac93cbc17ca967616e5fd`  
		Last Modified: Tue, 22 Oct 2024 19:55:33 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:874d5ec3cadb36a32bb07237b420a1f7dae1dc6b415d21edfca911a927fe74ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.4 KB (945413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878e61de24e216371cac057fae352502997f57115a18b176576275a51ad1fe16`

```dockerfile
```

-	Layers:
	-	`sha256:4c65636c7d529fd8d5be516ddf758b354823b8e602754c591ade112e0be41164`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 914.6 KB (914627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f494aa2572ef03fc09cba49db7a2ad4aa6a765e47a796f64ca5b1fc653c8d75`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:01d0fcd91674b394d26ef8f1eec9c475b7f403cf10257ebaed77ec26145856ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89244002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb389848654e8f0ea7f36e3dfb29bf5e97ff8c54e33400209ee70a5fb81ded1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deeb5bb87a9b047197ab047408d669771534ddd651ad86d0935717add352c29`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad71f843ccedd874c5468e97b4b7c17395262d7353e4ed6006aba08e18fae887`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 9.8 MB (9777142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a3e38e2ffb00f3e4786fdd01dd079eda34b3f65d8a05db74836f3739c0c8d1`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2def60e9aeb441cfc22ae4a5c007f86e41791863e6784828ec74390badf73a`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ea43a5fa5d50a03fbdbb5319d38071b43fd93879cfbb15f62721f491a347e4`  
		Last Modified: Tue, 22 Oct 2024 19:55:43 GMT  
		Size: 47.7 MB (47709532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047065b1bd569a1dee11f1813ce0051a11c7472c7d35e711609ecc2cbe7ad5d`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 22.2 MB (22197917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f9468215c53e8a896f9b934d83b0d0768f4e0e81441f0d8c5add921b1174d2`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a140ff0494c018fe34ddb0023fba7f95c40cf6201e1696fcec6901da350da6f0`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae45bb58db1b991a86bfe2c36cc8a55c4a9edcfbff715ebbab68907c6fc408`  
		Last Modified: Tue, 22 Oct 2024 19:55:43 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:5557d1011f8db6c8306114ebdb7f1caf2d969f06efc2b66ee34bb61b1fbb78a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.9 KB (944862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed25776500d61570cd6a6deb6a7b8e1855d3e69d44483c688c9a45185ca50ac6`

```dockerfile
```

-	Layers:
	-	`sha256:3af9a32ee0668a6af608337bcddbecc855029efd69933e9046f36682e84a2ad9`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 913.9 KB (913888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3370bfe3452a6e94532bb5823680a91661f51f027ee384f8ab7db7f969d8ea`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.10`

```console
$ docker pull influxdb@sha256:32418efff9e2e2efb99f0c93c78f2a2cd4f5316ec8c2983a64c9a53925f96fcc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.10` - linux; amd64

```console
$ docker pull influxdb@sha256:f5d5196210d9fb9acf485f18bdba66a0146b4ea1565005a6dc222e54c73f1390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168893012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903cf06eba30eddc4f08a676144fd3b03d2d0ac76bcdc42911bfad8bcca01b56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV GOSU_VER=1.16
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aafd1fd27c9676f57cb06374aa92c43541fcf93e2720bf3fa5d5bf45a284109`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 9.8 MB (9789031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61735b6533a48feec22deeb5e11cfc795f344ddd91e8cda094b5fbbfd789c6f2`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 5.8 MB (5820924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f27f427a2ce3808d8d9a09b50c52ff0933efa417b0bb9d281ec378def2d968`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf90975e867fab7ff0862159e12b24232ccebe662618746db3dc2d820506fbb`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 1.0 MB (1006363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55253b104f96a5e5ab0e9190cdbbf891d973155a6bd43a3e0f7dfe665e9b84b6`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 99.6 MB (99594050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b1de93c35668207e140c849313b99d49006c6f8fcc9cb1623a3a3915f10590`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 23.5 MB (23546404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd940528b08fc4347e306e9ba4c6be5cca185b598a9545f915c09fc97c2727a8`  
		Last Modified: Tue, 22 Oct 2024 19:55:48 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d55333cb59d840ce4b040a27abe0d24b5e44c9ec76107ad85193b5b3a086606`  
		Last Modified: Tue, 22 Oct 2024 19:55:48 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff84a72bb18b35058f8c116017714f3b4a543263aa2aa29ecddfca1b2519479`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:9cde691a07e51f352cc9ee6307c46b4a793741ba7a49f418037bba33d7ab9fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b20c55a4f47fd0d3aec51ead07b507cd683ae9693d265dd7e85159462b6d3df`

```dockerfile
```

-	Layers:
	-	`sha256:25056c70fdda68055fcfffd672a27976cc63407c18987e45e009d739d4e06e9c`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 2.8 MB (2849661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3057611b4133f25ca576be26bf2380aba98ff5136f48e234f51188f477b24de2`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 33.5 KB (33519 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:53c9749a685778bacdae9243980b8e5d0d0ef1ceb947ae41f91f50f621bdd595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162779131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bba075abbdb7b751d98b8f4ea79668db114d755eeb1e92bc60f42cb0086c961`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV GOSU_VER=1.16
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07320876b49207ad14955b1a31e4206a2a4153727413f4e8fcda5fd99916b4d4`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 9.6 MB (9587112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270e2f52b84341a01fd4a919bc929d7490c2caa4e34017d8376c18acf47acab0`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 5.5 MB (5463796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8837b8381563c809d09e25282b246ced163daf23d4c3c348813468b2323ad3a8`  
		Last Modified: Tue, 22 Oct 2024 19:55:08 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054534f2dd1b04e74b7e15809341ecf0eaf97c8736f86600f77b8e29157eb2ec`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d35e35d48ef6197e613fc0a0ff0dcc745084aa9439077bd2fc66add3b7885c6`  
		Last Modified: Tue, 22 Oct 2024 19:55:11 GMT  
		Size: 95.4 MB (95427909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb1b21f57ab00e3ecc4e16f96efeb63f8475fef567e59e85331bfb428ecf23f`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 22.2 MB (22197911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b88297b74f1c1c8700a853a735372741aadc94d4467ea21b2373a36ed465bf4`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37363f631d39bc3f49ae72bacaad18758d54157dbf4308a1a3f1b7aaa3eb4b89`  
		Last Modified: Tue, 22 Oct 2024 19:55:10 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013632725e99110127ab8f36dca492a8346ea517875e282a611b494b519e33d9`  
		Last Modified: Tue, 22 Oct 2024 19:55:10 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:684e07d361a121efaffb0611b94bb5bd45e4fbfd743f323029d3a52f633bd3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d6ca703457d4c565f9d48a20f346d8cfeaa0d9d18d394c948b0017c3e323fc`

```dockerfile
```

-	Layers:
	-	`sha256:f8b67510dcce1fc81e9b513aa534ce749c701750b139696527cbb54bb78e320f`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 2.8 MB (2848898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:514acbd511f7db84016cde5cc9c611926cde97d7b7733a7fa188ca8993a6d91b`  
		Last Modified: Tue, 22 Oct 2024 19:55:08 GMT  
		Size: 33.8 KB (33761 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.10-alpine`

```console
$ docker pull influxdb@sha256:407ed49d0b3e32362bbf9ee21740240893e62b9249a02397613a229652f64947
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:08d9e62b3e25b4ce5f55622654cd9979b9924aa0998a6c99923b75ae9fdda5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92442213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3badb18d31efb02e2268ff147fdea982e5dc8ee37b91e9010f5cf9488902a80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b052686eee98bc6eac2c55cdfc21b65703f40675b7e9a5ca8e363d4a8ab9db5a`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706bb39608a9fcc40a7863636b565e99300c14ebc8b01f8bee1bff576c3e346`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 9.7 MB (9652593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ba18c78730dca1ca920a72c5726b025a65089135c61e1e7a620d2b8471aaf4`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 5.8 MB (5820948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9991745f19f0cd45fc9ebc1c6befa3e94edb8a86cbe904216c1587e181bd2744`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd348b19e68ff1bdb0996ccae6df22753a67375d9593bf21fd727a06e11ec287`  
		Last Modified: Tue, 22 Oct 2024 19:55:32 GMT  
		Size: 49.8 MB (49790480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd1a635dcb59a7467f149e2c219346dc61ed6b816f1f0c8c50cde8c93b6b906`  
		Last Modified: Tue, 22 Oct 2024 19:55:32 GMT  
		Size: 23.5 MB (23546418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df577e715b6522db1f03aaf9c81977e416c84780057c41fb1eba468d8ec89224`  
		Last Modified: Tue, 22 Oct 2024 19:55:32 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aecd514cd25e9280e55610db5fc320bf07e9126415afe525e6f4d175627504`  
		Last Modified: Tue, 22 Oct 2024 19:55:33 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0853b6e6870bd74b624b56f40a38c3969af280d53dcac93cbc17ca967616e5fd`  
		Last Modified: Tue, 22 Oct 2024 19:55:33 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.10-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:874d5ec3cadb36a32bb07237b420a1f7dae1dc6b415d21edfca911a927fe74ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.4 KB (945413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878e61de24e216371cac057fae352502997f57115a18b176576275a51ad1fe16`

```dockerfile
```

-	Layers:
	-	`sha256:4c65636c7d529fd8d5be516ddf758b354823b8e602754c591ade112e0be41164`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 914.6 KB (914627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f494aa2572ef03fc09cba49db7a2ad4aa6a765e47a796f64ca5b1fc653c8d75`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.10-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:01d0fcd91674b394d26ef8f1eec9c475b7f403cf10257ebaed77ec26145856ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89244002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb389848654e8f0ea7f36e3dfb29bf5e97ff8c54e33400209ee70a5fb81ded1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deeb5bb87a9b047197ab047408d669771534ddd651ad86d0935717add352c29`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad71f843ccedd874c5468e97b4b7c17395262d7353e4ed6006aba08e18fae887`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 9.8 MB (9777142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a3e38e2ffb00f3e4786fdd01dd079eda34b3f65d8a05db74836f3739c0c8d1`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2def60e9aeb441cfc22ae4a5c007f86e41791863e6784828ec74390badf73a`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ea43a5fa5d50a03fbdbb5319d38071b43fd93879cfbb15f62721f491a347e4`  
		Last Modified: Tue, 22 Oct 2024 19:55:43 GMT  
		Size: 47.7 MB (47709532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047065b1bd569a1dee11f1813ce0051a11c7472c7d35e711609ecc2cbe7ad5d`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 22.2 MB (22197917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f9468215c53e8a896f9b934d83b0d0768f4e0e81441f0d8c5add921b1174d2`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a140ff0494c018fe34ddb0023fba7f95c40cf6201e1696fcec6901da350da6f0`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae45bb58db1b991a86bfe2c36cc8a55c4a9edcfbff715ebbab68907c6fc408`  
		Last Modified: Tue, 22 Oct 2024 19:55:43 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.10-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:5557d1011f8db6c8306114ebdb7f1caf2d969f06efc2b66ee34bb61b1fbb78a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.9 KB (944862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed25776500d61570cd6a6deb6a7b8e1855d3e69d44483c688c9a45185ca50ac6`

```dockerfile
```

-	Layers:
	-	`sha256:3af9a32ee0668a6af608337bcddbecc855029efd69933e9046f36682e84a2ad9`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 913.9 KB (913888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3370bfe3452a6e94532bb5823680a91661f51f027ee384f8ab7db7f969d8ea`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:407ed49d0b3e32362bbf9ee21740240893e62b9249a02397613a229652f64947
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:08d9e62b3e25b4ce5f55622654cd9979b9924aa0998a6c99923b75ae9fdda5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92442213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3badb18d31efb02e2268ff147fdea982e5dc8ee37b91e9010f5cf9488902a80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b052686eee98bc6eac2c55cdfc21b65703f40675b7e9a5ca8e363d4a8ab9db5a`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706bb39608a9fcc40a7863636b565e99300c14ebc8b01f8bee1bff576c3e346`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 9.7 MB (9652593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ba18c78730dca1ca920a72c5726b025a65089135c61e1e7a620d2b8471aaf4`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 5.8 MB (5820948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9991745f19f0cd45fc9ebc1c6befa3e94edb8a86cbe904216c1587e181bd2744`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd348b19e68ff1bdb0996ccae6df22753a67375d9593bf21fd727a06e11ec287`  
		Last Modified: Tue, 22 Oct 2024 19:55:32 GMT  
		Size: 49.8 MB (49790480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd1a635dcb59a7467f149e2c219346dc61ed6b816f1f0c8c50cde8c93b6b906`  
		Last Modified: Tue, 22 Oct 2024 19:55:32 GMT  
		Size: 23.5 MB (23546418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df577e715b6522db1f03aaf9c81977e416c84780057c41fb1eba468d8ec89224`  
		Last Modified: Tue, 22 Oct 2024 19:55:32 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aecd514cd25e9280e55610db5fc320bf07e9126415afe525e6f4d175627504`  
		Last Modified: Tue, 22 Oct 2024 19:55:33 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0853b6e6870bd74b624b56f40a38c3969af280d53dcac93cbc17ca967616e5fd`  
		Last Modified: Tue, 22 Oct 2024 19:55:33 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:874d5ec3cadb36a32bb07237b420a1f7dae1dc6b415d21edfca911a927fe74ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.4 KB (945413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878e61de24e216371cac057fae352502997f57115a18b176576275a51ad1fe16`

```dockerfile
```

-	Layers:
	-	`sha256:4c65636c7d529fd8d5be516ddf758b354823b8e602754c591ade112e0be41164`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 914.6 KB (914627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f494aa2572ef03fc09cba49db7a2ad4aa6a765e47a796f64ca5b1fc653c8d75`  
		Last Modified: Tue, 22 Oct 2024 19:55:31 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:01d0fcd91674b394d26ef8f1eec9c475b7f403cf10257ebaed77ec26145856ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89244002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb389848654e8f0ea7f36e3dfb29bf5e97ff8c54e33400209ee70a5fb81ded1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deeb5bb87a9b047197ab047408d669771534ddd651ad86d0935717add352c29`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad71f843ccedd874c5468e97b4b7c17395262d7353e4ed6006aba08e18fae887`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 9.8 MB (9777142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a3e38e2ffb00f3e4786fdd01dd079eda34b3f65d8a05db74836f3739c0c8d1`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2def60e9aeb441cfc22ae4a5c007f86e41791863e6784828ec74390badf73a`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ea43a5fa5d50a03fbdbb5319d38071b43fd93879cfbb15f62721f491a347e4`  
		Last Modified: Tue, 22 Oct 2024 19:55:43 GMT  
		Size: 47.7 MB (47709532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047065b1bd569a1dee11f1813ce0051a11c7472c7d35e711609ecc2cbe7ad5d`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 22.2 MB (22197917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f9468215c53e8a896f9b934d83b0d0768f4e0e81441f0d8c5add921b1174d2`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a140ff0494c018fe34ddb0023fba7f95c40cf6201e1696fcec6901da350da6f0`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae45bb58db1b991a86bfe2c36cc8a55c4a9edcfbff715ebbab68907c6fc408`  
		Last Modified: Tue, 22 Oct 2024 19:55:43 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:5557d1011f8db6c8306114ebdb7f1caf2d969f06efc2b66ee34bb61b1fbb78a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.9 KB (944862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed25776500d61570cd6a6deb6a7b8e1855d3e69d44483c688c9a45185ca50ac6`

```dockerfile
```

-	Layers:
	-	`sha256:3af9a32ee0668a6af608337bcddbecc855029efd69933e9046f36682e84a2ad9`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 913.9 KB (913888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3370bfe3452a6e94532bb5823680a91661f51f027ee384f8ab7db7f969d8ea`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:32418efff9e2e2efb99f0c93c78f2a2cd4f5316ec8c2983a64c9a53925f96fcc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:f5d5196210d9fb9acf485f18bdba66a0146b4ea1565005a6dc222e54c73f1390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168893012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903cf06eba30eddc4f08a676144fd3b03d2d0ac76bcdc42911bfad8bcca01b56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV GOSU_VER=1.16
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aafd1fd27c9676f57cb06374aa92c43541fcf93e2720bf3fa5d5bf45a284109`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 9.8 MB (9789031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61735b6533a48feec22deeb5e11cfc795f344ddd91e8cda094b5fbbfd789c6f2`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 5.8 MB (5820924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f27f427a2ce3808d8d9a09b50c52ff0933efa417b0bb9d281ec378def2d968`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf90975e867fab7ff0862159e12b24232ccebe662618746db3dc2d820506fbb`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 1.0 MB (1006363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55253b104f96a5e5ab0e9190cdbbf891d973155a6bd43a3e0f7dfe665e9b84b6`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 99.6 MB (99594050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b1de93c35668207e140c849313b99d49006c6f8fcc9cb1623a3a3915f10590`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 23.5 MB (23546404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd940528b08fc4347e306e9ba4c6be5cca185b598a9545f915c09fc97c2727a8`  
		Last Modified: Tue, 22 Oct 2024 19:55:48 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d55333cb59d840ce4b040a27abe0d24b5e44c9ec76107ad85193b5b3a086606`  
		Last Modified: Tue, 22 Oct 2024 19:55:48 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff84a72bb18b35058f8c116017714f3b4a543263aa2aa29ecddfca1b2519479`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:9cde691a07e51f352cc9ee6307c46b4a793741ba7a49f418037bba33d7ab9fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b20c55a4f47fd0d3aec51ead07b507cd683ae9693d265dd7e85159462b6d3df`

```dockerfile
```

-	Layers:
	-	`sha256:25056c70fdda68055fcfffd672a27976cc63407c18987e45e009d739d4e06e9c`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 2.8 MB (2849661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3057611b4133f25ca576be26bf2380aba98ff5136f48e234f51188f477b24de2`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 33.5 KB (33519 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:53c9749a685778bacdae9243980b8e5d0d0ef1ceb947ae41f91f50f621bdd595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162779131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bba075abbdb7b751d98b8f4ea79668db114d755eeb1e92bc60f42cb0086c961`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV GOSU_VER=1.16
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07320876b49207ad14955b1a31e4206a2a4153727413f4e8fcda5fd99916b4d4`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 9.6 MB (9587112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270e2f52b84341a01fd4a919bc929d7490c2caa4e34017d8376c18acf47acab0`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 5.5 MB (5463796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8837b8381563c809d09e25282b246ced163daf23d4c3c348813468b2323ad3a8`  
		Last Modified: Tue, 22 Oct 2024 19:55:08 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054534f2dd1b04e74b7e15809341ecf0eaf97c8736f86600f77b8e29157eb2ec`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d35e35d48ef6197e613fc0a0ff0dcc745084aa9439077bd2fc66add3b7885c6`  
		Last Modified: Tue, 22 Oct 2024 19:55:11 GMT  
		Size: 95.4 MB (95427909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb1b21f57ab00e3ecc4e16f96efeb63f8475fef567e59e85331bfb428ecf23f`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 22.2 MB (22197911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b88297b74f1c1c8700a853a735372741aadc94d4467ea21b2373a36ed465bf4`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37363f631d39bc3f49ae72bacaad18758d54157dbf4308a1a3f1b7aaa3eb4b89`  
		Last Modified: Tue, 22 Oct 2024 19:55:10 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013632725e99110127ab8f36dca492a8346ea517875e282a611b494b519e33d9`  
		Last Modified: Tue, 22 Oct 2024 19:55:10 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:684e07d361a121efaffb0611b94bb5bd45e4fbfd743f323029d3a52f633bd3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d6ca703457d4c565f9d48a20f346d8cfeaa0d9d18d394c948b0017c3e323fc`

```dockerfile
```

-	Layers:
	-	`sha256:f8b67510dcce1fc81e9b513aa534ce749c701750b139696527cbb54bb78e320f`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 2.8 MB (2848898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:514acbd511f7db84016cde5cc9c611926cde97d7b7733a7fa188ca8993a6d91b`  
		Last Modified: Tue, 22 Oct 2024 19:55:08 GMT  
		Size: 33.8 KB (33761 bytes)  
		MIME: application/vnd.in-toto+json
