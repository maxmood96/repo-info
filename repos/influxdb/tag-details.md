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
-	[`influxdb:1.11-data`](#influxdb111-data)
-	[`influxdb:1.11-data-alpine`](#influxdb111-data-alpine)
-	[`influxdb:1.11-meta`](#influxdb111-meta)
-	[`influxdb:1.11-meta-alpine`](#influxdb111-meta-alpine)
-	[`influxdb:1.11.7-data`](#influxdb1117-data)
-	[`influxdb:1.11.7-data-alpine`](#influxdb1117-data-alpine)
-	[`influxdb:1.11.7-meta`](#influxdb1117-meta)
-	[`influxdb:1.11.7-meta-alpine`](#influxdb1117-meta-alpine)
-	[`influxdb:1.8`](#influxdb18)
-	[`influxdb:1.8-alpine`](#influxdb18-alpine)
-	[`influxdb:1.8.10`](#influxdb1810)
-	[`influxdb:1.8.10-alpine`](#influxdb1810-alpine)
-	[`influxdb:1.9-data`](#influxdb19-data)
-	[`influxdb:1.9-data-alpine`](#influxdb19-data-alpine)
-	[`influxdb:1.9-meta`](#influxdb19-meta)
-	[`influxdb:1.9-meta-alpine`](#influxdb19-meta-alpine)
-	[`influxdb:1.9.13-data`](#influxdb1913-data)
-	[`influxdb:1.9.13-data-alpine`](#influxdb1913-data-alpine)
-	[`influxdb:1.9.13-meta`](#influxdb1913-meta)
-	[`influxdb:1.9.13-meta-alpine`](#influxdb1913-meta-alpine)
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

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:c1287fe0eb516ea5a27f45545dd9bd80d8c413655ec3d1d90cb8b71ea3d1b8ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:10ff9d7be60466f6c4df6a5aec82897a057da37ca59c5af34dc27fa71efc244c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114734343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24e1600d560ec66513b376f87e33c6b3a26b76435156fb49d79d99e03df19df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
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
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9901592dcf742da657dc993f7f811f86eb262f64c1a7a3898d33433f964b26e`  
		Last Modified: Sat, 19 Oct 2024 02:09:08 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60167bbcb9f949543985d2ae5e12892c0427697d4444d131912d4741b23b025`  
		Last Modified: Sat, 19 Oct 2024 02:09:09 GMT  
		Size: 41.1 MB (41124394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602f45f13c4fc7c34e68cf0ccab4c79c9dcd41509a1d74210ccaa5b94ccc438f`  
		Last Modified: Sat, 19 Oct 2024 02:09:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2264d2ff910b67333d76b8d9773207c2a1fadd72260eacb24c1aaa0e6b68adc7`  
		Last Modified: Sat, 19 Oct 2024 02:09:07 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8940cfc39177e2a9294a30e8d2153046e6ecece90e6faaf1202a450cb6d9ea26`  
		Last Modified: Sat, 19 Oct 2024 02:09:07 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:0e4ea76c7b3c57d10d3e089c25fef242aff42128be8796f5770b03072f3b67f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2369c8d065ceedf448a2d12cb70325803f4a653240b987ef160ae92d2d48a735`

```dockerfile
```

-	Layers:
	-	`sha256:31203311f9710de0cc4f8fd7a2110c235791968444c9c002466465add305e6b5`  
		Last Modified: Sat, 19 Oct 2024 02:09:08 GMT  
		Size: 4.5 MB (4516962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b205ea1ba3ae3b65fd4a0f3ff196027b75b7bd0bed87e002faa9e672b0513839`  
		Last Modified: Sat, 19 Oct 2024 02:09:08 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:793f886a0f196db5905fe5c032ad3ef68d70ad98c34c6637ea21bce6229a8ddf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:573fd78175f9c2b67d5134f99e038cb635825904582cebeb099e80587bc00159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45917646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ed4bbecfe834f3c3e8b5c61751972611866f1e7ae3deafc324207bd89a86f6`
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
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
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
	-	`sha256:857ecb64e1c45d46a8c34612f7a82dff76a2e2dc69ad314d38fb25ecbefb8935`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d259500ab08714fd23f323e03db9b6667d134caa6125bc719b389b715b0d72`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 1.2 MB (1223697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5ed4398154e144152fceb43093803a978b1642da200499812971bf123cdcfe`  
		Last Modified: Fri, 06 Sep 2024 23:21:31 GMT  
		Size: 41.1 MB (41068088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a6154e867ed06e7522e5f54847c2eae97d713e8902c5d37b425c92b5e3c45b`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d38d399e914c79804eebd54b4a7d99674b1e1d40f47a7bc9152a6ed3b0bdbf`  
		Last Modified: Fri, 06 Sep 2024 23:21:31 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464862829bd851eba89202a10fbcf1648268f3bc281488f81516fd88e9ec75b4`  
		Last Modified: Fri, 06 Sep 2024 23:21:31 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:131870e981caa20de1edd37280d24b40a7fe3b95cee55d955fa15b1af30a3e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.0 KB (769006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6649dc24824db616e8fc760ca5599e1218515de43eb8a6568dbdc6ad8cdd652c`

```dockerfile
```

-	Layers:
	-	`sha256:d1e882cf6a38dfc88429d43a01e90cd5f85aa265dc0f421c764a7267f6d54e42`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 752.6 KB (752582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80efadee668de3a90c9d62413a69233f4a279b4f423beb1d10924af871ad913b`  
		Last Modified: Fri, 06 Sep 2024 23:21:30 GMT  
		Size: 16.4 KB (16424 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:101cbc00e2a3eb72d8e5b3caf43af60473744a511972c6d8d31c812d8ca7d4f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:f65cc1df0728c7453457cec0c9a7b4e7e605af83192fc11d6122c31bf47599ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93401711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90691c2683477e8d955ee2c5d9c315901ea4f3f0d8b4154ac677943608d8256`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
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
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc77c0403007fcec96e307aede0c01a9541d4377cb2e459e99f8d7d3ddfcbca`  
		Last Modified: Sat, 19 Oct 2024 02:09:06 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8a82e8b239af863eb5e1533656f22e3e136b4141e9f257246b0deb5b541e5d`  
		Last Modified: Sat, 19 Oct 2024 02:09:07 GMT  
		Size: 19.8 MB (19792949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873607894aac0783d89707019f835ebbaad18bb75a63642bced3fb2a2897dd5c`  
		Last Modified: Sat, 19 Oct 2024 02:09:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9015644a0c987d47808ebd4b27662faac2fd814b235a8826d877e29066af7f`  
		Last Modified: Sat, 19 Oct 2024 02:09:06 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:2301d0e9df88ab46b538daeb1e31585cc724a8a1bd62e89bf507e8cd34711e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4454781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64cf79382900eaa8cc13030f44d96faaf2745db422634d3f4a16616c37336a2`

```dockerfile
```

-	Layers:
	-	`sha256:93801a933e7c9b4473845a2057646fb61bb920aa2d7262b2df1f3ae28bb81b64`  
		Last Modified: Sat, 19 Oct 2024 02:09:06 GMT  
		Size: 4.4 MB (4441714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52e3273cc3ea4aa808e20bb6fbe8740fbc6b8ee0411548fbbb7c5930b60286a5`  
		Last Modified: Sat, 19 Oct 2024 02:09:06 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:96bd9ec295c6c0ab62749a038cdc13ad5082792a73d41ded0f2d21e35fe9f21f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a56a53388024c062e4f3ee08114cf6986b61f6201e5d8373384ec217117e903b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24584604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500aabb8f592d298e1e576c5317e23c7059936093841aea87577a95931515648`
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
ENV INFLUXDB_VERSION=1.11.6-c1.11.6
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
	-	`sha256:078166243ebe0c2b9c91a2f7e164076218c7716b68301080fac2f19f177dd096`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1798891eeacb4169638b5166c9e8cac1a921167b71619feef52252cbc89c4dda`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 1.2 MB (1223696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef37378c1a1c94f9d7791528dd34dc79702e4799fd548e2bfe6b9ca7b343955`  
		Last Modified: Fri, 06 Sep 2024 23:21:36 GMT  
		Size: 19.7 MB (19736254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8e176e0b983dd08fc989b466f8cbf8fb62e7e9c6c212c76ea7bd08b5118414`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227ebad2c15b696728c9d1fa05d604f31709b9ddfecaa3e9cf9a0b6aedce32e3`  
		Last Modified: Fri, 06 Sep 2024 23:21:36 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3cb8c03d383d8b03f6bda40519a6a1d6d8fce3d357ca1193992ccbca30832abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (693016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5562508b37e0ac45d12bf7f861aee0c9b278146b238c0c07af053d8dc44277de`

```dockerfile
```

-	Layers:
	-	`sha256:8733ae4a661f1f95273f1984aa60368d9b1a0c7d2e9affdbce5ab38fb7aa9192`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 678.2 KB (678227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42d685a470a69c05014558d05c4b43b664c5d30866a83c2a64b167a2204ff9bf`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 14.8 KB (14789 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.7-data`

```console
$ docker pull influxdb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `influxdb:1.11.7-data-alpine`

```console
$ docker pull influxdb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `influxdb:1.11.7-meta`

```console
$ docker pull influxdb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `influxdb:1.11.7-meta-alpine`

```console
$ docker pull influxdb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:299ebda2c7e308dbef42e26ac9b8fd1d9b3bcb8a0aee80c6509aa0219c1d0290
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:03ba655e0c8b4d60dc8c74d437c4f441c5e7934bfaa8ea4545edf1274c8eb223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125731805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899f8d89099b0603c025fec86b4034564ce92dab9e3702d002eb1c3da958a842`
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
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
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
	-	`sha256:7e6ef86bdb80e3cf9c634010be2b8577031031e1cebc985aebace4104688166f`  
		Last Modified: Sat, 19 Oct 2024 02:08:59 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0a8853fbab256b71e3f5b97fc099b410207ec0d7b746a391373149f10af39c`  
		Last Modified: Sat, 19 Oct 2024 02:09:00 GMT  
		Size: 54.9 MB (54885386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734d2edced1bce0dfd14e3f6ded33bdcaa051d866d5a4a45930b212c39ba7132`  
		Last Modified: Sat, 19 Oct 2024 02:08:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00843a9c58b8ecde858a4dea591eb706ace1dc15f134e71abd3b10a044708c7`  
		Last Modified: Sat, 19 Oct 2024 02:08:59 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b9c8d60da9f3e1fe9896f0a64b7c37c1445446a5e8d5e9b799061e65962f58`  
		Last Modified: Sat, 19 Oct 2024 02:09:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:5590451c24a9fa6e6fad3c432a9000266f52b1a950cd16626ebf40afc7b0e471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18212086e5758c8e24781a1ca9873d91ad898f2a9edfa7905f12f0caf9dd1c4c`

```dockerfile
```

-	Layers:
	-	`sha256:a2a8b002219ae5df7cf826603e73345d7de269e0cfd653ab04c44d3503491672`  
		Last Modified: Sat, 19 Oct 2024 02:09:00 GMT  
		Size: 4.5 MB (4506158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77222241a1724ca08de0648e9f9512c072950ce07b26f39cadee9b82c03967ec`  
		Last Modified: Sat, 19 Oct 2024 02:08:59 GMT  
		Size: 15.6 KB (15596 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:5b3ed6d93e1e2236940d44f883422fbdb74fb9fde6f448e58819fb7406ec8bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116735686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f7678f4e967cf0f943dafa1283ebebb17758fe572b0dcba8b328d861ed911c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
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
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c89c320deb84b8976dcdba7a2ff34ebb6b9fcf548eb59083f8718717ec39c9`  
		Last Modified: Sat, 19 Oct 2024 07:09:11 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef2be25f1a4a7b0a447193d9b20aba2902ecee72993fac969fb7e5f6017906b`  
		Last Modified: Sat, 19 Oct 2024 07:09:13 GMT  
		Size: 51.6 MB (51612907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b8b497c8af37b2400b55e3eb2273c348bbe0faf570377016910327a27e9eb7`  
		Last Modified: Sat, 19 Oct 2024 07:09:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962a772aaf7cec1c84a3d3d50b9427d71624212d8d52578c67ffb4d9499cf25f`  
		Last Modified: Sat, 19 Oct 2024 07:09:12 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a7c0c70f77a940001c55c50fa6246ab83037b6fe0aba906d194cea243d9aca`  
		Last Modified: Sat, 19 Oct 2024 07:09:12 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:9ef26a0fe48deb54696dd790ab0ca2bbe8dfb3dcf8984e322c06f4168c611dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37deedd3a984386ffbe7c2547865d3793037a63440309366c95444f0a9c0395b`

```dockerfile
```

-	Layers:
	-	`sha256:7460e13d907056a96e50c55b3431931e5ce9e4996a9b41b60431cb10822bee96`  
		Last Modified: Sat, 19 Oct 2024 07:09:12 GMT  
		Size: 4.5 MB (4507792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64f9e604678dd45fcb7678b2a2287704f042c92ce720db8c21b5b827ef408d89`  
		Last Modified: Sat, 19 Oct 2024 07:09:11 GMT  
		Size: 15.7 KB (15705 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:93ee9cd349882c18e69980d85fe4d2d0667c9dcbdd611c019bd1f7816884aa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120716125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe366b9a9af62c1d199e01e5898d650011bc52fc18be481851ff4f236aff284`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71efbbe32e44303a3305fcc39de75a46e033b4ffd4176944c7e3c7eb7063148a`  
		Last Modified: Sat, 19 Oct 2024 05:53:52 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822229d5942c09beb2b6b9cca4f78a6f49f33025a1e30feea735942abb7fb6a5`  
		Last Modified: Sat, 19 Oct 2024 05:53:53 GMT  
		Size: 51.2 MB (51229938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa0738214bb9b9c99a4687a36d2f88b1da7bee68cfb099439210663bc99d7d6`  
		Last Modified: Sat, 19 Oct 2024 05:53:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54df75daf565fb6d2ed179ea7b170f9692df1301c9c1234823572e780a758f19`  
		Last Modified: Sat, 19 Oct 2024 05:53:52 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ace858e7d3c6b17074be16ab9448e1241e907bef8fa72a4d53144e8a7f065a`  
		Last Modified: Sat, 19 Oct 2024 05:53:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:7e495ef5f39c743495a977ecaf57e4b97be53f9726e715caadd7c2e881280525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551cfeb7901955b807705717326d7874b2a38f14a23ba4c0e443e9320de4851c`

```dockerfile
```

-	Layers:
	-	`sha256:9920cb1c0bd2feed5db9180d16e53da647f11f69c8df5d4f6ce793ce4611e496`  
		Last Modified: Sat, 19 Oct 2024 05:53:52 GMT  
		Size: 4.5 MB (4505770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ed315d91596c34aa9ebecf24b40e9d455c147b729865decb2161b618ced290`  
		Last Modified: Sat, 19 Oct 2024 05:53:52 GMT  
		Size: 15.7 KB (15727 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:2601e27d6b7eac276017d7ea48d2685d52639cea974744b5877924376283a4cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:323bec748932cf3049bcd0ad3df03da7a85743014f37c5c06390d3dd090d5027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59520385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c14632645a8e98cabcfa629d7f97d199afdc7b0435d24fe7c0bffcbd0925fe6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a63e70873dd8d18fc4e609edbcd780bf91673580b44f6778efc5cd01e91416`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3019afc3f13df4911e2077ec99e0d88ca3cea7acca75646748dc4448363fdc6`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 1.5 MB (1479482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40cfe8e6bcbeae6388a3e7d07db6cd1394e73cdf54ce683edbb1b7c3671a17c`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 54.6 MB (54646714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784f4de03565d8b1d250901b03046846f5c1d470c593bd5c3659ace47f783ede`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736622afe4eb3db6ea76fd89d7ac1d5e77d5880030d85231d501cfcbbf109518`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85d23128f7bc1806470e05b177060a051b55e1f209ee6fbdc04ff31e2077651`  
		Last Modified: Fri, 06 Sep 2024 23:21:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bb8c66f3e48bbdf4bf837fcc1ee9679803fbe889db56efdf5357a718e9e0949c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1004063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67740208b251a99deebeae23d6c8d13b17326e8cca04cbb249627ac8460a4277`

```dockerfile
```

-	Layers:
	-	`sha256:a9272376189bcad2f11697903cbc6eccc780943ecc0445d25c1c98feb509eaf7`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 986.7 KB (986701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58257e0baabc8dbe52d193e3864f126406b8a8ef94fcc42024004fe91365e44f`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 17.4 KB (17362 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8.10`

```console
$ docker pull influxdb@sha256:299ebda2c7e308dbef42e26ac9b8fd1d9b3bcb8a0aee80c6509aa0219c1d0290
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.8.10` - linux; amd64

```console
$ docker pull influxdb@sha256:03ba655e0c8b4d60dc8c74d437c4f441c5e7934bfaa8ea4545edf1274c8eb223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125731805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899f8d89099b0603c025fec86b4034564ce92dab9e3702d002eb1c3da958a842`
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
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
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
	-	`sha256:7e6ef86bdb80e3cf9c634010be2b8577031031e1cebc985aebace4104688166f`  
		Last Modified: Sat, 19 Oct 2024 02:08:59 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0a8853fbab256b71e3f5b97fc099b410207ec0d7b746a391373149f10af39c`  
		Last Modified: Sat, 19 Oct 2024 02:09:00 GMT  
		Size: 54.9 MB (54885386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734d2edced1bce0dfd14e3f6ded33bdcaa051d866d5a4a45930b212c39ba7132`  
		Last Modified: Sat, 19 Oct 2024 02:08:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00843a9c58b8ecde858a4dea591eb706ace1dc15f134e71abd3b10a044708c7`  
		Last Modified: Sat, 19 Oct 2024 02:08:59 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b9c8d60da9f3e1fe9896f0a64b7c37c1445446a5e8d5e9b799061e65962f58`  
		Last Modified: Sat, 19 Oct 2024 02:09:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:5590451c24a9fa6e6fad3c432a9000266f52b1a950cd16626ebf40afc7b0e471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18212086e5758c8e24781a1ca9873d91ad898f2a9edfa7905f12f0caf9dd1c4c`

```dockerfile
```

-	Layers:
	-	`sha256:a2a8b002219ae5df7cf826603e73345d7de269e0cfd653ab04c44d3503491672`  
		Last Modified: Sat, 19 Oct 2024 02:09:00 GMT  
		Size: 4.5 MB (4506158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77222241a1724ca08de0648e9f9512c072950ce07b26f39cadee9b82c03967ec`  
		Last Modified: Sat, 19 Oct 2024 02:08:59 GMT  
		Size: 15.6 KB (15596 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:5b3ed6d93e1e2236940d44f883422fbdb74fb9fde6f448e58819fb7406ec8bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116735686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f7678f4e967cf0f943dafa1283ebebb17758fe572b0dcba8b328d861ed911c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
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
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c89c320deb84b8976dcdba7a2ff34ebb6b9fcf548eb59083f8718717ec39c9`  
		Last Modified: Sat, 19 Oct 2024 07:09:11 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef2be25f1a4a7b0a447193d9b20aba2902ecee72993fac969fb7e5f6017906b`  
		Last Modified: Sat, 19 Oct 2024 07:09:13 GMT  
		Size: 51.6 MB (51612907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b8b497c8af37b2400b55e3eb2273c348bbe0faf570377016910327a27e9eb7`  
		Last Modified: Sat, 19 Oct 2024 07:09:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962a772aaf7cec1c84a3d3d50b9427d71624212d8d52578c67ffb4d9499cf25f`  
		Last Modified: Sat, 19 Oct 2024 07:09:12 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a7c0c70f77a940001c55c50fa6246ab83037b6fe0aba906d194cea243d9aca`  
		Last Modified: Sat, 19 Oct 2024 07:09:12 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:9ef26a0fe48deb54696dd790ab0ca2bbe8dfb3dcf8984e322c06f4168c611dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37deedd3a984386ffbe7c2547865d3793037a63440309366c95444f0a9c0395b`

```dockerfile
```

-	Layers:
	-	`sha256:7460e13d907056a96e50c55b3431931e5ce9e4996a9b41b60431cb10822bee96`  
		Last Modified: Sat, 19 Oct 2024 07:09:12 GMT  
		Size: 4.5 MB (4507792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64f9e604678dd45fcb7678b2a2287704f042c92ce720db8c21b5b827ef408d89`  
		Last Modified: Sat, 19 Oct 2024 07:09:11 GMT  
		Size: 15.7 KB (15705 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:93ee9cd349882c18e69980d85fe4d2d0667c9dcbdd611c019bd1f7816884aa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120716125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe366b9a9af62c1d199e01e5898d650011bc52fc18be481851ff4f236aff284`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb* # buildkit
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71efbbe32e44303a3305fcc39de75a46e033b4ffd4176944c7e3c7eb7063148a`  
		Last Modified: Sat, 19 Oct 2024 05:53:52 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822229d5942c09beb2b6b9cca4f78a6f49f33025a1e30feea735942abb7fb6a5`  
		Last Modified: Sat, 19 Oct 2024 05:53:53 GMT  
		Size: 51.2 MB (51229938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa0738214bb9b9c99a4687a36d2f88b1da7bee68cfb099439210663bc99d7d6`  
		Last Modified: Sat, 19 Oct 2024 05:53:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54df75daf565fb6d2ed179ea7b170f9692df1301c9c1234823572e780a758f19`  
		Last Modified: Sat, 19 Oct 2024 05:53:52 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ace858e7d3c6b17074be16ab9448e1241e907bef8fa72a4d53144e8a7f065a`  
		Last Modified: Sat, 19 Oct 2024 05:53:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:7e495ef5f39c743495a977ecaf57e4b97be53f9726e715caadd7c2e881280525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551cfeb7901955b807705717326d7874b2a38f14a23ba4c0e443e9320de4851c`

```dockerfile
```

-	Layers:
	-	`sha256:9920cb1c0bd2feed5db9180d16e53da647f11f69c8df5d4f6ce793ce4611e496`  
		Last Modified: Sat, 19 Oct 2024 05:53:52 GMT  
		Size: 4.5 MB (4505770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ed315d91596c34aa9ebecf24b40e9d455c147b729865decb2161b618ced290`  
		Last Modified: Sat, 19 Oct 2024 05:53:52 GMT  
		Size: 15.7 KB (15727 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.8.10-alpine`

```console
$ docker pull influxdb@sha256:2601e27d6b7eac276017d7ea48d2685d52639cea974744b5877924376283a4cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.8.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:323bec748932cf3049bcd0ad3df03da7a85743014f37c5c06390d3dd090d5027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59520385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c14632645a8e98cabcfa629d7f97d199afdc7b0435d24fe7c0bffcbd0925fe6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.8.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a63e70873dd8d18fc4e609edbcd780bf91673580b44f6778efc5cd01e91416`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3019afc3f13df4911e2077ec99e0d88ca3cea7acca75646748dc4448363fdc6`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 1.5 MB (1479482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40cfe8e6bcbeae6388a3e7d07db6cd1394e73cdf54ce683edbb1b7c3671a17c`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 54.6 MB (54646714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784f4de03565d8b1d250901b03046846f5c1d470c593bd5c3659ace47f783ede`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736622afe4eb3db6ea76fd89d7ac1d5e77d5880030d85231d501cfcbbf109518`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85d23128f7bc1806470e05b177060a051b55e1f209ee6fbdc04ff31e2077651`  
		Last Modified: Fri, 06 Sep 2024 23:21:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.8.10-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bb8c66f3e48bbdf4bf837fcc1ee9679803fbe889db56efdf5357a718e9e0949c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1004063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67740208b251a99deebeae23d6c8d13b17326e8cca04cbb249627ac8460a4277`

```dockerfile
```

-	Layers:
	-	`sha256:a9272376189bcad2f11697903cbc6eccc780943ecc0445d25c1c98feb509eaf7`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 986.7 KB (986701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58257e0baabc8dbe52d193e3864f126406b8a8ef94fcc42024004fe91365e44f`  
		Last Modified: Fri, 06 Sep 2024 23:21:20 GMT  
		Size: 17.4 KB (17362 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-data`

```console
$ docker pull influxdb@sha256:d402d9b65bd3e85768c36e331f814792566216516419609c4951e55588cbeab6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a17cd2201b6b833623a25da9a1e7b6e0c130e14efb4957feaaa5f659c9342af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104135433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e11da574745bbd18c09ebbbf43d1bdd55a253714b3769e129fe0e0e28a1787`
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
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
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
	-	`sha256:7d49783477707d4b2325b918d71b6325a0ea5dc9bce5775beaff74204fad8682`  
		Last Modified: Sat, 19 Oct 2024 02:09:06 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b95169afc760ba590b871ab304202a3ebaa667509c466a1aa496fdcbe737eeb`  
		Last Modified: Sat, 19 Oct 2024 02:09:07 GMT  
		Size: 33.3 MB (33288962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d95218d2da28d04d81c234b738de8dbb1ebb995e5e0d79ac9a15cd0141bf467`  
		Last Modified: Sat, 19 Oct 2024 02:09:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2264d2ff910b67333d76b8d9773207c2a1fadd72260eacb24c1aaa0e6b68adc7`  
		Last Modified: Sat, 19 Oct 2024 02:09:07 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8940cfc39177e2a9294a30e8d2153046e6ecece90e6faaf1202a450cb6d9ea26`  
		Last Modified: Sat, 19 Oct 2024 02:09:07 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:adcce1b6d87db7e3e86f252bb29b53eaa84144a6bac068a4f652cdc67eecbb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4647714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f23fc0888008bf76e6fdc127c8cc79130ba16c90c30a98cb10877273a7b2e9`

```dockerfile
```

-	Layers:
	-	`sha256:dcddeb1bacaee184c5d3c7163250eb28d79b834d5076cd3a80fdabda4fc4c619`  
		Last Modified: Sat, 19 Oct 2024 02:09:07 GMT  
		Size: 4.6 MB (4633039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcff244de46f780a8df7b4db4e66969d004dd7763dd1fe2d8a7f490097b69fe3`  
		Last Modified: Sat, 19 Oct 2024 02:09:06 GMT  
		Size: 14.7 KB (14675 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-data-alpine`

```console
$ docker pull influxdb@sha256:8e4766170552f7235b1c95b807219c581220679cfff432ac822c633df62bc67d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2be9c69c4dcd5b5ae85762696e710b68b9274a3ffece838c55f1c4dfd476720e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38122546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d021f63e78c0dcaf4f0c4843c08277496a2f3fa39a22064e24859434ce7570a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc88cdf71faaf02dcebd3cdcc8ce57a3b308c18e1848992c3aa12889d68a7301`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f1954a31a733b8d976bc7f913379f93944a904187dada2925e7b3cdbabc0f5`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 1.5 MB (1479490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea04e3b2c5bbeec39091ab366a332265cf6a1fcd0a00a3d955795bfbdefdf86b`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 33.2 MB (33248810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31752a5b6441ca3f6fbf58a13a9df69554b08cd5a0a98b42b9af86bd91bae722`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e28722e5f3c56298697a4b05f52f60035c8581bfc3598ce2fcf490278b3e4fa`  
		Last Modified: Fri, 06 Sep 2024 23:21:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a27e41d4bb82b0a46cee7d7b7054ea092e52fb02cf0c3620e2cdf32e0038ca`  
		Last Modified: Fri, 06 Sep 2024 23:21:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:52997d7d8ef387e2e2bf5593c589b466eae768552b84efa1547cdb8ce44616e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1137829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baab96e09494545e50ecde071d196cb1a9b8250cb52b0d169702e169b2c85bb1`

```dockerfile
```

-	Layers:
	-	`sha256:1781d7e34c0831e0d91185e04c6d0e841144d3fdfcfe61991f8e8c86ba334130`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 1.1 MB (1121383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1d27a2c65fe763ea61971a95d715655cd32f3bcf319da8dabb4f1900c2e7056`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 16.4 KB (16446 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-meta`

```console
$ docker pull influxdb@sha256:0b12d867797874998ce544bb011dc633fb75c8899fca47f0ff9a246f8b9d9a30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c62fd9cf4f8989fe6de61393e6a47bac445f2d3b2d88cfff9afc37eb1c7e2feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83614618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046720e40a7ffc852d231dcc274e2df95828bf26e440c1082e29adbb43e143b9`
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
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb* # buildkit
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
	-	`sha256:44177e4886f7b216e3082e1da60e6d82848c622f46a53a9ed933dba52a1426f0`  
		Last Modified: Sat, 19 Oct 2024 02:09:10 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0585491307193b87cbf3dbe3c4e401f798d5be4cf362b38c3619d6a4f0127fc`  
		Last Modified: Sat, 19 Oct 2024 02:09:11 GMT  
		Size: 12.8 MB (12769365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f84edd12eb3d695d601eb18d7338912e0729c578e1643bf817c6da8a7b2b2c`  
		Last Modified: Sat, 19 Oct 2024 02:09:10 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60fe16d5196be0ced0631ee5eb99a1cdad0d437779872ee5a5d98dafe39d058`  
		Last Modified: Sat, 19 Oct 2024 02:09:10 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:ede9eb5b8b1efe8e5369ce181615ccaf28355559fb41cc45ed3b532085d7ec03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4581906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23425e5904dc79952c381d0415976bc3b173f5f0f2047b7f5ef9b006d2c10e53`

```dockerfile
```

-	Layers:
	-	`sha256:90c42b7d85376fd8ebfe9d4902f7f9925f53b6608f667ba7bf6034fe8735d929`  
		Last Modified: Sat, 19 Oct 2024 02:09:10 GMT  
		Size: 4.6 MB (4568872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cefd7ecd6ebca3486567d4c00570a5f30eefc83cbd1d0bb8439d7aba14d00dd`  
		Last Modified: Sat, 19 Oct 2024 02:09:10 GMT  
		Size: 13.0 KB (13034 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9-meta-alpine`

```console
$ docker pull influxdb@sha256:4d3a9c68cfc5211e9079595580408c93af827777d33bf0f66a34a87c0966a03f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e4d7f35c0a96a009bc919f98118cf471c253e54c5dd47ff14ab4fd80b86e4c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17569067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77bc62f618fb464838b1d92de778a70e3072262f06ecd84f96c4073d5898eb3`
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
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:020562199c64aad524deae5d3ab9ce90e8b6cd8a2f2efa68dc89be44c4bbbcb0`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164109d9ed866529603429a063011bb370e035ba2582d27646c7d720dc703e70`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 1.2 MB (1223701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2001df372492d0f10ab280222c05f3d766032e54ebdbb87c17e1c55489fbcf8`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 12.7 MB (12720713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680dcab1180b67227ca80095a9b3b636c0182c7d8df7c911b8b8f2a097e3456`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8044a8f410b1af2cb55de0e9463e0da9482b826ed89980872400a29373ad7145`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e4ec93149fe8e573bc5b6cdfbd1476c21c497f6b34a54badf6e7addaf3b882ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (692992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a56585d872141e680b91773c695f6dc007ef5b4ade58ae79965a0d351dcd95`

```dockerfile
```

-	Layers:
	-	`sha256:b6d1ec9d01fb7b59c9c9d2c5998b0930a3b42d3648164bb5573ae0fc0cf64fa8`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 678.2 KB (678179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a4e5534447245d871a73fce3f69e717a88c925647a19d9bfabd1b57d1b5e69`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 14.8 KB (14813 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-data`

```console
$ docker pull influxdb@sha256:d402d9b65bd3e85768c36e331f814792566216516419609c4951e55588cbeab6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a17cd2201b6b833623a25da9a1e7b6e0c130e14efb4957feaaa5f659c9342af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104135433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e11da574745bbd18c09ebbbf43d1bdd55a253714b3769e129fe0e0e28a1787`
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
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb* # buildkit
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
	-	`sha256:7d49783477707d4b2325b918d71b6325a0ea5dc9bce5775beaff74204fad8682`  
		Last Modified: Sat, 19 Oct 2024 02:09:06 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b95169afc760ba590b871ab304202a3ebaa667509c466a1aa496fdcbe737eeb`  
		Last Modified: Sat, 19 Oct 2024 02:09:07 GMT  
		Size: 33.3 MB (33288962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d95218d2da28d04d81c234b738de8dbb1ebb995e5e0d79ac9a15cd0141bf467`  
		Last Modified: Sat, 19 Oct 2024 02:09:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2264d2ff910b67333d76b8d9773207c2a1fadd72260eacb24c1aaa0e6b68adc7`  
		Last Modified: Sat, 19 Oct 2024 02:09:07 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8940cfc39177e2a9294a30e8d2153046e6ecece90e6faaf1202a450cb6d9ea26`  
		Last Modified: Sat, 19 Oct 2024 02:09:07 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:adcce1b6d87db7e3e86f252bb29b53eaa84144a6bac068a4f652cdc67eecbb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4647714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f23fc0888008bf76e6fdc127c8cc79130ba16c90c30a98cb10877273a7b2e9`

```dockerfile
```

-	Layers:
	-	`sha256:dcddeb1bacaee184c5d3c7163250eb28d79b834d5076cd3a80fdabda4fc4c619`  
		Last Modified: Sat, 19 Oct 2024 02:09:07 GMT  
		Size: 4.6 MB (4633039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcff244de46f780a8df7b4db4e66969d004dd7763dd1fe2d8a7f490097b69fe3`  
		Last Modified: Sat, 19 Oct 2024 02:09:06 GMT  
		Size: 14.7 KB (14675 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-data-alpine`

```console
$ docker pull influxdb@sha256:8e4766170552f7235b1c95b807219c581220679cfff432ac822c633df62bc67d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2be9c69c4dcd5b5ae85762696e710b68b9274a3ffece838c55f1c4dfd476720e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38122546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d021f63e78c0dcaf4f0c4843c08277496a2f3fa39a22064e24859434ce7570a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc88cdf71faaf02dcebd3cdcc8ce57a3b308c18e1848992c3aa12889d68a7301`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f1954a31a733b8d976bc7f913379f93944a904187dada2925e7b3cdbabc0f5`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 1.5 MB (1479490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea04e3b2c5bbeec39091ab366a332265cf6a1fcd0a00a3d955795bfbdefdf86b`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 33.2 MB (33248810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31752a5b6441ca3f6fbf58a13a9df69554b08cd5a0a98b42b9af86bd91bae722`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e28722e5f3c56298697a4b05f52f60035c8581bfc3598ce2fcf490278b3e4fa`  
		Last Modified: Fri, 06 Sep 2024 23:21:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a27e41d4bb82b0a46cee7d7b7054ea092e52fb02cf0c3620e2cdf32e0038ca`  
		Last Modified: Fri, 06 Sep 2024 23:21:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:52997d7d8ef387e2e2bf5593c589b466eae768552b84efa1547cdb8ce44616e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1137829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baab96e09494545e50ecde071d196cb1a9b8250cb52b0d169702e169b2c85bb1`

```dockerfile
```

-	Layers:
	-	`sha256:1781d7e34c0831e0d91185e04c6d0e841144d3fdfcfe61991f8e8c86ba334130`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 1.1 MB (1121383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1d27a2c65fe763ea61971a95d715655cd32f3bcf319da8dabb4f1900c2e7056`  
		Last Modified: Fri, 06 Sep 2024 23:21:25 GMT  
		Size: 16.4 KB (16446 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-meta`

```console
$ docker pull influxdb@sha256:0b12d867797874998ce544bb011dc633fb75c8899fca47f0ff9a246f8b9d9a30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c62fd9cf4f8989fe6de61393e6a47bac445f2d3b2d88cfff9afc37eb1c7e2feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83614618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046720e40a7ffc852d231dcc274e2df95828bf26e440c1082e29adbb43e143b9`
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
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb* # buildkit
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
	-	`sha256:44177e4886f7b216e3082e1da60e6d82848c622f46a53a9ed933dba52a1426f0`  
		Last Modified: Sat, 19 Oct 2024 02:09:10 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0585491307193b87cbf3dbe3c4e401f798d5be4cf362b38c3619d6a4f0127fc`  
		Last Modified: Sat, 19 Oct 2024 02:09:11 GMT  
		Size: 12.8 MB (12769365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f84edd12eb3d695d601eb18d7338912e0729c578e1643bf817c6da8a7b2b2c`  
		Last Modified: Sat, 19 Oct 2024 02:09:10 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60fe16d5196be0ced0631ee5eb99a1cdad0d437779872ee5a5d98dafe39d058`  
		Last Modified: Sat, 19 Oct 2024 02:09:10 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:ede9eb5b8b1efe8e5369ce181615ccaf28355559fb41cc45ed3b532085d7ec03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4581906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23425e5904dc79952c381d0415976bc3b173f5f0f2047b7f5ef9b006d2c10e53`

```dockerfile
```

-	Layers:
	-	`sha256:90c42b7d85376fd8ebfe9d4902f7f9925f53b6608f667ba7bf6034fe8735d929`  
		Last Modified: Sat, 19 Oct 2024 02:09:10 GMT  
		Size: 4.6 MB (4568872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cefd7ecd6ebca3486567d4c00570a5f30eefc83cbd1d0bb8439d7aba14d00dd`  
		Last Modified: Sat, 19 Oct 2024 02:09:10 GMT  
		Size: 13.0 KB (13034 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.9.13-meta-alpine`

```console
$ docker pull influxdb@sha256:4d3a9c68cfc5211e9079595580408c93af827777d33bf0f66a34a87c0966a03f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.9.13-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e4d7f35c0a96a009bc919f98118cf471c253e54c5dd47ff14ab4fd80b86e4c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17569067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77bc62f618fb464838b1d92de778a70e3072262f06ecd84f96c4073d5898eb3`
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
ENV INFLUXDB_VERSION=1.9.13-c1.9.13
# Fri, 16 Aug 2024 20:18:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:020562199c64aad524deae5d3ab9ce90e8b6cd8a2f2efa68dc89be44c4bbbcb0`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164109d9ed866529603429a063011bb370e035ba2582d27646c7d720dc703e70`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 1.2 MB (1223701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2001df372492d0f10ab280222c05f3d766032e54ebdbb87c17e1c55489fbcf8`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 12.7 MB (12720713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680dcab1180b67227ca80095a9b3b636c0182c7d8df7c911b8b8f2a097e3456`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8044a8f410b1af2cb55de0e9463e0da9482b826ed89980872400a29373ad7145`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.9.13-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e4ec93149fe8e573bc5b6cdfbd1476c21c497f6b34a54badf6e7addaf3b882ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.0 KB (692992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a56585d872141e680b91773c695f6dc007ef5b4ade58ae79965a0d351dcd95`

```dockerfile
```

-	Layers:
	-	`sha256:b6d1ec9d01fb7b59c9c9d2c5998b0930a3b42d3648164bb5573ae0fc0cf64fa8`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 678.2 KB (678179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a4e5534447245d871a73fce3f69e717a88c925647a19d9bfabd1b57d1b5e69`  
		Last Modified: Fri, 06 Sep 2024 23:21:34 GMT  
		Size: 14.8 KB (14813 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:5b798d7416136e428ff526d2ad83303bb4edb81da0d5fa95888b1c8c0bcda134
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:319ce022b85d282d07bc52dc5c18cf7061d20c943611ea9485edcb81c50f1298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168474895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf97a8387e4cb591c98a8f0f63095eb62d4881987e85353e78b27421382c5e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d63a08c7eae5440f701cc6858c73ecb663ca464ca5f7297a45e9fb3eb3a4f`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 9.8 MB (9789023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79d848131cf22d53e8aac7afc13de4c94db0e67fcb3a1f542c9323d405c6da9`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa68d30e96e615e9fca421d49b4a1cd3182019ed643e18a649c6d409a92908d`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0632fe52ca6e66aef9a0ee508404b1580938021b1a4cba3dfa05a0748af0a2f`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daaf46366a05714e76e3cf878c6bbd187fb227432c84990976f619898eb50ca`  
		Last Modified: Thu, 17 Oct 2024 01:20:50 GMT  
		Size: 99.6 MB (99594042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267a093a7340725a354143031282a6e51e5e87a83448fdf2f6564444e904a82e`  
		Last Modified: Thu, 17 Oct 2024 01:20:44 GMT  
		Size: 23.1 MB (23128284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1db2304a9d48c608be0123ecbd6dd867c451a4320dd9d6264e4996ec75b561`  
		Last Modified: Thu, 17 Oct 2024 01:20:44 GMT  
		Size: 206.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea034d43eb0fa15d935a1fe5a76a42ace203c6511bfc64abb2f834adb3bc9f27`  
		Last Modified: Thu, 17 Oct 2024 01:20:44 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ea9af04bec13c5021a411268e61867e029bb50d54e1cf0fdc113c917fa6cb0`  
		Last Modified: Thu, 17 Oct 2024 01:20:45 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:2b12fa68711e9695673f23dc14dd48014f76e76fecdbe27d05c9cc94907ffebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf6598a45e001dcc4d2748317a5cee546d29ebaf17d81b1be77d723d46979af`

```dockerfile
```

-	Layers:
	-	`sha256:ddbb603944f9653c6a71080f284b9be4ed442a43900e74768fb8df7f580af7eb`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 2.8 MB (2833456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af171e6fb6fc6ff576639374f6efb89f1663e9dc28a8b3ddcbe93fb4523e2f05`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 33.6 KB (33583 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e868d1600edd8089fee79ec93bc9b9a874dd59657685beab6aa33e89628b88c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162243738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0392a105c41bbb7f21d5d2e4cdd81d8b5971c12c740ff1c40151e07e8161c780`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
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
	-	`sha256:4c47723566f228b07ff5d57db18e1c87e4463f7a36491d3090a9c6dd5a5d19d7`  
		Last Modified: Thu, 17 Oct 2024 13:12:49 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b3acaa3d8a770045bbf66c385f8a09823c1ac901232e38788aa227470bd547`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb149da990954284311258019f063f8f0bd13f4b5cedaca0e0d0ed1b44aff5f`  
		Last Modified: Thu, 17 Oct 2024 13:12:53 GMT  
		Size: 95.4 MB (95427914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b64f5633487b8aac6d38c04bf606d5f3f91d6426c9d10d1eba20a894f116683`  
		Last Modified: Thu, 17 Oct 2024 13:12:52 GMT  
		Size: 21.7 MB (21662510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626512735487ab501075ee9cf97e20c3938b2d4c2e0445c47b17c8c08a5af7fc`  
		Last Modified: Thu, 17 Oct 2024 13:12:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f6f1f28517e9fc76e13aa0b82d70a168fa8689079c271f48810701c28e1721`  
		Last Modified: Thu, 17 Oct 2024 13:12:51 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481781e12f0bbee62601a33c32e3462a5285cd571880dcea2d477e429585ff68`  
		Last Modified: Thu, 17 Oct 2024 13:12:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:84d3dc0ef53c0da5c5d20a9994eb0395f337e5be5f03efb3e337c59321fd05a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ea009bc533482e8df701998bcc811daeed56da89ae23553325e9d28a798599`

```dockerfile
```

-	Layers:
	-	`sha256:4c90288f5758d3ed7e62cc826e059c1d584a23a8a55f89ca30c0f6625278e02c`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 2.8 MB (2832693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdeb6a187d8b2bf9c3a184709f1f277fb12cb2a8fb80e5a93e5d5cc3026ae7e3`  
		Last Modified: Thu, 17 Oct 2024 13:12:49 GMT  
		Size: 33.8 KB (33765 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:327be0243a329b1da350a37c1468d756f4258330d50d10a2a993e5bb9a6e3d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cac47619d57d832e6a0f787362eba5b3e1f36629afd0e2e843e066b35151e380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92006098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6a7f3befda36a7f068f8339e56f8f59f6e527333e161482eae1d0df560e75c`
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
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078166243ebe0c2b9c91a2f7e164076218c7716b68301080fac2f19f177dd096`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1587bf1467bd7fa0cc2b3706d4443a35b49f61bd49b1290f081643d747c38c`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 9.6 MB (9634631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed395597bc0621a59fd604631b8c292c382b858b04d465c184da49759e54a5f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 5.8 MB (5820945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0f5c43f5e203308ab55d4d25d6adedc07ff5e1ae398853254c3b438bbf159`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050deb0e5ac12402242203b9a1622d17bb64075b547efbbd845bec1f2a228b3f`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 49.8 MB (49790466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84be9b15369ef3c36eb630297dc094d0685e0b0b896139448712012f1770e988`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 23.1 MB (23128284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64fac09c6feb55954579c03c8eb95a176fa4466a843ffd0bff0f34285b16fff`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc407c5347f2647cdac2b45ee7c93f275e3b7b3ae212b1ef9aa98d85bcde01a2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd950ffb540d8825efa00e5972a9aa81a31adcd1b9c6350cac0788e1a18392f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:acbb7b79cd5c3b0c183013df9776032eb14bb163e9eb2b3becd90c70b47a0c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3b3774810f57f3371aa23eaffa51ffbdc41e5b074a7c7e3ab902304cffe58`

```dockerfile
```

-	Layers:
	-	`sha256:5c072ab20e36c5f3b5b02ca06364a72e79aad9b7562f55eacf3460ebc071a8ed`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 914.1 KB (914093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b689f3cda8aaa0b6667d6a4d53280e261fa5922f2272a2269832f1b17f8711f`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1000811b02d8b6fdb75ea723c4e9c33746c27e6d0be65a84b9152ecc28fb0f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88688483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feba5f301346b7e3cba9218b3a9b5ae318b06386a0b000e04c7dab92f1576f5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9713c4c4a81b87a3373d8e7be5320c3cc5cc86ad74b6c2a3b331c3be04d8cac`  
		Last Modified: Sat, 07 Sep 2024 05:27:20 GMT  
		Size: 9.8 MB (9757048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbef7f92137af9c8d8b2ceb13c99138a68cd759251cc1d5e407ff11e6bd9db8`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 5.5 MB (5463803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7a1f6a4d13197b794b1cec6c7f7160c8d5a86013ec29ba75ac7fb7cd7dda19`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928a7eba1ff5a21c666fa39ef8dade819caf6ce52010688b7d5b2d950456277`  
		Last Modified: Sat, 07 Sep 2024 05:27:22 GMT  
		Size: 47.7 MB (47709505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2432c5f0597753c705d3724184b3356815256a64a8c93aa3781d2e785593ce7`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5933260cd0024e114bab17baef98e72aa06083573baa234ae705402c874b1a6e`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fdf5a00e872d5be68ab0f1f4c181170fb92a665999710b3589a2f80b8354b`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c614e03155dfd058b554c17f6b42e3fa4eddd5938d80ec113ef5ea4e07bc045a`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd0b50cc9671d0a3aded8e829d944212c24854b17ce177492fdd78e3c85adbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c436daff587bcef14431aa15b0a39ef47994bc66d9a0353450d30a519c01ad27`

```dockerfile
```

-	Layers:
	-	`sha256:ca5611f32d0ac5d978cefb8dc3b90ae6bfae5a67b19d2f2bdc02d6c9000569a7`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 913.4 KB (913354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e00d02321e4e44e7c735484a05227ce7d6b07e76a212b03bf5b22f30d7ee3d3`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:5b798d7416136e428ff526d2ad83303bb4edb81da0d5fa95888b1c8c0bcda134
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:319ce022b85d282d07bc52dc5c18cf7061d20c943611ea9485edcb81c50f1298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168474895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf97a8387e4cb591c98a8f0f63095eb62d4881987e85353e78b27421382c5e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d63a08c7eae5440f701cc6858c73ecb663ca464ca5f7297a45e9fb3eb3a4f`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 9.8 MB (9789023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79d848131cf22d53e8aac7afc13de4c94db0e67fcb3a1f542c9323d405c6da9`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa68d30e96e615e9fca421d49b4a1cd3182019ed643e18a649c6d409a92908d`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0632fe52ca6e66aef9a0ee508404b1580938021b1a4cba3dfa05a0748af0a2f`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daaf46366a05714e76e3cf878c6bbd187fb227432c84990976f619898eb50ca`  
		Last Modified: Thu, 17 Oct 2024 01:20:50 GMT  
		Size: 99.6 MB (99594042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267a093a7340725a354143031282a6e51e5e87a83448fdf2f6564444e904a82e`  
		Last Modified: Thu, 17 Oct 2024 01:20:44 GMT  
		Size: 23.1 MB (23128284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1db2304a9d48c608be0123ecbd6dd867c451a4320dd9d6264e4996ec75b561`  
		Last Modified: Thu, 17 Oct 2024 01:20:44 GMT  
		Size: 206.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea034d43eb0fa15d935a1fe5a76a42ace203c6511bfc64abb2f834adb3bc9f27`  
		Last Modified: Thu, 17 Oct 2024 01:20:44 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ea9af04bec13c5021a411268e61867e029bb50d54e1cf0fdc113c917fa6cb0`  
		Last Modified: Thu, 17 Oct 2024 01:20:45 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:2b12fa68711e9695673f23dc14dd48014f76e76fecdbe27d05c9cc94907ffebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf6598a45e001dcc4d2748317a5cee546d29ebaf17d81b1be77d723d46979af`

```dockerfile
```

-	Layers:
	-	`sha256:ddbb603944f9653c6a71080f284b9be4ed442a43900e74768fb8df7f580af7eb`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 2.8 MB (2833456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af171e6fb6fc6ff576639374f6efb89f1663e9dc28a8b3ddcbe93fb4523e2f05`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 33.6 KB (33583 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e868d1600edd8089fee79ec93bc9b9a874dd59657685beab6aa33e89628b88c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162243738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0392a105c41bbb7f21d5d2e4cdd81d8b5971c12c740ff1c40151e07e8161c780`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
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
	-	`sha256:4c47723566f228b07ff5d57db18e1c87e4463f7a36491d3090a9c6dd5a5d19d7`  
		Last Modified: Thu, 17 Oct 2024 13:12:49 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b3acaa3d8a770045bbf66c385f8a09823c1ac901232e38788aa227470bd547`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb149da990954284311258019f063f8f0bd13f4b5cedaca0e0d0ed1b44aff5f`  
		Last Modified: Thu, 17 Oct 2024 13:12:53 GMT  
		Size: 95.4 MB (95427914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b64f5633487b8aac6d38c04bf606d5f3f91d6426c9d10d1eba20a894f116683`  
		Last Modified: Thu, 17 Oct 2024 13:12:52 GMT  
		Size: 21.7 MB (21662510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626512735487ab501075ee9cf97e20c3938b2d4c2e0445c47b17c8c08a5af7fc`  
		Last Modified: Thu, 17 Oct 2024 13:12:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f6f1f28517e9fc76e13aa0b82d70a168fa8689079c271f48810701c28e1721`  
		Last Modified: Thu, 17 Oct 2024 13:12:51 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481781e12f0bbee62601a33c32e3462a5285cd571880dcea2d477e429585ff68`  
		Last Modified: Thu, 17 Oct 2024 13:12:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:84d3dc0ef53c0da5c5d20a9994eb0395f337e5be5f03efb3e337c59321fd05a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ea009bc533482e8df701998bcc811daeed56da89ae23553325e9d28a798599`

```dockerfile
```

-	Layers:
	-	`sha256:4c90288f5758d3ed7e62cc826e059c1d584a23a8a55f89ca30c0f6625278e02c`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 2.8 MB (2832693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdeb6a187d8b2bf9c3a184709f1f277fb12cb2a8fb80e5a93e5d5cc3026ae7e3`  
		Last Modified: Thu, 17 Oct 2024 13:12:49 GMT  
		Size: 33.8 KB (33765 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:327be0243a329b1da350a37c1468d756f4258330d50d10a2a993e5bb9a6e3d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cac47619d57d832e6a0f787362eba5b3e1f36629afd0e2e843e066b35151e380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92006098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6a7f3befda36a7f068f8339e56f8f59f6e527333e161482eae1d0df560e75c`
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
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078166243ebe0c2b9c91a2f7e164076218c7716b68301080fac2f19f177dd096`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1587bf1467bd7fa0cc2b3706d4443a35b49f61bd49b1290f081643d747c38c`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 9.6 MB (9634631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed395597bc0621a59fd604631b8c292c382b858b04d465c184da49759e54a5f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 5.8 MB (5820945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0f5c43f5e203308ab55d4d25d6adedc07ff5e1ae398853254c3b438bbf159`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050deb0e5ac12402242203b9a1622d17bb64075b547efbbd845bec1f2a228b3f`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 49.8 MB (49790466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84be9b15369ef3c36eb630297dc094d0685e0b0b896139448712012f1770e988`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 23.1 MB (23128284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64fac09c6feb55954579c03c8eb95a176fa4466a843ffd0bff0f34285b16fff`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc407c5347f2647cdac2b45ee7c93f275e3b7b3ae212b1ef9aa98d85bcde01a2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd950ffb540d8825efa00e5972a9aa81a31adcd1b9c6350cac0788e1a18392f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:acbb7b79cd5c3b0c183013df9776032eb14bb163e9eb2b3becd90c70b47a0c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3b3774810f57f3371aa23eaffa51ffbdc41e5b074a7c7e3ab902304cffe58`

```dockerfile
```

-	Layers:
	-	`sha256:5c072ab20e36c5f3b5b02ca06364a72e79aad9b7562f55eacf3460ebc071a8ed`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 914.1 KB (914093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b689f3cda8aaa0b6667d6a4d53280e261fa5922f2272a2269832f1b17f8711f`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1000811b02d8b6fdb75ea723c4e9c33746c27e6d0be65a84b9152ecc28fb0f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88688483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feba5f301346b7e3cba9218b3a9b5ae318b06386a0b000e04c7dab92f1576f5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9713c4c4a81b87a3373d8e7be5320c3cc5cc86ad74b6c2a3b331c3be04d8cac`  
		Last Modified: Sat, 07 Sep 2024 05:27:20 GMT  
		Size: 9.8 MB (9757048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbef7f92137af9c8d8b2ceb13c99138a68cd759251cc1d5e407ff11e6bd9db8`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 5.5 MB (5463803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7a1f6a4d13197b794b1cec6c7f7160c8d5a86013ec29ba75ac7fb7cd7dda19`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928a7eba1ff5a21c666fa39ef8dade819caf6ce52010688b7d5b2d950456277`  
		Last Modified: Sat, 07 Sep 2024 05:27:22 GMT  
		Size: 47.7 MB (47709505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2432c5f0597753c705d3724184b3356815256a64a8c93aa3781d2e785593ce7`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5933260cd0024e114bab17baef98e72aa06083573baa234ae705402c874b1a6e`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fdf5a00e872d5be68ab0f1f4c181170fb92a665999710b3589a2f80b8354b`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c614e03155dfd058b554c17f6b42e3fa4eddd5938d80ec113ef5ea4e07bc045a`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd0b50cc9671d0a3aded8e829d944212c24854b17ce177492fdd78e3c85adbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c436daff587bcef14431aa15b0a39ef47994bc66d9a0353450d30a519c01ad27`

```dockerfile
```

-	Layers:
	-	`sha256:ca5611f32d0ac5d978cefb8dc3b90ae6bfae5a67b19d2f2bdc02d6c9000569a7`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 913.4 KB (913354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e00d02321e4e44e7c735484a05227ce7d6b07e76a212b03bf5b22f30d7ee3d3`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.10`

```console
$ docker pull influxdb@sha256:5b798d7416136e428ff526d2ad83303bb4edb81da0d5fa95888b1c8c0bcda134
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.10` - linux; amd64

```console
$ docker pull influxdb@sha256:319ce022b85d282d07bc52dc5c18cf7061d20c943611ea9485edcb81c50f1298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168474895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf97a8387e4cb591c98a8f0f63095eb62d4881987e85353e78b27421382c5e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d63a08c7eae5440f701cc6858c73ecb663ca464ca5f7297a45e9fb3eb3a4f`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 9.8 MB (9789023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79d848131cf22d53e8aac7afc13de4c94db0e67fcb3a1f542c9323d405c6da9`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa68d30e96e615e9fca421d49b4a1cd3182019ed643e18a649c6d409a92908d`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0632fe52ca6e66aef9a0ee508404b1580938021b1a4cba3dfa05a0748af0a2f`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daaf46366a05714e76e3cf878c6bbd187fb227432c84990976f619898eb50ca`  
		Last Modified: Thu, 17 Oct 2024 01:20:50 GMT  
		Size: 99.6 MB (99594042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267a093a7340725a354143031282a6e51e5e87a83448fdf2f6564444e904a82e`  
		Last Modified: Thu, 17 Oct 2024 01:20:44 GMT  
		Size: 23.1 MB (23128284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1db2304a9d48c608be0123ecbd6dd867c451a4320dd9d6264e4996ec75b561`  
		Last Modified: Thu, 17 Oct 2024 01:20:44 GMT  
		Size: 206.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea034d43eb0fa15d935a1fe5a76a42ace203c6511bfc64abb2f834adb3bc9f27`  
		Last Modified: Thu, 17 Oct 2024 01:20:44 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ea9af04bec13c5021a411268e61867e029bb50d54e1cf0fdc113c917fa6cb0`  
		Last Modified: Thu, 17 Oct 2024 01:20:45 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:2b12fa68711e9695673f23dc14dd48014f76e76fecdbe27d05c9cc94907ffebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf6598a45e001dcc4d2748317a5cee546d29ebaf17d81b1be77d723d46979af`

```dockerfile
```

-	Layers:
	-	`sha256:ddbb603944f9653c6a71080f284b9be4ed442a43900e74768fb8df7f580af7eb`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 2.8 MB (2833456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af171e6fb6fc6ff576639374f6efb89f1663e9dc28a8b3ddcbe93fb4523e2f05`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 33.6 KB (33583 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e868d1600edd8089fee79ec93bc9b9a874dd59657685beab6aa33e89628b88c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162243738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0392a105c41bbb7f21d5d2e4cdd81d8b5971c12c740ff1c40151e07e8161c780`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
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
	-	`sha256:4c47723566f228b07ff5d57db18e1c87e4463f7a36491d3090a9c6dd5a5d19d7`  
		Last Modified: Thu, 17 Oct 2024 13:12:49 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b3acaa3d8a770045bbf66c385f8a09823c1ac901232e38788aa227470bd547`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb149da990954284311258019f063f8f0bd13f4b5cedaca0e0d0ed1b44aff5f`  
		Last Modified: Thu, 17 Oct 2024 13:12:53 GMT  
		Size: 95.4 MB (95427914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b64f5633487b8aac6d38c04bf606d5f3f91d6426c9d10d1eba20a894f116683`  
		Last Modified: Thu, 17 Oct 2024 13:12:52 GMT  
		Size: 21.7 MB (21662510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626512735487ab501075ee9cf97e20c3938b2d4c2e0445c47b17c8c08a5af7fc`  
		Last Modified: Thu, 17 Oct 2024 13:12:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f6f1f28517e9fc76e13aa0b82d70a168fa8689079c271f48810701c28e1721`  
		Last Modified: Thu, 17 Oct 2024 13:12:51 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481781e12f0bbee62601a33c32e3462a5285cd571880dcea2d477e429585ff68`  
		Last Modified: Thu, 17 Oct 2024 13:12:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.10` - unknown; unknown

```console
$ docker pull influxdb@sha256:84d3dc0ef53c0da5c5d20a9994eb0395f337e5be5f03efb3e337c59321fd05a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ea009bc533482e8df701998bcc811daeed56da89ae23553325e9d28a798599`

```dockerfile
```

-	Layers:
	-	`sha256:4c90288f5758d3ed7e62cc826e059c1d584a23a8a55f89ca30c0f6625278e02c`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 2.8 MB (2832693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdeb6a187d8b2bf9c3a184709f1f277fb12cb2a8fb80e5a93e5d5cc3026ae7e3`  
		Last Modified: Thu, 17 Oct 2024 13:12:49 GMT  
		Size: 33.8 KB (33765 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.10-alpine`

```console
$ docker pull influxdb@sha256:327be0243a329b1da350a37c1468d756f4258330d50d10a2a993e5bb9a6e3d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cac47619d57d832e6a0f787362eba5b3e1f36629afd0e2e843e066b35151e380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92006098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6a7f3befda36a7f068f8339e56f8f59f6e527333e161482eae1d0df560e75c`
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
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078166243ebe0c2b9c91a2f7e164076218c7716b68301080fac2f19f177dd096`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1587bf1467bd7fa0cc2b3706d4443a35b49f61bd49b1290f081643d747c38c`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 9.6 MB (9634631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed395597bc0621a59fd604631b8c292c382b858b04d465c184da49759e54a5f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 5.8 MB (5820945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0f5c43f5e203308ab55d4d25d6adedc07ff5e1ae398853254c3b438bbf159`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050deb0e5ac12402242203b9a1622d17bb64075b547efbbd845bec1f2a228b3f`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 49.8 MB (49790466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84be9b15369ef3c36eb630297dc094d0685e0b0b896139448712012f1770e988`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 23.1 MB (23128284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64fac09c6feb55954579c03c8eb95a176fa4466a843ffd0bff0f34285b16fff`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc407c5347f2647cdac2b45ee7c93f275e3b7b3ae212b1ef9aa98d85bcde01a2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd950ffb540d8825efa00e5972a9aa81a31adcd1b9c6350cac0788e1a18392f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.10-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:acbb7b79cd5c3b0c183013df9776032eb14bb163e9eb2b3becd90c70b47a0c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3b3774810f57f3371aa23eaffa51ffbdc41e5b074a7c7e3ab902304cffe58`

```dockerfile
```

-	Layers:
	-	`sha256:5c072ab20e36c5f3b5b02ca06364a72e79aad9b7562f55eacf3460ebc071a8ed`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 914.1 KB (914093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b689f3cda8aaa0b6667d6a4d53280e261fa5922f2272a2269832f1b17f8711f`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.10-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1000811b02d8b6fdb75ea723c4e9c33746c27e6d0be65a84b9152ecc28fb0f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88688483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feba5f301346b7e3cba9218b3a9b5ae318b06386a0b000e04c7dab92f1576f5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9713c4c4a81b87a3373d8e7be5320c3cc5cc86ad74b6c2a3b331c3be04d8cac`  
		Last Modified: Sat, 07 Sep 2024 05:27:20 GMT  
		Size: 9.8 MB (9757048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbef7f92137af9c8d8b2ceb13c99138a68cd759251cc1d5e407ff11e6bd9db8`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 5.5 MB (5463803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7a1f6a4d13197b794b1cec6c7f7160c8d5a86013ec29ba75ac7fb7cd7dda19`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928a7eba1ff5a21c666fa39ef8dade819caf6ce52010688b7d5b2d950456277`  
		Last Modified: Sat, 07 Sep 2024 05:27:22 GMT  
		Size: 47.7 MB (47709505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2432c5f0597753c705d3724184b3356815256a64a8c93aa3781d2e785593ce7`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5933260cd0024e114bab17baef98e72aa06083573baa234ae705402c874b1a6e`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fdf5a00e872d5be68ab0f1f4c181170fb92a665999710b3589a2f80b8354b`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c614e03155dfd058b554c17f6b42e3fa4eddd5938d80ec113ef5ea4e07bc045a`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.10-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd0b50cc9671d0a3aded8e829d944212c24854b17ce177492fdd78e3c85adbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c436daff587bcef14431aa15b0a39ef47994bc66d9a0353450d30a519c01ad27`

```dockerfile
```

-	Layers:
	-	`sha256:ca5611f32d0ac5d978cefb8dc3b90ae6bfae5a67b19d2f2bdc02d6c9000569a7`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 913.4 KB (913354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e00d02321e4e44e7c735484a05227ce7d6b07e76a212b03bf5b22f30d7ee3d3`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:327be0243a329b1da350a37c1468d756f4258330d50d10a2a993e5bb9a6e3d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cac47619d57d832e6a0f787362eba5b3e1f36629afd0e2e843e066b35151e380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92006098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6a7f3befda36a7f068f8339e56f8f59f6e527333e161482eae1d0df560e75c`
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
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078166243ebe0c2b9c91a2f7e164076218c7716b68301080fac2f19f177dd096`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1587bf1467bd7fa0cc2b3706d4443a35b49f61bd49b1290f081643d747c38c`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 9.6 MB (9634631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed395597bc0621a59fd604631b8c292c382b858b04d465c184da49759e54a5f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 5.8 MB (5820945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0f5c43f5e203308ab55d4d25d6adedc07ff5e1ae398853254c3b438bbf159`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050deb0e5ac12402242203b9a1622d17bb64075b547efbbd845bec1f2a228b3f`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 49.8 MB (49790466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84be9b15369ef3c36eb630297dc094d0685e0b0b896139448712012f1770e988`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 23.1 MB (23128284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64fac09c6feb55954579c03c8eb95a176fa4466a843ffd0bff0f34285b16fff`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc407c5347f2647cdac2b45ee7c93f275e3b7b3ae212b1ef9aa98d85bcde01a2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd950ffb540d8825efa00e5972a9aa81a31adcd1b9c6350cac0788e1a18392f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:acbb7b79cd5c3b0c183013df9776032eb14bb163e9eb2b3becd90c70b47a0c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3b3774810f57f3371aa23eaffa51ffbdc41e5b074a7c7e3ab902304cffe58`

```dockerfile
```

-	Layers:
	-	`sha256:5c072ab20e36c5f3b5b02ca06364a72e79aad9b7562f55eacf3460ebc071a8ed`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 914.1 KB (914093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b689f3cda8aaa0b6667d6a4d53280e261fa5922f2272a2269832f1b17f8711f`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1000811b02d8b6fdb75ea723c4e9c33746c27e6d0be65a84b9152ecc28fb0f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88688483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feba5f301346b7e3cba9218b3a9b5ae318b06386a0b000e04c7dab92f1576f5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9713c4c4a81b87a3373d8e7be5320c3cc5cc86ad74b6c2a3b331c3be04d8cac`  
		Last Modified: Sat, 07 Sep 2024 05:27:20 GMT  
		Size: 9.8 MB (9757048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbef7f92137af9c8d8b2ceb13c99138a68cd759251cc1d5e407ff11e6bd9db8`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 5.5 MB (5463803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7a1f6a4d13197b794b1cec6c7f7160c8d5a86013ec29ba75ac7fb7cd7dda19`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928a7eba1ff5a21c666fa39ef8dade819caf6ce52010688b7d5b2d950456277`  
		Last Modified: Sat, 07 Sep 2024 05:27:22 GMT  
		Size: 47.7 MB (47709505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2432c5f0597753c705d3724184b3356815256a64a8c93aa3781d2e785593ce7`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5933260cd0024e114bab17baef98e72aa06083573baa234ae705402c874b1a6e`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fdf5a00e872d5be68ab0f1f4c181170fb92a665999710b3589a2f80b8354b`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c614e03155dfd058b554c17f6b42e3fa4eddd5938d80ec113ef5ea4e07bc045a`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd0b50cc9671d0a3aded8e829d944212c24854b17ce177492fdd78e3c85adbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c436daff587bcef14431aa15b0a39ef47994bc66d9a0353450d30a519c01ad27`

```dockerfile
```

-	Layers:
	-	`sha256:ca5611f32d0ac5d978cefb8dc3b90ae6bfae5a67b19d2f2bdc02d6c9000569a7`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 913.4 KB (913354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e00d02321e4e44e7c735484a05227ce7d6b07e76a212b03bf5b22f30d7ee3d3`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:5b798d7416136e428ff526d2ad83303bb4edb81da0d5fa95888b1c8c0bcda134
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:319ce022b85d282d07bc52dc5c18cf7061d20c943611ea9485edcb81c50f1298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168474895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf97a8387e4cb591c98a8f0f63095eb62d4881987e85353e78b27421382c5e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d63a08c7eae5440f701cc6858c73ecb663ca464ca5f7297a45e9fb3eb3a4f`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 9.8 MB (9789023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79d848131cf22d53e8aac7afc13de4c94db0e67fcb3a1f542c9323d405c6da9`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa68d30e96e615e9fca421d49b4a1cd3182019ed643e18a649c6d409a92908d`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0632fe52ca6e66aef9a0ee508404b1580938021b1a4cba3dfa05a0748af0a2f`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daaf46366a05714e76e3cf878c6bbd187fb227432c84990976f619898eb50ca`  
		Last Modified: Thu, 17 Oct 2024 01:20:50 GMT  
		Size: 99.6 MB (99594042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267a093a7340725a354143031282a6e51e5e87a83448fdf2f6564444e904a82e`  
		Last Modified: Thu, 17 Oct 2024 01:20:44 GMT  
		Size: 23.1 MB (23128284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1db2304a9d48c608be0123ecbd6dd867c451a4320dd9d6264e4996ec75b561`  
		Last Modified: Thu, 17 Oct 2024 01:20:44 GMT  
		Size: 206.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea034d43eb0fa15d935a1fe5a76a42ace203c6511bfc64abb2f834adb3bc9f27`  
		Last Modified: Thu, 17 Oct 2024 01:20:44 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ea9af04bec13c5021a411268e61867e029bb50d54e1cf0fdc113c917fa6cb0`  
		Last Modified: Thu, 17 Oct 2024 01:20:45 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:2b12fa68711e9695673f23dc14dd48014f76e76fecdbe27d05c9cc94907ffebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf6598a45e001dcc4d2748317a5cee546d29ebaf17d81b1be77d723d46979af`

```dockerfile
```

-	Layers:
	-	`sha256:ddbb603944f9653c6a71080f284b9be4ed442a43900e74768fb8df7f580af7eb`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 2.8 MB (2833456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af171e6fb6fc6ff576639374f6efb89f1663e9dc28a8b3ddcbe93fb4523e2f05`  
		Last Modified: Thu, 17 Oct 2024 01:20:43 GMT  
		Size: 33.6 KB (33583 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e868d1600edd8089fee79ec93bc9b9a874dd59657685beab6aa33e89628b88c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162243738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0392a105c41bbb7f21d5d2e4cdd81d8b5971c12c740ff1c40151e07e8161c780`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
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
	-	`sha256:4c47723566f228b07ff5d57db18e1c87e4463f7a36491d3090a9c6dd5a5d19d7`  
		Last Modified: Thu, 17 Oct 2024 13:12:49 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b3acaa3d8a770045bbf66c385f8a09823c1ac901232e38788aa227470bd547`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb149da990954284311258019f063f8f0bd13f4b5cedaca0e0d0ed1b44aff5f`  
		Last Modified: Thu, 17 Oct 2024 13:12:53 GMT  
		Size: 95.4 MB (95427914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b64f5633487b8aac6d38c04bf606d5f3f91d6426c9d10d1eba20a894f116683`  
		Last Modified: Thu, 17 Oct 2024 13:12:52 GMT  
		Size: 21.7 MB (21662510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626512735487ab501075ee9cf97e20c3938b2d4c2e0445c47b17c8c08a5af7fc`  
		Last Modified: Thu, 17 Oct 2024 13:12:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f6f1f28517e9fc76e13aa0b82d70a168fa8689079c271f48810701c28e1721`  
		Last Modified: Thu, 17 Oct 2024 13:12:51 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481781e12f0bbee62601a33c32e3462a5285cd571880dcea2d477e429585ff68`  
		Last Modified: Thu, 17 Oct 2024 13:12:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:84d3dc0ef53c0da5c5d20a9994eb0395f337e5be5f03efb3e337c59321fd05a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ea009bc533482e8df701998bcc811daeed56da89ae23553325e9d28a798599`

```dockerfile
```

-	Layers:
	-	`sha256:4c90288f5758d3ed7e62cc826e059c1d584a23a8a55f89ca30c0f6625278e02c`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 2.8 MB (2832693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdeb6a187d8b2bf9c3a184709f1f277fb12cb2a8fb80e5a93e5d5cc3026ae7e3`  
		Last Modified: Thu, 17 Oct 2024 13:12:49 GMT  
		Size: 33.8 KB (33765 bytes)  
		MIME: application/vnd.in-toto+json
