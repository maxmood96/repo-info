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
-	[`influxdb:2.7.11-alpine`](#influxdb2711-alpine)
-	[`influxdb:2.7.12`](#influxdb2712)
-	[`influxdb:3-core`](#influxdb3-core)
-	[`influxdb:3-enterprise`](#influxdb3-enterprise)
-	[`influxdb:3.0-core`](#influxdb30-core)
-	[`influxdb:3.0-enterprise`](#influxdb30-enterprise)
-	[`influxdb:3.0.3-core`](#influxdb303-core)
-	[`influxdb:3.0.3-enterprise`](#influxdb303-enterprise)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:core`](#influxdbcore)
-	[`influxdb:enterprise`](#influxdbenterprise)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:02b28b1633616f89563dd2694443f484ba45975d7d3fc284e592e687be06937c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:299e28e2df9b201edeabd055ac6753d7a9fa07ac2ab2abec21883d2671819ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108954418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a035503ee762898979a9c87d629e8c60fbf5e5a35e7cef5121bfda9bf3a04658`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Fri, 18 Apr 2025 17:08:47 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
VOLUME [/var/lib/influxdb]
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5625e9841209608ed8fbf58ec91607a091e297d8e448c06fd390384b8ac9b448`  
		Last Modified: Mon, 28 Apr 2025 22:17:55 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8578b90e8ac366fb831a7f17abe91ff20bdd86579a6b8c139a85c31d35c0a7`  
		Last Modified: Mon, 28 Apr 2025 22:17:55 GMT  
		Size: 39.4 MB (39439591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c52e3b29029afd417369c1c91873156e5128e5ac8204c6afab7f79d4c317114`  
		Last Modified: Mon, 28 Apr 2025 22:17:55 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f5528ee7fde2d0a67c6139990982a9514e7a2abd6e1d0c8184306b9feac89d`  
		Last Modified: Mon, 28 Apr 2025 22:17:55 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c1b205ddbd909fbebce295988a3582141b4694cbe15b5ce092a206e14c3364`  
		Last Modified: Mon, 28 Apr 2025 22:17:56 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:5f5e552d7fa0518bbddc08472fc929a34893e8853bb3e61e0bfd86e5c22edb6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4654704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1c26614e0cd01005885015d31600e5f2a2c819f3f0260b078cbe62e2ea5c9a`

```dockerfile
```

-	Layers:
	-	`sha256:b388f0b4824bffc34a74eccfd394877cf0f78150937d6d27a0308e2b34e94fe8`  
		Last Modified: Mon, 28 Apr 2025 22:17:55 GMT  
		Size: 4.6 MB (4639996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f29e29d5987ae7afe4dc3d331a2910432778915d83c26494c772384eefb9f21`  
		Last Modified: Mon, 28 Apr 2025 22:17:55 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:d334f7dc80f2350c7972ef626a18483481a4111b465072ec868d0c546e90eedd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3f7471d504d376f836e120c5023e587439f6702cc8eca5738128f41b43070676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44235015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828996846e1d79f70ff450ac9a51aefcf47703a2e6cc565d07ce6ce6cb9f8d59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Thu, 16 Jan 2025 12:29:50 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 16 Jan 2025 12:29:50 GMT
VOLUME [/var/lib/influxdb]
# Thu, 16 Jan 2025 12:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c981537527a695b8c20b6027e59d150b12110fc841db76dca1309d531060204c`  
		Last Modified: Fri, 14 Feb 2025 19:26:21 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe95b0d50fd108a7bab7229bf48c4d6f15d501d181e060aa9d75c5733498b45a`  
		Last Modified: Fri, 14 Feb 2025 19:26:22 GMT  
		Size: 1.2 MB (1226185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44173060551cc5ccb97812e53b623aa03ebd2405605f40c08c828ec1348fbce4`  
		Last Modified: Fri, 14 Feb 2025 19:26:22 GMT  
		Size: 39.4 MB (39379880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd95c0fb0fc1a1fe7c4dc1bac921311d6b89557c3b1a21520add3766f2d79b1d`  
		Last Modified: Fri, 14 Feb 2025 19:26:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2c3ee9de55100bff4c1fc71b7158bd83eb790d8173d9e4eabcc4d912accb3d`  
		Last Modified: Fri, 14 Feb 2025 19:26:22 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d857fb73ed049778a398a1c483940b544aa66d0b1548085c55a0f6e4c983671f`  
		Last Modified: Fri, 14 Feb 2025 19:26:22 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bf268b2ddc40a8a10950a75c25e7638047817bab7e45c5240c0d80f27dc103b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **772.3 KB (772266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1adeae65e3b21c8b252481f771bf870002bcee4fb1bc90afabb1994664332cd9`

```dockerfile
```

-	Layers:
	-	`sha256:ed3c3f6f87542f7b58682754fd0363c648e9018b214b9b105f86b910503c4dc6`  
		Last Modified: Fri, 14 Feb 2025 19:26:22 GMT  
		Size: 755.6 KB (755627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9539fc66665e5ef5dbcf98abd6782b4bb32862e6c51158c4d525f8a3acd705da`  
		Last Modified: Fri, 14 Feb 2025 19:26:21 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:427ab8e3ab8dba1e94b1f80d36aa78f40b8d91dabdbcfd9573b2d79b693ad926
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:b5fc1a7f2314d40d2f6f5a33bce67b62f7af71c411fa3d14c3e43c604ae1c601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88153648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8b1f100e31ea920f471be0c9ec694ac7d408742421dd4b0e21f55f7fb049ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Fri, 18 Apr 2025 17:08:47 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
VOLUME [/var/lib/influxdb]
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02731972ada82abba369a58d7ea56c1dcd9c5c882bdd9f7afa5a56f76dc1d3f`  
		Last Modified: Mon, 28 Apr 2025 22:17:53 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb76be7373bb12afbb56c531ffe41f7dd2bbb26ab6876dc8760e753339769a3`  
		Last Modified: Mon, 28 Apr 2025 22:17:54 GMT  
		Size: 18.6 MB (18640027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524da3c8d374d5322f8542fb5550d19d8876a88ea9d1b4f82f2c32c4f9de73f3`  
		Last Modified: Mon, 28 Apr 2025 22:17:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2b9d4ca75885855f52fdaf9ae6720e0cd67b867b54068e81d88eadcf7576da`  
		Last Modified: Mon, 28 Apr 2025 22:17:53 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:e58a80be4b1e968fb2367732f81227080b57aef48e9527a214b3b676cd413eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4577043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684ce1da4cd600c8d919aefc9d4314d068c0aa176ce01b64f02e6211dc7ccfa3`

```dockerfile
```

-	Layers:
	-	`sha256:99106bc6a08416e18b7b852507e7a2b234e96f7d056e28bd679cbe80e6424d12`  
		Last Modified: Mon, 28 Apr 2025 22:17:54 GMT  
		Size: 4.6 MB (4563976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c13e8520144bc4b437e771b48bf4c0b954f4a430a70333787405fe6aeee6bea`  
		Last Modified: Mon, 28 Apr 2025 22:17:53 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:4527cfdd71beb4c8c8c4c538ad398a23f857aa343fef75bf955f6fa8a0c3d0fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d7f1860406930457c4baceaebc6ab8a26b3ddb70f50d17c0e67e4b7710282f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23450300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b98f5e0509910fe0946600bc057ba0d496d52dcff577e63a97ea627ecbddeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Thu, 16 Jan 2025 12:29:50 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 16 Jan 2025 12:29:50 GMT
VOLUME [/var/lib/influxdb]
# Thu, 16 Jan 2025 12:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb5c8cdbec35edc43e48ac5677234575ad99cf8e483ecb8687d5419d5b425d`  
		Last Modified: Fri, 14 Feb 2025 19:26:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8e09bdbba52f1107efa5e5ba96ff16880584254227de593d5e9327a809f95`  
		Last Modified: Fri, 14 Feb 2025 19:26:12 GMT  
		Size: 1.2 MB (1226193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d9a6ef6450631c9e70c6a4ac06fd7f6a159ce59e4615829510b0c3cc0bb69b`  
		Last Modified: Fri, 14 Feb 2025 19:26:12 GMT  
		Size: 18.6 MB (18596363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c171bf24072ac133ca0666ed07f4bab8ca9f5e785f8726e5b6b22a6bcdafb7`  
		Last Modified: Fri, 14 Feb 2025 19:26:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb43bdb4aca4dfbb93ec902aaf20f61ea9ce655828dae6308ce794bb52b39c4`  
		Last Modified: Fri, 14 Feb 2025 19:26:13 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:1093805f816e88cbe248281568476054ed9adc8053e0a92d502b2c1581ea0ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.5 KB (694521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4672eb56930bd7a17bf509028cb07b25d9c262da044e3a99441b30d330fa2532`

```dockerfile
```

-	Layers:
	-	`sha256:42501ae21ce822aaef8827fd808bc3fbdce1cdf8b99a661c71aad06581352fb4`  
		Last Modified: Fri, 14 Feb 2025 19:26:12 GMT  
		Size: 679.5 KB (679511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f792b8250d838c0cf30993d65d8457974cc3309d67893a5bd86b44cb832c6098`  
		Last Modified: Fri, 14 Feb 2025 19:26:12 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.8-data`

```console
$ docker pull influxdb@sha256:02b28b1633616f89563dd2694443f484ba45975d7d3fc284e592e687be06937c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:299e28e2df9b201edeabd055ac6753d7a9fa07ac2ab2abec21883d2671819ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108954418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a035503ee762898979a9c87d629e8c60fbf5e5a35e7cef5121bfda9bf3a04658`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Fri, 18 Apr 2025 17:08:47 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
VOLUME [/var/lib/influxdb]
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5625e9841209608ed8fbf58ec91607a091e297d8e448c06fd390384b8ac9b448`  
		Last Modified: Mon, 28 Apr 2025 22:17:55 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8578b90e8ac366fb831a7f17abe91ff20bdd86579a6b8c139a85c31d35c0a7`  
		Last Modified: Mon, 28 Apr 2025 22:17:55 GMT  
		Size: 39.4 MB (39439591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c52e3b29029afd417369c1c91873156e5128e5ac8204c6afab7f79d4c317114`  
		Last Modified: Mon, 28 Apr 2025 22:17:55 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f5528ee7fde2d0a67c6139990982a9514e7a2abd6e1d0c8184306b9feac89d`  
		Last Modified: Mon, 28 Apr 2025 22:17:55 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c1b205ddbd909fbebce295988a3582141b4694cbe15b5ce092a206e14c3364`  
		Last Modified: Mon, 28 Apr 2025 22:17:56 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:5f5e552d7fa0518bbddc08472fc929a34893e8853bb3e61e0bfd86e5c22edb6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4654704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1c26614e0cd01005885015d31600e5f2a2c819f3f0260b078cbe62e2ea5c9a`

```dockerfile
```

-	Layers:
	-	`sha256:b388f0b4824bffc34a74eccfd394877cf0f78150937d6d27a0308e2b34e94fe8`  
		Last Modified: Mon, 28 Apr 2025 22:17:55 GMT  
		Size: 4.6 MB (4639996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f29e29d5987ae7afe4dc3d331a2910432778915d83c26494c772384eefb9f21`  
		Last Modified: Mon, 28 Apr 2025 22:17:55 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.8-data-alpine`

```console
$ docker pull influxdb@sha256:d334f7dc80f2350c7972ef626a18483481a4111b465072ec868d0c546e90eedd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3f7471d504d376f836e120c5023e587439f6702cc8eca5738128f41b43070676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44235015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828996846e1d79f70ff450ac9a51aefcf47703a2e6cc565d07ce6ce6cb9f8d59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Thu, 16 Jan 2025 12:29:50 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 16 Jan 2025 12:29:50 GMT
VOLUME [/var/lib/influxdb]
# Thu, 16 Jan 2025 12:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c981537527a695b8c20b6027e59d150b12110fc841db76dca1309d531060204c`  
		Last Modified: Fri, 14 Feb 2025 19:26:21 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe95b0d50fd108a7bab7229bf48c4d6f15d501d181e060aa9d75c5733498b45a`  
		Last Modified: Fri, 14 Feb 2025 19:26:22 GMT  
		Size: 1.2 MB (1226185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44173060551cc5ccb97812e53b623aa03ebd2405605f40c08c828ec1348fbce4`  
		Last Modified: Fri, 14 Feb 2025 19:26:22 GMT  
		Size: 39.4 MB (39379880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd95c0fb0fc1a1fe7c4dc1bac921311d6b89557c3b1a21520add3766f2d79b1d`  
		Last Modified: Fri, 14 Feb 2025 19:26:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2c3ee9de55100bff4c1fc71b7158bd83eb790d8173d9e4eabcc4d912accb3d`  
		Last Modified: Fri, 14 Feb 2025 19:26:22 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d857fb73ed049778a398a1c483940b544aa66d0b1548085c55a0f6e4c983671f`  
		Last Modified: Fri, 14 Feb 2025 19:26:22 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bf268b2ddc40a8a10950a75c25e7638047817bab7e45c5240c0d80f27dc103b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **772.3 KB (772266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1adeae65e3b21c8b252481f771bf870002bcee4fb1bc90afabb1994664332cd9`

```dockerfile
```

-	Layers:
	-	`sha256:ed3c3f6f87542f7b58682754fd0363c648e9018b214b9b105f86b910503c4dc6`  
		Last Modified: Fri, 14 Feb 2025 19:26:22 GMT  
		Size: 755.6 KB (755627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9539fc66665e5ef5dbcf98abd6782b4bb32862e6c51158c4d525f8a3acd705da`  
		Last Modified: Fri, 14 Feb 2025 19:26:21 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.8-meta`

```console
$ docker pull influxdb@sha256:427ab8e3ab8dba1e94b1f80d36aa78f40b8d91dabdbcfd9573b2d79b693ad926
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:b5fc1a7f2314d40d2f6f5a33bce67b62f7af71c411fa3d14c3e43c604ae1c601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88153648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8b1f100e31ea920f471be0c9ec694ac7d408742421dd4b0e21f55f7fb049ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Fri, 18 Apr 2025 17:08:47 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
VOLUME [/var/lib/influxdb]
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02731972ada82abba369a58d7ea56c1dcd9c5c882bdd9f7afa5a56f76dc1d3f`  
		Last Modified: Mon, 28 Apr 2025 22:17:53 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb76be7373bb12afbb56c531ffe41f7dd2bbb26ab6876dc8760e753339769a3`  
		Last Modified: Mon, 28 Apr 2025 22:17:54 GMT  
		Size: 18.6 MB (18640027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524da3c8d374d5322f8542fb5550d19d8876a88ea9d1b4f82f2c32c4f9de73f3`  
		Last Modified: Mon, 28 Apr 2025 22:17:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2b9d4ca75885855f52fdaf9ae6720e0cd67b867b54068e81d88eadcf7576da`  
		Last Modified: Mon, 28 Apr 2025 22:17:53 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:e58a80be4b1e968fb2367732f81227080b57aef48e9527a214b3b676cd413eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4577043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684ce1da4cd600c8d919aefc9d4314d068c0aa176ce01b64f02e6211dc7ccfa3`

```dockerfile
```

-	Layers:
	-	`sha256:99106bc6a08416e18b7b852507e7a2b234e96f7d056e28bd679cbe80e6424d12`  
		Last Modified: Mon, 28 Apr 2025 22:17:54 GMT  
		Size: 4.6 MB (4563976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c13e8520144bc4b437e771b48bf4c0b954f4a430a70333787405fe6aeee6bea`  
		Last Modified: Mon, 28 Apr 2025 22:17:53 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.8-meta-alpine`

```console
$ docker pull influxdb@sha256:4527cfdd71beb4c8c8c4c538ad398a23f857aa343fef75bf955f6fa8a0c3d0fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d7f1860406930457c4baceaebc6ab8a26b3ddb70f50d17c0e67e4b7710282f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23450300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b98f5e0509910fe0946600bc057ba0d496d52dcff577e63a97ea627ecbddeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Thu, 16 Jan 2025 12:29:50 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 16 Jan 2025 12:29:50 GMT
VOLUME [/var/lib/influxdb]
# Thu, 16 Jan 2025 12:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb5c8cdbec35edc43e48ac5677234575ad99cf8e483ecb8687d5419d5b425d`  
		Last Modified: Fri, 14 Feb 2025 19:26:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8e09bdbba52f1107efa5e5ba96ff16880584254227de593d5e9327a809f95`  
		Last Modified: Fri, 14 Feb 2025 19:26:12 GMT  
		Size: 1.2 MB (1226193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d9a6ef6450631c9e70c6a4ac06fd7f6a159ce59e4615829510b0c3cc0bb69b`  
		Last Modified: Fri, 14 Feb 2025 19:26:12 GMT  
		Size: 18.6 MB (18596363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c171bf24072ac133ca0666ed07f4bab8ca9f5e785f8726e5b6b22a6bcdafb7`  
		Last Modified: Fri, 14 Feb 2025 19:26:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb43bdb4aca4dfbb93ec902aaf20f61ea9ce655828dae6308ce794bb52b39c4`  
		Last Modified: Fri, 14 Feb 2025 19:26:13 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:1093805f816e88cbe248281568476054ed9adc8053e0a92d502b2c1581ea0ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.5 KB (694521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4672eb56930bd7a17bf509028cb07b25d9c262da044e3a99441b30d330fa2532`

```dockerfile
```

-	Layers:
	-	`sha256:42501ae21ce822aaef8827fd808bc3fbdce1cdf8b99a661c71aad06581352fb4`  
		Last Modified: Fri, 14 Feb 2025 19:26:12 GMT  
		Size: 679.5 KB (679511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f792b8250d838c0cf30993d65d8457974cc3309d67893a5bd86b44cb832c6098`  
		Last Modified: Fri, 14 Feb 2025 19:26:12 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11`

```console
$ docker pull influxdb@sha256:94a49b5a61133bd4a1ecb2f38834db269e650319396155dd45849dc3ade9a7a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:a13ef5e5c430e9db2abe0c0bcd01978a72198f0ef9de9b24b21fb2cd11f18174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116156659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866344fcd40677a9d9ca7d283e495ff4d848db3f1dc0e6b21e11ae52dcab6126`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ARG INFLUXDB_VERSION=1.11.8
# Fri, 18 Apr 2025 17:08:47 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
VOLUME [/var/lib/influxdb]
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
USER influxdb
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fefe14e102038e78e20a115f008c031e3c3e96c2e77e7f7376446763fc28fb7`  
		Last Modified: Mon, 28 Apr 2025 22:18:01 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966d2d230cc562a21baafb245a1a1bab566bed7aae54dedf03b273dadd8f4b39`  
		Last Modified: Mon, 28 Apr 2025 22:18:02 GMT  
		Size: 43.7 MB (43651364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371c10d9fe511cbff3235e7a119d07b3324912f8f99d9c5f29cf5c0c933516e5`  
		Last Modified: Mon, 28 Apr 2025 22:18:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b07d638cefee5c37c8998152872da139940a19f150fe06cda7f7631ef8fb9a6`  
		Last Modified: Mon, 28 Apr 2025 22:18:01 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add44ec0f9db3f00aeec425b060a2d5a44b91334276f4aa1e398eac9538944fb`  
		Last Modified: Mon, 28 Apr 2025 22:18:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:cbaef94be206b5c056d3e4dd54e672dd817fec7003d16d502dec881138e50afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4900642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754579a892d8389485d7a79ff7269ccc3acb4c13eb7ed64aafae257b8df65213`

```dockerfile
```

-	Layers:
	-	`sha256:da7a558bff723c7ca0bef362986720a2987fb96a12778ccfa3ed9e03e8f40d1f`  
		Last Modified: Mon, 28 Apr 2025 22:18:01 GMT  
		Size: 4.9 MB (4885113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c586946812b0db92b44664b8e35450a52316508c521560113066aba031117292`  
		Last Modified: Mon, 28 Apr 2025 22:18:01 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4bdc93e676b312056e4bea9ff6cf3f949bb3c59b22baf5aedab705bda6602a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112994104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f473f89a709507dafcb68452f89b945a6094c6ed86a237b33658274ab6daef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ARG INFLUXDB_VERSION=1.11.8
# Fri, 18 Apr 2025 17:08:47 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
VOLUME [/var/lib/influxdb]
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
USER influxdb
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7230da96acdc94e3f8d8734018cbe4356ea9e8cfa51f70bd0af80b6fe62f4e9`  
		Last Modified: Tue, 29 Apr 2025 19:03:33 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf9366b03aca06d7efa8e8a2431e785d468f64d28466453e4a314302f67b9d6`  
		Last Modified: Tue, 29 Apr 2025 19:03:35 GMT  
		Size: 41.1 MB (41119293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e6e3994447bf40bc2a3f6a7363620746307f567f86ba748d729abe46927066`  
		Last Modified: Tue, 29 Apr 2025 19:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f753b82db118c2a83a645110e36e028a38339203966ac3e3642c01d25bbf63`  
		Last Modified: Tue, 29 Apr 2025 19:03:34 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a230f3c7034cf12b98d77f24e6e50dba499eafee7057eddb91ebd16100faebc5`  
		Last Modified: Tue, 29 Apr 2025 19:03:34 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:da41dbb32ea141cb9e9398304c9bac55b671e64f72d17effa264db3c83bedf87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4900202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1323747a43fd182d2e34510446e4dbc4f8b64c1d33b1622875303d130d6184`

```dockerfile
```

-	Layers:
	-	`sha256:0a0501fc8b5e41ceb49ad17a5571cb6d67a84587b324113e2d8513ed2c128cbb`  
		Last Modified: Tue, 29 Apr 2025 19:03:34 GMT  
		Size: 4.9 MB (4884578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:230bc931e6f3434e5ddb0c866e30663d3d267b0a7ac0791db14f25c2825a1970`  
		Last Modified: Tue, 29 Apr 2025 19:03:33 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-alpine`

```console
$ docker pull influxdb@sha256:296f6b84023644996087634e52ace8ce166072f4cf4d3de134cf3d12a4e14daf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9f82853b44202c9b9543797da922fc200a11fb4d3ab3802919fcbd8b30d2885f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42924012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffa1d079420b9dd6b45c1eb667d6cbe07765e63ca3a9ddcf17a94469a235052`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 16 Jan 2025 12:29:50 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 16 Jan 2025 12:29:50 GMT
VOLUME [/var/lib/influxdb]
# Thu, 16 Jan 2025 12:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
USER influxdb
# Thu, 16 Jan 2025 12:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2430b91d27c94577a29aa4a63bc67b9a6bdb38f557ff03f2f47fe9fc4912a6e6`  
		Last Modified: Fri, 14 Feb 2025 19:26:19 GMT  
		Size: 1.2 MB (1226180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccd48b38856008daab1f21e8835b3d7b372598317d42820fc3f047db607ccec`  
		Last Modified: Fri, 14 Feb 2025 19:26:20 GMT  
		Size: 38.1 MB (38068218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94026e2b0d6f99fed3dedfb812a03fd046e8373145be2b2e4aee6b44295f325`  
		Last Modified: Fri, 14 Feb 2025 19:26:19 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfc22a651b18903f12176ed3447abf101612d8f6c009dde4beb5d65b864ff40`  
		Last Modified: Fri, 14 Feb 2025 19:26:19 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff30a98894f91ab375651dec55dbdaa6676482eba3ae74a247a1227bf992e1e`  
		Last Modified: Fri, 14 Feb 2025 19:26:20 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02c49477a92d638620b098485571f719849cc4a14d1a0bbbf9475ac5036c368`  
		Last Modified: Fri, 14 Feb 2025 19:26:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:6aece94c98efbd06cabb8c240362992a7c541ea528326d78f89f00453903db3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **761.2 KB (761197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eef1547a75ac110ec9e8b88fd14d8f8ee24dd109fffd7b1076e0e570262c36f`

```dockerfile
```

-	Layers:
	-	`sha256:71bf4ec5268dedf5ca4c30a6a5925e7e457bde1e6459d68581c4f78a5cc814d2`  
		Last Modified: Fri, 14 Feb 2025 19:26:19 GMT  
		Size: 743.3 KB (743321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f642c9f83ff2a959cec65a14ea556a5c772b8a03eecfc06b77b2212dd3f8fc78`  
		Last Modified: Fri, 14 Feb 2025 19:26:19 GMT  
		Size: 17.9 KB (17876 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:953b49df68a85bd7a4249179427f2ccf7a32492077fbaaf76086aefdaafd3b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40946457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57e22fed09a879e6c6b210345d03839c734d7a58a78a1bca8458178333a8b67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 16 Jan 2025 12:29:50 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 16 Jan 2025 12:29:50 GMT
VOLUME [/var/lib/influxdb]
# Thu, 16 Jan 2025 12:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
USER influxdb
# Thu, 16 Jan 2025 12:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e30a0c587fbc2e84c1b8c55a170ea149c6f6fb91469699f82a5d44e4dad9fdf`  
		Last Modified: Fri, 14 Feb 2025 23:51:00 GMT  
		Size: 1.3 MB (1307075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aedc2e6ed32b6b172146ed1536e1bc4675e2368a442a55fcbc77d582da9ded`  
		Last Modified: Fri, 14 Feb 2025 23:51:01 GMT  
		Size: 35.5 MB (35545506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f6a37ff4f04b2e3f6d6663dc1ad32dca8556db22f6aba5fa140293e06b8be6`  
		Last Modified: Fri, 14 Feb 2025 23:50:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e42b050238199a9cf809362968a20163c7d745329b332b4c122d9810b828e2`  
		Last Modified: Fri, 14 Feb 2025 23:51:00 GMT  
		Size: 995.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afc13286215e26f9388e94e989e8e7f25e3ba851d010c09add249a03c7801ee`  
		Last Modified: Fri, 14 Feb 2025 23:51:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644f23186760a8bda37888b6b2a4baf18413763b0df806f478204d981fb50ef4`  
		Last Modified: Fri, 14 Feb 2025 23:51:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:860c8f802880c137e332828aa61d9ed176550fd869d022ee7e855884da8be5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.5 KB (760532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f42dd545635dc9ef0090a95d89b4d81befa789af9e32c92013b929fff3ef08`

```dockerfile
```

-	Layers:
	-	`sha256:f4f18639c44a9d2627db6142d1f0777cada87e232e3b63751f110640b89a6e51`  
		Last Modified: Fri, 14 Feb 2025 23:51:00 GMT  
		Size: 742.5 KB (742548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b1bc5d6ee15c6f1c9cb67454a907a5fafdc070f8a6cfd9143ff759f6ff93bd`  
		Last Modified: Fri, 14 Feb 2025 23:50:59 GMT  
		Size: 18.0 KB (17984 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:8ecaef75f8c0bb89d35d6805d91cdbbc928350044c004480fd92a487c34d774f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:64c51dc476e2e465503c527f6d27da53e8257f05413c277ebf3f98e273fb0d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111685244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5edc9b10be52efb489f6691964fcab404e708e54bc2db68cf6b9cd62608be5ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Fri, 18 Apr 2025 17:08:47 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
VOLUME [/var/lib/influxdb]
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6149e1950349e0c9f9a5854ac506edf5d45fe1c302b2dbd705d495efaf2f0f21`  
		Last Modified: Mon, 28 Apr 2025 22:18:07 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52884e57a43cef396fbcff061c4c1de68e2e8fba751e51a14e59c6a6789eae0`  
		Last Modified: Mon, 28 Apr 2025 22:18:09 GMT  
		Size: 39.2 MB (39179322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb2bd74cbc7feaea36a2fc9c184bfe53dfc56dba503e4cafb2399f781ee73af`  
		Last Modified: Mon, 28 Apr 2025 22:18:08 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415c78c9fe0bd7a8e209755c9ca5e86a955cabc8fb754ad4bf669615e2414d31`  
		Last Modified: Mon, 28 Apr 2025 22:18:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714df960fd5aba5cbbb3465b7bb701e334649135d3ab1d70d27e018cff762ca3`  
		Last Modified: Mon, 28 Apr 2025 22:18:09 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:caa9e2554cce0d559a5fe8bc3e4129f16482b8b8ee269dfe20fb013122e2a8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f3ad3665c7c51df22341d40878a9d73eb126aab0e73be6c8f9898fc40c3674`

```dockerfile
```

-	Layers:
	-	`sha256:6143354baf92eb00cbcf310a250654d8cd6caddb29084ce4906851bc6549bf57`  
		Last Modified: Mon, 28 Apr 2025 22:18:08 GMT  
		Size: 4.5 MB (4511025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77ba6433fcfe9ee9ba6e613e3516ef167d8bf15a1f1bdaf7b4d96e4ffcee9b68`  
		Last Modified: Mon, 28 Apr 2025 22:18:08 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:b943f63b17154bd38986b4c5b9a0af0249236165f240fa206593314f649b1ac5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7aa895a364c24bc5333629b5a1816b11483daf44788993a081f9c5edfe48c9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43978966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b7dbe4f6ac8195a090a812df32b6c6102401eddf348757eb94b191b8fa9e6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Thu, 16 Jan 2025 12:29:50 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 16 Jan 2025 12:29:50 GMT
VOLUME [/var/lib/influxdb]
# Thu, 16 Jan 2025 12:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d5b5d68d9f3f80ff363fb8fe3e7a2685990aa9ec18892b275d90a98637fd17`  
		Last Modified: Fri, 14 Feb 2025 19:26:25 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41957e5bb968a4cefc35246db18ec3931c853e733e93c5deb740f35f7e84c2e`  
		Last Modified: Fri, 14 Feb 2025 19:26:25 GMT  
		Size: 1.2 MB (1226185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468f4a21923f4bd549c35732446830e62e956dc03cdfd2c2d232f42d0e5009eb`  
		Last Modified: Fri, 14 Feb 2025 19:26:27 GMT  
		Size: 39.1 MB (39123831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb276187bda5db3e631d8724e8f410f96a6fec1390f6e75843194034f808c84`  
		Last Modified: Fri, 14 Feb 2025 19:26:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850540575a0c377c0f3b7ae91868304b5c287a5cb70ace26bbe032383b2c56ea`  
		Last Modified: Fri, 14 Feb 2025 19:26:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfd23d02f8457ddfcf7d4ccf1c6bb08ad6f3a8477e528e6a15a319acf3a2815`  
		Last Modified: Fri, 14 Feb 2025 19:26:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e1b99cf3cd507d164945dbad30697f4c4f94bf12fdda51aaea11b80671fec4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **770.5 KB (770505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcb19022f150720dcbbd3fb3bc4e77d1165c681907c4a05efd4575c0dd7c442`

```dockerfile
```

-	Layers:
	-	`sha256:d0ae2dedf0f0304ff777759becff24e698ec7929051d7ef081197f2c001ced8c`  
		Last Modified: Fri, 14 Feb 2025 19:26:25 GMT  
		Size: 753.9 KB (753866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9454c17edf183df5c9482191597585786c035bd37719a2898cd15830eb5307de`  
		Last Modified: Fri, 14 Feb 2025 19:26:25 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:1fd65c73565a826245d28513e4531cbcefaf0d1beb9fa586ce8ce9c83581acdb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:77eb9b73eab09a5e25d483f1a86c607bd2be980bd019a8a312382c457a01e80b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90841290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1251659de5a02d275e3ca792fb4ba98c79c08f2a600622bfcecd53836f61b509`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Fri, 18 Apr 2025 17:08:47 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
VOLUME [/var/lib/influxdb]
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b539f7bb495299d65038e99a4cb28dd1c755e1f9178a48f740ed3082bc34d5c0`  
		Last Modified: Mon, 28 Apr 2025 22:18:06 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c97b7e6fa251d5dae275d277c07c39911c5e4d6f7a0f89513b6531a85b9068`  
		Last Modified: Mon, 28 Apr 2025 22:18:07 GMT  
		Size: 18.3 MB (18336563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f14d2391e7b15f486b05f74c311006f13f98c12de14cd5f89dd6770fb8959c`  
		Last Modified: Mon, 28 Apr 2025 22:18:06 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a5787dcbaec1910ccef8bd1be8645649637dcc3a838cc310ca50710b95d1ba`  
		Last Modified: Mon, 28 Apr 2025 22:18:06 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:058f14d88300bf831f2f624397a8f245342d9bd9024f1442f6a5e2f7f5823dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4449062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8215f468048e5cc816988d8dcb06ce2cf85e78ccb5354ea6eb63192a4c219d1`

```dockerfile
```

-	Layers:
	-	`sha256:a2b0f2e4b46b1ec3ad33f480c1f381e20abb42141a933ee9f44551904af0092e`  
		Last Modified: Mon, 28 Apr 2025 22:18:06 GMT  
		Size: 4.4 MB (4435996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82ff98e68c2a09d279bd4ff0bcdd5608759f5bfba7934d29d751f3cecb01ec06`  
		Last Modified: Mon, 28 Apr 2025 22:18:06 GMT  
		Size: 13.1 KB (13066 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:b6ea3ca0af12f2149d869e7b7ea23b58fa20604fc826700e1455a4a46d219ae1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8d425a084ed0912e9ddf30b5d05ade40f6808be79f8d6175a0941cb9134e3aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23144077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a51df3dc6384c1687ae74b021bdbbe1cf6a9257e5416f1ac61145fa5afb9fdf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Thu, 16 Jan 2025 12:29:50 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 16 Jan 2025 12:29:50 GMT
VOLUME [/var/lib/influxdb]
# Thu, 16 Jan 2025 12:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4179006b77d77220705fbc7483a58da67581ebd4d5bf829d0980b8db79003f1e`  
		Last Modified: Fri, 14 Feb 2025 19:26:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58f9f665d3c04d6bfaac3ce80ba636ce75ab95470cc0f20d90698dbf0e48a21`  
		Last Modified: Fri, 14 Feb 2025 19:26:27 GMT  
		Size: 1.2 MB (1226190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d69749d5bf90de3587c4ee4cb6bc93c8c06657a9a43bd45349ecbe7e28000`  
		Last Modified: Fri, 14 Feb 2025 19:26:27 GMT  
		Size: 18.3 MB (18290145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b217b49bcf8d231ad0be29e90559a86cf71a7c69d87fbcde6ea9fdc9ce890ed2`  
		Last Modified: Fri, 14 Feb 2025 19:26:27 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e590cc10505815ce504cb35c5a54e6ce48745e9056cf6b663c353770b5eeb6a0`  
		Last Modified: Fri, 14 Feb 2025 19:26:27 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:385c44c35f414aacccfd0fd90122de5dcb8706bc694ec77acaf9d80ae8776998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.4 KB (694381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc4b6a2d5ac10fc20928d4a5b82a01a829e534b21e680965701b6545cb66b52`

```dockerfile
```

-	Layers:
	-	`sha256:378232aa4317d5845a82468b7359c114b7de78c9e5aaef9a5f7edf1a453b434a`  
		Last Modified: Fri, 14 Feb 2025 19:26:27 GMT  
		Size: 679.4 KB (679371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f443301cf502af1ad2d1bf6dc40192ee84a3ae01f7351cb118a6d2f8c6ff619`  
		Last Modified: Fri, 14 Feb 2025 19:26:26 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8`

```console
$ docker pull influxdb@sha256:94a49b5a61133bd4a1ecb2f38834db269e650319396155dd45849dc3ade9a7a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:a13ef5e5c430e9db2abe0c0bcd01978a72198f0ef9de9b24b21fb2cd11f18174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116156659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866344fcd40677a9d9ca7d283e495ff4d848db3f1dc0e6b21e11ae52dcab6126`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ARG INFLUXDB_VERSION=1.11.8
# Fri, 18 Apr 2025 17:08:47 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
VOLUME [/var/lib/influxdb]
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
USER influxdb
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fefe14e102038e78e20a115f008c031e3c3e96c2e77e7f7376446763fc28fb7`  
		Last Modified: Mon, 28 Apr 2025 22:18:01 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966d2d230cc562a21baafb245a1a1bab566bed7aae54dedf03b273dadd8f4b39`  
		Last Modified: Mon, 28 Apr 2025 22:18:02 GMT  
		Size: 43.7 MB (43651364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371c10d9fe511cbff3235e7a119d07b3324912f8f99d9c5f29cf5c0c933516e5`  
		Last Modified: Mon, 28 Apr 2025 22:18:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b07d638cefee5c37c8998152872da139940a19f150fe06cda7f7631ef8fb9a6`  
		Last Modified: Mon, 28 Apr 2025 22:18:01 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add44ec0f9db3f00aeec425b060a2d5a44b91334276f4aa1e398eac9538944fb`  
		Last Modified: Mon, 28 Apr 2025 22:18:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:cbaef94be206b5c056d3e4dd54e672dd817fec7003d16d502dec881138e50afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4900642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754579a892d8389485d7a79ff7269ccc3acb4c13eb7ed64aafae257b8df65213`

```dockerfile
```

-	Layers:
	-	`sha256:da7a558bff723c7ca0bef362986720a2987fb96a12778ccfa3ed9e03e8f40d1f`  
		Last Modified: Mon, 28 Apr 2025 22:18:01 GMT  
		Size: 4.9 MB (4885113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c586946812b0db92b44664b8e35450a52316508c521560113066aba031117292`  
		Last Modified: Mon, 28 Apr 2025 22:18:01 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4bdc93e676b312056e4bea9ff6cf3f949bb3c59b22baf5aedab705bda6602a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112994104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f473f89a709507dafcb68452f89b945a6094c6ed86a237b33658274ab6daef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ARG INFLUXDB_VERSION=1.11.8
# Fri, 18 Apr 2025 17:08:47 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
VOLUME [/var/lib/influxdb]
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
USER influxdb
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7230da96acdc94e3f8d8734018cbe4356ea9e8cfa51f70bd0af80b6fe62f4e9`  
		Last Modified: Tue, 29 Apr 2025 19:03:33 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf9366b03aca06d7efa8e8a2431e785d468f64d28466453e4a314302f67b9d6`  
		Last Modified: Tue, 29 Apr 2025 19:03:35 GMT  
		Size: 41.1 MB (41119293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e6e3994447bf40bc2a3f6a7363620746307f567f86ba748d729abe46927066`  
		Last Modified: Tue, 29 Apr 2025 19:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f753b82db118c2a83a645110e36e028a38339203966ac3e3642c01d25bbf63`  
		Last Modified: Tue, 29 Apr 2025 19:03:34 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a230f3c7034cf12b98d77f24e6e50dba499eafee7057eddb91ebd16100faebc5`  
		Last Modified: Tue, 29 Apr 2025 19:03:34 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:da41dbb32ea141cb9e9398304c9bac55b671e64f72d17effa264db3c83bedf87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4900202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1323747a43fd182d2e34510446e4dbc4f8b64c1d33b1622875303d130d6184`

```dockerfile
```

-	Layers:
	-	`sha256:0a0501fc8b5e41ceb49ad17a5571cb6d67a84587b324113e2d8513ed2c128cbb`  
		Last Modified: Tue, 29 Apr 2025 19:03:34 GMT  
		Size: 4.9 MB (4884578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:230bc931e6f3434e5ddb0c866e30663d3d267b0a7ac0791db14f25c2825a1970`  
		Last Modified: Tue, 29 Apr 2025 19:03:33 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-alpine`

```console
$ docker pull influxdb@sha256:296f6b84023644996087634e52ace8ce166072f4cf4d3de134cf3d12a4e14daf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9f82853b44202c9b9543797da922fc200a11fb4d3ab3802919fcbd8b30d2885f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42924012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffa1d079420b9dd6b45c1eb667d6cbe07765e63ca3a9ddcf17a94469a235052`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 16 Jan 2025 12:29:50 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 16 Jan 2025 12:29:50 GMT
VOLUME [/var/lib/influxdb]
# Thu, 16 Jan 2025 12:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
USER influxdb
# Thu, 16 Jan 2025 12:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2430b91d27c94577a29aa4a63bc67b9a6bdb38f557ff03f2f47fe9fc4912a6e6`  
		Last Modified: Fri, 14 Feb 2025 19:26:19 GMT  
		Size: 1.2 MB (1226180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccd48b38856008daab1f21e8835b3d7b372598317d42820fc3f047db607ccec`  
		Last Modified: Fri, 14 Feb 2025 19:26:20 GMT  
		Size: 38.1 MB (38068218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94026e2b0d6f99fed3dedfb812a03fd046e8373145be2b2e4aee6b44295f325`  
		Last Modified: Fri, 14 Feb 2025 19:26:19 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfc22a651b18903f12176ed3447abf101612d8f6c009dde4beb5d65b864ff40`  
		Last Modified: Fri, 14 Feb 2025 19:26:19 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff30a98894f91ab375651dec55dbdaa6676482eba3ae74a247a1227bf992e1e`  
		Last Modified: Fri, 14 Feb 2025 19:26:20 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02c49477a92d638620b098485571f719849cc4a14d1a0bbbf9475ac5036c368`  
		Last Modified: Fri, 14 Feb 2025 19:26:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:6aece94c98efbd06cabb8c240362992a7c541ea528326d78f89f00453903db3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **761.2 KB (761197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eef1547a75ac110ec9e8b88fd14d8f8ee24dd109fffd7b1076e0e570262c36f`

```dockerfile
```

-	Layers:
	-	`sha256:71bf4ec5268dedf5ca4c30a6a5925e7e457bde1e6459d68581c4f78a5cc814d2`  
		Last Modified: Fri, 14 Feb 2025 19:26:19 GMT  
		Size: 743.3 KB (743321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f642c9f83ff2a959cec65a14ea556a5c772b8a03eecfc06b77b2212dd3f8fc78`  
		Last Modified: Fri, 14 Feb 2025 19:26:19 GMT  
		Size: 17.9 KB (17876 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:953b49df68a85bd7a4249179427f2ccf7a32492077fbaaf76086aefdaafd3b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40946457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57e22fed09a879e6c6b210345d03839c734d7a58a78a1bca8458178333a8b67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 16 Jan 2025 12:29:50 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 16 Jan 2025 12:29:50 GMT
VOLUME [/var/lib/influxdb]
# Thu, 16 Jan 2025 12:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
USER influxdb
# Thu, 16 Jan 2025 12:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e30a0c587fbc2e84c1b8c55a170ea149c6f6fb91469699f82a5d44e4dad9fdf`  
		Last Modified: Fri, 14 Feb 2025 23:51:00 GMT  
		Size: 1.3 MB (1307075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aedc2e6ed32b6b172146ed1536e1bc4675e2368a442a55fcbc77d582da9ded`  
		Last Modified: Fri, 14 Feb 2025 23:51:01 GMT  
		Size: 35.5 MB (35545506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f6a37ff4f04b2e3f6d6663dc1ad32dca8556db22f6aba5fa140293e06b8be6`  
		Last Modified: Fri, 14 Feb 2025 23:50:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e42b050238199a9cf809362968a20163c7d745329b332b4c122d9810b828e2`  
		Last Modified: Fri, 14 Feb 2025 23:51:00 GMT  
		Size: 995.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afc13286215e26f9388e94e989e8e7f25e3ba851d010c09add249a03c7801ee`  
		Last Modified: Fri, 14 Feb 2025 23:51:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644f23186760a8bda37888b6b2a4baf18413763b0df806f478204d981fb50ef4`  
		Last Modified: Fri, 14 Feb 2025 23:51:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:860c8f802880c137e332828aa61d9ed176550fd869d022ee7e855884da8be5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.5 KB (760532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f42dd545635dc9ef0090a95d89b4d81befa789af9e32c92013b929fff3ef08`

```dockerfile
```

-	Layers:
	-	`sha256:f4f18639c44a9d2627db6142d1f0777cada87e232e3b63751f110640b89a6e51`  
		Last Modified: Fri, 14 Feb 2025 23:51:00 GMT  
		Size: 742.5 KB (742548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b1bc5d6ee15c6f1c9cb67454a907a5fafdc070f8a6cfd9143ff759f6ff93bd`  
		Last Modified: Fri, 14 Feb 2025 23:50:59 GMT  
		Size: 18.0 KB (17984 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-data`

```console
$ docker pull influxdb@sha256:8ecaef75f8c0bb89d35d6805d91cdbbc928350044c004480fd92a487c34d774f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:64c51dc476e2e465503c527f6d27da53e8257f05413c277ebf3f98e273fb0d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111685244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5edc9b10be52efb489f6691964fcab404e708e54bc2db68cf6b9cd62608be5ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Fri, 18 Apr 2025 17:08:47 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
VOLUME [/var/lib/influxdb]
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6149e1950349e0c9f9a5854ac506edf5d45fe1c302b2dbd705d495efaf2f0f21`  
		Last Modified: Mon, 28 Apr 2025 22:18:07 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52884e57a43cef396fbcff061c4c1de68e2e8fba751e51a14e59c6a6789eae0`  
		Last Modified: Mon, 28 Apr 2025 22:18:09 GMT  
		Size: 39.2 MB (39179322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb2bd74cbc7feaea36a2fc9c184bfe53dfc56dba503e4cafb2399f781ee73af`  
		Last Modified: Mon, 28 Apr 2025 22:18:08 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415c78c9fe0bd7a8e209755c9ca5e86a955cabc8fb754ad4bf669615e2414d31`  
		Last Modified: Mon, 28 Apr 2025 22:18:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714df960fd5aba5cbbb3465b7bb701e334649135d3ab1d70d27e018cff762ca3`  
		Last Modified: Mon, 28 Apr 2025 22:18:09 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:caa9e2554cce0d559a5fe8bc3e4129f16482b8b8ee269dfe20fb013122e2a8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f3ad3665c7c51df22341d40878a9d73eb126aab0e73be6c8f9898fc40c3674`

```dockerfile
```

-	Layers:
	-	`sha256:6143354baf92eb00cbcf310a250654d8cd6caddb29084ce4906851bc6549bf57`  
		Last Modified: Mon, 28 Apr 2025 22:18:08 GMT  
		Size: 4.5 MB (4511025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77ba6433fcfe9ee9ba6e613e3516ef167d8bf15a1f1bdaf7b4d96e4ffcee9b68`  
		Last Modified: Mon, 28 Apr 2025 22:18:08 GMT  
		Size: 14.7 KB (14708 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-data-alpine`

```console
$ docker pull influxdb@sha256:b943f63b17154bd38986b4c5b9a0af0249236165f240fa206593314f649b1ac5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7aa895a364c24bc5333629b5a1816b11483daf44788993a081f9c5edfe48c9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43978966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b7dbe4f6ac8195a090a812df32b6c6102401eddf348757eb94b191b8fa9e6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Thu, 16 Jan 2025 12:29:50 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 16 Jan 2025 12:29:50 GMT
VOLUME [/var/lib/influxdb]
# Thu, 16 Jan 2025 12:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d5b5d68d9f3f80ff363fb8fe3e7a2685990aa9ec18892b275d90a98637fd17`  
		Last Modified: Fri, 14 Feb 2025 19:26:25 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41957e5bb968a4cefc35246db18ec3931c853e733e93c5deb740f35f7e84c2e`  
		Last Modified: Fri, 14 Feb 2025 19:26:25 GMT  
		Size: 1.2 MB (1226185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468f4a21923f4bd549c35732446830e62e956dc03cdfd2c2d232f42d0e5009eb`  
		Last Modified: Fri, 14 Feb 2025 19:26:27 GMT  
		Size: 39.1 MB (39123831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb276187bda5db3e631d8724e8f410f96a6fec1390f6e75843194034f808c84`  
		Last Modified: Fri, 14 Feb 2025 19:26:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850540575a0c377c0f3b7ae91868304b5c287a5cb70ace26bbe032383b2c56ea`  
		Last Modified: Fri, 14 Feb 2025 19:26:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfd23d02f8457ddfcf7d4ccf1c6bb08ad6f3a8477e528e6a15a319acf3a2815`  
		Last Modified: Fri, 14 Feb 2025 19:26:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e1b99cf3cd507d164945dbad30697f4c4f94bf12fdda51aaea11b80671fec4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **770.5 KB (770505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcb19022f150720dcbbd3fb3bc4e77d1165c681907c4a05efd4575c0dd7c442`

```dockerfile
```

-	Layers:
	-	`sha256:d0ae2dedf0f0304ff777759becff24e698ec7929051d7ef081197f2c001ced8c`  
		Last Modified: Fri, 14 Feb 2025 19:26:25 GMT  
		Size: 753.9 KB (753866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9454c17edf183df5c9482191597585786c035bd37719a2898cd15830eb5307de`  
		Last Modified: Fri, 14 Feb 2025 19:26:25 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-meta`

```console
$ docker pull influxdb@sha256:1fd65c73565a826245d28513e4531cbcefaf0d1beb9fa586ce8ce9c83581acdb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:77eb9b73eab09a5e25d483f1a86c607bd2be980bd019a8a312382c457a01e80b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90841290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1251659de5a02d275e3ca792fb4ba98c79c08f2a600622bfcecd53836f61b509`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Fri, 18 Apr 2025 17:08:47 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
VOLUME [/var/lib/influxdb]
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b539f7bb495299d65038e99a4cb28dd1c755e1f9178a48f740ed3082bc34d5c0`  
		Last Modified: Mon, 28 Apr 2025 22:18:06 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c97b7e6fa251d5dae275d277c07c39911c5e4d6f7a0f89513b6531a85b9068`  
		Last Modified: Mon, 28 Apr 2025 22:18:07 GMT  
		Size: 18.3 MB (18336563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f14d2391e7b15f486b05f74c311006f13f98c12de14cd5f89dd6770fb8959c`  
		Last Modified: Mon, 28 Apr 2025 22:18:06 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a5787dcbaec1910ccef8bd1be8645649637dcc3a838cc310ca50710b95d1ba`  
		Last Modified: Mon, 28 Apr 2025 22:18:06 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:058f14d88300bf831f2f624397a8f245342d9bd9024f1442f6a5e2f7f5823dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4449062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8215f468048e5cc816988d8dcb06ce2cf85e78ccb5354ea6eb63192a4c219d1`

```dockerfile
```

-	Layers:
	-	`sha256:a2b0f2e4b46b1ec3ad33f480c1f381e20abb42141a933ee9f44551904af0092e`  
		Last Modified: Mon, 28 Apr 2025 22:18:06 GMT  
		Size: 4.4 MB (4435996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82ff98e68c2a09d279bd4ff0bcdd5608759f5bfba7934d29d751f3cecb01ec06`  
		Last Modified: Mon, 28 Apr 2025 22:18:06 GMT  
		Size: 13.1 KB (13066 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-meta-alpine`

```console
$ docker pull influxdb@sha256:b6ea3ca0af12f2149d869e7b7ea23b58fa20604fc826700e1455a4a46d219ae1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8d425a084ed0912e9ddf30b5d05ade40f6808be79f8d6175a0941cb9134e3aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23144077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a51df3dc6384c1687ae74b021bdbbe1cf6a9257e5416f1ac61145fa5afb9fdf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Thu, 16 Jan 2025 12:29:50 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 16 Jan 2025 12:29:50 GMT
VOLUME [/var/lib/influxdb]
# Thu, 16 Jan 2025 12:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4179006b77d77220705fbc7483a58da67581ebd4d5bf829d0980b8db79003f1e`  
		Last Modified: Fri, 14 Feb 2025 19:26:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58f9f665d3c04d6bfaac3ce80ba636ce75ab95470cc0f20d90698dbf0e48a21`  
		Last Modified: Fri, 14 Feb 2025 19:26:27 GMT  
		Size: 1.2 MB (1226190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d69749d5bf90de3587c4ee4cb6bc93c8c06657a9a43bd45349ecbe7e28000`  
		Last Modified: Fri, 14 Feb 2025 19:26:27 GMT  
		Size: 18.3 MB (18290145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b217b49bcf8d231ad0be29e90559a86cf71a7c69d87fbcde6ea9fdc9ce890ed2`  
		Last Modified: Fri, 14 Feb 2025 19:26:27 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e590cc10505815ce504cb35c5a54e6ce48745e9056cf6b663c353770b5eeb6a0`  
		Last Modified: Fri, 14 Feb 2025 19:26:27 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:385c44c35f414aacccfd0fd90122de5dcb8706bc694ec77acaf9d80ae8776998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.4 KB (694381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc4b6a2d5ac10fc20928d4a5b82a01a829e534b21e680965701b6545cb66b52`

```dockerfile
```

-	Layers:
	-	`sha256:378232aa4317d5845a82468b7359c114b7de78c9e5aaef9a5f7edf1a453b434a`  
		Last Modified: Fri, 14 Feb 2025 19:26:27 GMT  
		Size: 679.4 KB (679371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f443301cf502af1ad2d1bf6dc40192ee84a3ae01f7351cb118a6d2f8c6ff619`  
		Last Modified: Fri, 14 Feb 2025 19:26:26 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:c33ac14af66fee77fe5ba14d7ae3b7d7bdc53186cc589eceb413af9f02ca01a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:7be7e75f358cc9a41498b774a217457862e26b9fb0add2fb807cc8eeff8b09b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168645172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2def43b479b5213296cf94cc546f6d13f0b60f6891d9ba5034f5fb93f82c87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 21 May 2025 19:23:38 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV GOSU_VER=1.16
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e42863fbf917dba1d766836b81770e15967448a3c6410d92e950ddecac6c55`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 9.8 MB (9790933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfbdcc44decf955f1d649b2ee7fb1dbfa1c71998d36496387259861082068cf`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dbeb28e9b9a5ac6bd7dc5f4e1a0492b48dee1b297b7960b9dbb5e70cfd316f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619522457ecb94cbc0e36611bbb2312d35b8ca38bac40596c4e5965a64ff6e6f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 1.0 MB (1006372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d3e2d4d64dbe43902a5d0f793e7bef3eea64d5a22f519ea3c4f36b8a78144b`  
		Last Modified: Wed, 21 May 2025 21:01:37 GMT  
		Size: 100.2 MB (100242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701cad0e28464a9b1c3f5196d8bfcdc50fd2bec501bb8fe30f5b0c3f1bb7fcb7`  
		Last Modified: Wed, 21 May 2025 21:01:37 GMT  
		Size: 23.5 MB (23546398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c58b87f333a4d73eea79083aa2294f7753b04c402a321e6098ef7a67dab54`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6393554df92840606b3ffe8e897b394b7ce2b681cffd41f3e170a9446dc089`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc25c80f073d68bad44122268fd1a57631febec15ee6b544d34975ce4773ec4`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:31ffdab1dcfa7b7027482c046340e0e4e3d3d5f746b81f0e5e25c81d8fe2bef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2902904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47429ba26e292482bceec4cdf8dbb0dca3795338f22c3030a890ac85d4ee8df`

```dockerfile
```

-	Layers:
	-	`sha256:b80c4678d52151bdba2ddadbec502eaf3df048dad8cdd7e73316f85c619a910c`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 2.9 MB (2869086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef63408be21053676231c89cbda0f54072a30c09521bb38c546f3823423a68f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 33.8 KB (33818 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0839cb088f4a243f06560a4851d14ee7522263cce0b700cf84b53dd97ca900ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162301307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4045d580c6b33dc7f3056070fb3056024446dedf2f454fb9ac18669087e55c06`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 21 May 2025 19:23:38 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV GOSU_VER=1.16
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b410a06ce4fcda8c631e50621e6543d50ed900c819663b8e8c41c7f7ac89053`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 9.6 MB (9588509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de0fff97c4cf200ca210ae20785978cda6a042a650e28db59b324b44f41f905`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806918d354e310d08b135e40f2e2d26fcd65062af8700b837f4aa84de0482de6`  
		Last Modified: Wed, 21 May 2025 21:02:06 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dd02a48352d53c118b216ffe4dbce8cea9676dd3da4bebf4dcefc7d299a03c`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 936.1 KB (936100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc6e61093af6624558cddc2362654c606748ecb54cee1a3486c6098cdbfed22`  
		Last Modified: Wed, 21 May 2025 21:02:11 GMT  
		Size: 96.0 MB (96038376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae02942e730c824aa6fbe30374d5af1dd7d72e7c8c4c9a0298374f5c6962c87c`  
		Last Modified: Wed, 21 May 2025 21:02:09 GMT  
		Size: 22.2 MB (22197938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b32a406b9d356f60656a71f8e36b9f9bcf243eaf723901c78828482765101a`  
		Last Modified: Wed, 21 May 2025 21:02:08 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9872dc5e700b80dd89f142c8e61e7c3f60a789e35de74d0c0f4321b48245b58`  
		Last Modified: Wed, 21 May 2025 21:02:08 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f917e572fef7a9039d0ba795a86b841215a450065b9e2e783189157ef6e19122`  
		Last Modified: Wed, 21 May 2025 21:02:09 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:f0906a5dd25bedffed8866016cdbe9b64eeb5e6c3d11c522f74a73e616785680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2902315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ceac7e7fd2dc69af9be74f65c2a4737611300d774979a37d6dc13f6695244d`

```dockerfile
```

-	Layers:
	-	`sha256:1e76d058079ee2ce737fe5009b78a9362df4797f206fcf557ce706df337fde24`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 2.9 MB (2868314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f554075615356b4d24f3930e6ac1ae2742ffae4bbd677ce1846d300062b29382`  
		Last Modified: Wed, 21 May 2025 21:02:06 GMT  
		Size: 34.0 KB (34001 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:a7a9e96c9bfc443a79d13e2b1989dc43608eb5b6c06fec6d30651ca5f8219330
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cbee5988f47dfa92bea7f72ff9e0fb07ba7956ead0141dc2ab27245b31f4f105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92785945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ade717ac7e624b9847ff64fa2b0f29775c53f8ea1418f8ec9c486ffc444719a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 21 May 2025 19:23:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b4da6257d4dab81f7ea9b217e8990fa02b532b487dc09f66cfe66b7a5ab1b7`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f227616a4b65630020272b1a4736c45d2072fea1f6ae56d8987f001bff1868e5`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 9.7 MB (9668254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28153e71486f54b7e2d6898878271446058952c9919aaad4310fd5662e14073`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 5.8 MB (5820951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17da966601b69ee27cf7e07f71e8d3a293465f510f662a95761c204c476039`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f351545292c8d4b32b561f37f2761b8143e35ea7b2aed6ada764d91675953e2`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 50.1 MB (50115457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec39c678e278ff055d4d22e8402129df928caa4a2647ff3024e97721f0f5943`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 23.5 MB (23546414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428d400809cb7ad31d35a7f2d948c8121b3f7499c617f94eb95080f6705d2c6`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195b609b670962adf4a4fd55112b8f3ee09ab9b864b63db78893c7e7b6de06aa`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213bcca749f51ef7f5ebe65ef3ee91941b8ead606c2179e2247bba98e5d1ba1`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:07a190e7a4e44a2d2349ddf22bcf6a411cb327788d87cbe24dfbfb319e2346ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.5 KB (949513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0face7c412448d24ef27a189fc81813532f5930f3f6a820e3311b431cb71a2`

```dockerfile
```

-	Layers:
	-	`sha256:dc8858c4baeaf5b780566e1f56dac4769e4c5fb4a00452d59c94970c80b6638d`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 918.5 KB (918468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15b588c6b6124a1aa918ae48f879aa8e721ecd2db834e3c78af76a20738c283`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 31.0 KB (31045 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:acd117211c431790fc6d016c91eec85d13c132bf2179149dd9c1163fd5b36f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89567348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f25c6a394b54e0d7afd6e4960b11cc3c7389d6a99abd4edc658192b2ed4782b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 21 May 2025 19:23:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c8ed1b411bf87e31d51dcd5e11ad29b842c6ac23d29867f58c9b6657217f9`  
		Last Modified: Tue, 06 May 2025 02:07:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7581744a5f8b851a37b006b9f70c0dfc1aabfbbf6e54e0d468d11332b9a89155`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 9.8 MB (9790275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8e2420533fb94a98c3c0cea702d65af3aac200564d71bf02039933d45752c4`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d98ff612225a614c58f5f650b55a20d2a5f607933c56ec0b343dc54d39316`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9943be5d4ecac40794357058ec1ead2ffe57b93ad82f1c046f9490950fb8be`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 48.0 MB (48016208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592941019971dc33dba5c666bebc57139662a00acd86e6dc6e85310542b62a90`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 22.2 MB (22197933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a652dc6c421b2c1298eb71f3a1a77ad5317359d42f97d2ba7e0256166f7908`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c5c55779859032454928168c0eaf5620289e22d09443a4c303e920fbc0f25e`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c5a87a5ee69568a4bb3e3c7fbcb83b0bd9250e68ef8618525ab0df87a7c0`  
		Last Modified: Wed, 21 May 2025 21:02:38 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:729a0121b69401596161e2c26bec6508731ab99a75514774f24c6af6bfc18323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.0 KB (948960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c122a9ee58ab54b906e11b0f4efc6fa24ec9862171d48194a1c13655341895`

```dockerfile
```

-	Layers:
	-	`sha256:5f2a9ab7569906dc8b16cb3c30fa1f29afe85dc187f764fa5f1821fc5d6848ec`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 917.7 KB (917719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f4f5e2584d7feb4ec7fc289bad890abb4f9f813f7c20ca231fb580b0db01d6d`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 31.2 KB (31241 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:c33ac14af66fee77fe5ba14d7ae3b7d7bdc53186cc589eceb413af9f02ca01a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:7be7e75f358cc9a41498b774a217457862e26b9fb0add2fb807cc8eeff8b09b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168645172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2def43b479b5213296cf94cc546f6d13f0b60f6891d9ba5034f5fb93f82c87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 21 May 2025 19:23:38 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV GOSU_VER=1.16
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e42863fbf917dba1d766836b81770e15967448a3c6410d92e950ddecac6c55`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 9.8 MB (9790933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfbdcc44decf955f1d649b2ee7fb1dbfa1c71998d36496387259861082068cf`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dbeb28e9b9a5ac6bd7dc5f4e1a0492b48dee1b297b7960b9dbb5e70cfd316f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619522457ecb94cbc0e36611bbb2312d35b8ca38bac40596c4e5965a64ff6e6f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 1.0 MB (1006372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d3e2d4d64dbe43902a5d0f793e7bef3eea64d5a22f519ea3c4f36b8a78144b`  
		Last Modified: Wed, 21 May 2025 21:01:37 GMT  
		Size: 100.2 MB (100242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701cad0e28464a9b1c3f5196d8bfcdc50fd2bec501bb8fe30f5b0c3f1bb7fcb7`  
		Last Modified: Wed, 21 May 2025 21:01:37 GMT  
		Size: 23.5 MB (23546398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c58b87f333a4d73eea79083aa2294f7753b04c402a321e6098ef7a67dab54`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6393554df92840606b3ffe8e897b394b7ce2b681cffd41f3e170a9446dc089`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc25c80f073d68bad44122268fd1a57631febec15ee6b544d34975ce4773ec4`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:31ffdab1dcfa7b7027482c046340e0e4e3d3d5f746b81f0e5e25c81d8fe2bef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2902904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47429ba26e292482bceec4cdf8dbb0dca3795338f22c3030a890ac85d4ee8df`

```dockerfile
```

-	Layers:
	-	`sha256:b80c4678d52151bdba2ddadbec502eaf3df048dad8cdd7e73316f85c619a910c`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 2.9 MB (2869086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef63408be21053676231c89cbda0f54072a30c09521bb38c546f3823423a68f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 33.8 KB (33818 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0839cb088f4a243f06560a4851d14ee7522263cce0b700cf84b53dd97ca900ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162301307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4045d580c6b33dc7f3056070fb3056024446dedf2f454fb9ac18669087e55c06`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 21 May 2025 19:23:38 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV GOSU_VER=1.16
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b410a06ce4fcda8c631e50621e6543d50ed900c819663b8e8c41c7f7ac89053`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 9.6 MB (9588509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de0fff97c4cf200ca210ae20785978cda6a042a650e28db59b324b44f41f905`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806918d354e310d08b135e40f2e2d26fcd65062af8700b837f4aa84de0482de6`  
		Last Modified: Wed, 21 May 2025 21:02:06 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dd02a48352d53c118b216ffe4dbce8cea9676dd3da4bebf4dcefc7d299a03c`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 936.1 KB (936100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc6e61093af6624558cddc2362654c606748ecb54cee1a3486c6098cdbfed22`  
		Last Modified: Wed, 21 May 2025 21:02:11 GMT  
		Size: 96.0 MB (96038376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae02942e730c824aa6fbe30374d5af1dd7d72e7c8c4c9a0298374f5c6962c87c`  
		Last Modified: Wed, 21 May 2025 21:02:09 GMT  
		Size: 22.2 MB (22197938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b32a406b9d356f60656a71f8e36b9f9bcf243eaf723901c78828482765101a`  
		Last Modified: Wed, 21 May 2025 21:02:08 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9872dc5e700b80dd89f142c8e61e7c3f60a789e35de74d0c0f4321b48245b58`  
		Last Modified: Wed, 21 May 2025 21:02:08 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f917e572fef7a9039d0ba795a86b841215a450065b9e2e783189157ef6e19122`  
		Last Modified: Wed, 21 May 2025 21:02:09 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:f0906a5dd25bedffed8866016cdbe9b64eeb5e6c3d11c522f74a73e616785680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2902315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ceac7e7fd2dc69af9be74f65c2a4737611300d774979a37d6dc13f6695244d`

```dockerfile
```

-	Layers:
	-	`sha256:1e76d058079ee2ce737fe5009b78a9362df4797f206fcf557ce706df337fde24`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 2.9 MB (2868314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f554075615356b4d24f3930e6ac1ae2742ffae4bbd677ce1846d300062b29382`  
		Last Modified: Wed, 21 May 2025 21:02:06 GMT  
		Size: 34.0 KB (34001 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:a7a9e96c9bfc443a79d13e2b1989dc43608eb5b6c06fec6d30651ca5f8219330
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cbee5988f47dfa92bea7f72ff9e0fb07ba7956ead0141dc2ab27245b31f4f105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92785945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ade717ac7e624b9847ff64fa2b0f29775c53f8ea1418f8ec9c486ffc444719a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 21 May 2025 19:23:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b4da6257d4dab81f7ea9b217e8990fa02b532b487dc09f66cfe66b7a5ab1b7`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f227616a4b65630020272b1a4736c45d2072fea1f6ae56d8987f001bff1868e5`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 9.7 MB (9668254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28153e71486f54b7e2d6898878271446058952c9919aaad4310fd5662e14073`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 5.8 MB (5820951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17da966601b69ee27cf7e07f71e8d3a293465f510f662a95761c204c476039`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f351545292c8d4b32b561f37f2761b8143e35ea7b2aed6ada764d91675953e2`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 50.1 MB (50115457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec39c678e278ff055d4d22e8402129df928caa4a2647ff3024e97721f0f5943`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 23.5 MB (23546414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428d400809cb7ad31d35a7f2d948c8121b3f7499c617f94eb95080f6705d2c6`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195b609b670962adf4a4fd55112b8f3ee09ab9b864b63db78893c7e7b6de06aa`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213bcca749f51ef7f5ebe65ef3ee91941b8ead606c2179e2247bba98e5d1ba1`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:07a190e7a4e44a2d2349ddf22bcf6a411cb327788d87cbe24dfbfb319e2346ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.5 KB (949513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0face7c412448d24ef27a189fc81813532f5930f3f6a820e3311b431cb71a2`

```dockerfile
```

-	Layers:
	-	`sha256:dc8858c4baeaf5b780566e1f56dac4769e4c5fb4a00452d59c94970c80b6638d`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 918.5 KB (918468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15b588c6b6124a1aa918ae48f879aa8e721ecd2db834e3c78af76a20738c283`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 31.0 KB (31045 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:acd117211c431790fc6d016c91eec85d13c132bf2179149dd9c1163fd5b36f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89567348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f25c6a394b54e0d7afd6e4960b11cc3c7389d6a99abd4edc658192b2ed4782b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 21 May 2025 19:23:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c8ed1b411bf87e31d51dcd5e11ad29b842c6ac23d29867f58c9b6657217f9`  
		Last Modified: Tue, 06 May 2025 02:07:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7581744a5f8b851a37b006b9f70c0dfc1aabfbbf6e54e0d468d11332b9a89155`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 9.8 MB (9790275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8e2420533fb94a98c3c0cea702d65af3aac200564d71bf02039933d45752c4`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d98ff612225a614c58f5f650b55a20d2a5f607933c56ec0b343dc54d39316`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9943be5d4ecac40794357058ec1ead2ffe57b93ad82f1c046f9490950fb8be`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 48.0 MB (48016208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592941019971dc33dba5c666bebc57139662a00acd86e6dc6e85310542b62a90`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 22.2 MB (22197933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a652dc6c421b2c1298eb71f3a1a77ad5317359d42f97d2ba7e0256166f7908`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c5c55779859032454928168c0eaf5620289e22d09443a4c303e920fbc0f25e`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c5a87a5ee69568a4bb3e3c7fbcb83b0bd9250e68ef8618525ab0df87a7c0`  
		Last Modified: Wed, 21 May 2025 21:02:38 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:729a0121b69401596161e2c26bec6508731ab99a75514774f24c6af6bfc18323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.0 KB (948960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c122a9ee58ab54b906e11b0f4efc6fa24ec9862171d48194a1c13655341895`

```dockerfile
```

-	Layers:
	-	`sha256:5f2a9ab7569906dc8b16cb3c30fa1f29afe85dc187f764fa5f1821fc5d6848ec`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 917.7 KB (917719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f4f5e2584d7feb4ec7fc289bad890abb4f9f813f7c20ca231fb580b0db01d6d`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 31.2 KB (31241 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.11-alpine`

```console
$ docker pull influxdb@sha256:a7a9e96c9bfc443a79d13e2b1989dc43608eb5b6c06fec6d30651ca5f8219330
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cbee5988f47dfa92bea7f72ff9e0fb07ba7956ead0141dc2ab27245b31f4f105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92785945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ade717ac7e624b9847ff64fa2b0f29775c53f8ea1418f8ec9c486ffc444719a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 21 May 2025 19:23:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b4da6257d4dab81f7ea9b217e8990fa02b532b487dc09f66cfe66b7a5ab1b7`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f227616a4b65630020272b1a4736c45d2072fea1f6ae56d8987f001bff1868e5`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 9.7 MB (9668254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28153e71486f54b7e2d6898878271446058952c9919aaad4310fd5662e14073`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 5.8 MB (5820951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17da966601b69ee27cf7e07f71e8d3a293465f510f662a95761c204c476039`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f351545292c8d4b32b561f37f2761b8143e35ea7b2aed6ada764d91675953e2`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 50.1 MB (50115457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec39c678e278ff055d4d22e8402129df928caa4a2647ff3024e97721f0f5943`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 23.5 MB (23546414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428d400809cb7ad31d35a7f2d948c8121b3f7499c617f94eb95080f6705d2c6`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195b609b670962adf4a4fd55112b8f3ee09ab9b864b63db78893c7e7b6de06aa`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213bcca749f51ef7f5ebe65ef3ee91941b8ead606c2179e2247bba98e5d1ba1`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:07a190e7a4e44a2d2349ddf22bcf6a411cb327788d87cbe24dfbfb319e2346ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.5 KB (949513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0face7c412448d24ef27a189fc81813532f5930f3f6a820e3311b431cb71a2`

```dockerfile
```

-	Layers:
	-	`sha256:dc8858c4baeaf5b780566e1f56dac4769e4c5fb4a00452d59c94970c80b6638d`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 918.5 KB (918468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15b588c6b6124a1aa918ae48f879aa8e721ecd2db834e3c78af76a20738c283`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 31.0 KB (31045 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:acd117211c431790fc6d016c91eec85d13c132bf2179149dd9c1163fd5b36f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89567348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f25c6a394b54e0d7afd6e4960b11cc3c7389d6a99abd4edc658192b2ed4782b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 21 May 2025 19:23:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c8ed1b411bf87e31d51dcd5e11ad29b842c6ac23d29867f58c9b6657217f9`  
		Last Modified: Tue, 06 May 2025 02:07:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7581744a5f8b851a37b006b9f70c0dfc1aabfbbf6e54e0d468d11332b9a89155`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 9.8 MB (9790275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8e2420533fb94a98c3c0cea702d65af3aac200564d71bf02039933d45752c4`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d98ff612225a614c58f5f650b55a20d2a5f607933c56ec0b343dc54d39316`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9943be5d4ecac40794357058ec1ead2ffe57b93ad82f1c046f9490950fb8be`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 48.0 MB (48016208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592941019971dc33dba5c666bebc57139662a00acd86e6dc6e85310542b62a90`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 22.2 MB (22197933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a652dc6c421b2c1298eb71f3a1a77ad5317359d42f97d2ba7e0256166f7908`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c5c55779859032454928168c0eaf5620289e22d09443a4c303e920fbc0f25e`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c5a87a5ee69568a4bb3e3c7fbcb83b0bd9250e68ef8618525ab0df87a7c0`  
		Last Modified: Wed, 21 May 2025 21:02:38 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:729a0121b69401596161e2c26bec6508731ab99a75514774f24c6af6bfc18323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.0 KB (948960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c122a9ee58ab54b906e11b0f4efc6fa24ec9862171d48194a1c13655341895`

```dockerfile
```

-	Layers:
	-	`sha256:5f2a9ab7569906dc8b16cb3c30fa1f29afe85dc187f764fa5f1821fc5d6848ec`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 917.7 KB (917719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f4f5e2584d7feb4ec7fc289bad890abb4f9f813f7c20ca231fb580b0db01d6d`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 31.2 KB (31241 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12`

```console
$ docker pull influxdb@sha256:c33ac14af66fee77fe5ba14d7ae3b7d7bdc53186cc589eceb413af9f02ca01a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:7be7e75f358cc9a41498b774a217457862e26b9fb0add2fb807cc8eeff8b09b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168645172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2def43b479b5213296cf94cc546f6d13f0b60f6891d9ba5034f5fb93f82c87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 21 May 2025 19:23:38 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV GOSU_VER=1.16
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e42863fbf917dba1d766836b81770e15967448a3c6410d92e950ddecac6c55`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 9.8 MB (9790933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfbdcc44decf955f1d649b2ee7fb1dbfa1c71998d36496387259861082068cf`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dbeb28e9b9a5ac6bd7dc5f4e1a0492b48dee1b297b7960b9dbb5e70cfd316f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619522457ecb94cbc0e36611bbb2312d35b8ca38bac40596c4e5965a64ff6e6f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 1.0 MB (1006372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d3e2d4d64dbe43902a5d0f793e7bef3eea64d5a22f519ea3c4f36b8a78144b`  
		Last Modified: Wed, 21 May 2025 21:01:37 GMT  
		Size: 100.2 MB (100242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701cad0e28464a9b1c3f5196d8bfcdc50fd2bec501bb8fe30f5b0c3f1bb7fcb7`  
		Last Modified: Wed, 21 May 2025 21:01:37 GMT  
		Size: 23.5 MB (23546398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c58b87f333a4d73eea79083aa2294f7753b04c402a321e6098ef7a67dab54`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6393554df92840606b3ffe8e897b394b7ce2b681cffd41f3e170a9446dc089`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc25c80f073d68bad44122268fd1a57631febec15ee6b544d34975ce4773ec4`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:31ffdab1dcfa7b7027482c046340e0e4e3d3d5f746b81f0e5e25c81d8fe2bef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2902904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47429ba26e292482bceec4cdf8dbb0dca3795338f22c3030a890ac85d4ee8df`

```dockerfile
```

-	Layers:
	-	`sha256:b80c4678d52151bdba2ddadbec502eaf3df048dad8cdd7e73316f85c619a910c`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 2.9 MB (2869086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef63408be21053676231c89cbda0f54072a30c09521bb38c546f3823423a68f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 33.8 KB (33818 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0839cb088f4a243f06560a4851d14ee7522263cce0b700cf84b53dd97ca900ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162301307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4045d580c6b33dc7f3056070fb3056024446dedf2f454fb9ac18669087e55c06`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 21 May 2025 19:23:38 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV GOSU_VER=1.16
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b410a06ce4fcda8c631e50621e6543d50ed900c819663b8e8c41c7f7ac89053`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 9.6 MB (9588509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de0fff97c4cf200ca210ae20785978cda6a042a650e28db59b324b44f41f905`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806918d354e310d08b135e40f2e2d26fcd65062af8700b837f4aa84de0482de6`  
		Last Modified: Wed, 21 May 2025 21:02:06 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dd02a48352d53c118b216ffe4dbce8cea9676dd3da4bebf4dcefc7d299a03c`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 936.1 KB (936100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc6e61093af6624558cddc2362654c606748ecb54cee1a3486c6098cdbfed22`  
		Last Modified: Wed, 21 May 2025 21:02:11 GMT  
		Size: 96.0 MB (96038376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae02942e730c824aa6fbe30374d5af1dd7d72e7c8c4c9a0298374f5c6962c87c`  
		Last Modified: Wed, 21 May 2025 21:02:09 GMT  
		Size: 22.2 MB (22197938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b32a406b9d356f60656a71f8e36b9f9bcf243eaf723901c78828482765101a`  
		Last Modified: Wed, 21 May 2025 21:02:08 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9872dc5e700b80dd89f142c8e61e7c3f60a789e35de74d0c0f4321b48245b58`  
		Last Modified: Wed, 21 May 2025 21:02:08 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f917e572fef7a9039d0ba795a86b841215a450065b9e2e783189157ef6e19122`  
		Last Modified: Wed, 21 May 2025 21:02:09 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:f0906a5dd25bedffed8866016cdbe9b64eeb5e6c3d11c522f74a73e616785680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2902315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ceac7e7fd2dc69af9be74f65c2a4737611300d774979a37d6dc13f6695244d`

```dockerfile
```

-	Layers:
	-	`sha256:1e76d058079ee2ce737fe5009b78a9362df4797f206fcf557ce706df337fde24`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 2.9 MB (2868314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f554075615356b4d24f3930e6ac1ae2742ffae4bbd677ce1846d300062b29382`  
		Last Modified: Wed, 21 May 2025 21:02:06 GMT  
		Size: 34.0 KB (34001 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:9aa9e65e851b7bf5f8573765c86dedcf106f6c1c4540e68526c9fc5908d58b64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:0541f1915c0365e216e5c7c9ad359dfd431d659a48ea38fa1b7efe221f971b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97916361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56191da4e4fcb680e5fd37a29a1cc1fbad49e1cc4a48dfac85c1519027fd874`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45d233bca13463d087d78f8628ee0e48246bb2260ddc2e1753b8edf7a60465e`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 6.7 MB (6663446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2335e5ccc6e74199b81cac14d25ef86c600701f0cb179af4909be93c76c0b85`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2929d11995a5be55a68d56cea52f4a5524a83f19a5064bd79181045de67784`  
		Last Modified: Fri, 16 May 2025 19:09:44 GMT  
		Size: 61.5 MB (61531262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b996a11e64194691cec83263137edbf2d5ac286dd80cfba6e8ac9f61e23ccab`  
		Last Modified: Fri, 16 May 2025 19:09:43 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09920d7411dc2b83cd2ba0f66828d637a672c098969a3a96038f742659eb227b`  
		Last Modified: Fri, 16 May 2025 19:09:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4366db6a68771db7c80db70c86d8d352d1700165eaf74db8151308928ef8d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70985cac70f460065e4f4404b8a8792f8871d12d05656a0cce1b4fe5785780f4`

```dockerfile
```

-	Layers:
	-	`sha256:3b47a22f93be6a7ff58cd3e2658f9e3e7024019f24a496b4b7aa3ff56b7799dc`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 2.2 MB (2203240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9822b6a3d8b69e8a72ef5bb1ed07e7e811727df146971621810ba146ae8919`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:672c4a4221b3406da630526e426d4e4b172cb72179262e990e6a88f1d5099f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90509144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2005ef240f1a4c466d0784802963fa2b166ace199af5fc927753457eb3efaee0`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d3ffcca3dea02f4c8adcd31729621ed8d7e4b7531c23b8cac9775f570b5085`  
		Last Modified: Mon, 05 May 2025 21:30:45 GMT  
		Size: 6.7 MB (6674461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f74b4aeea550ca1632e75aa80f8fa8a2ccff90a4138e9f7d1c3d8333e53e3e`  
		Last Modified: Mon, 05 May 2025 21:30:44 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07863461f8e1c5ae19e31f7cd33f989a24208a6e83bbd372b715442c76c7b68d`  
		Last Modified: Fri, 16 May 2025 19:09:16 GMT  
		Size: 55.0 MB (54983680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e77c07210f0fc32bc01a1f689f570f68d1684537afb8272a0a54dbf781f4b8`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5425d10b3656e5aa3b699869d3b14e9890737e5953d97f93c95130ae739417`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3fceef544916459184e06b503c25120d859ee98e6327290ee166e5af44b15f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d106116f0cda0f646738472152eb611a392c3f18d5c2694d15c0d276d62ff03d`

```dockerfile
```

-	Layers:
	-	`sha256:71235520c5b8db6cbc081b11126bd944131d82b49f898244ed2ecd97aadc285b`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 2.2 MB (2204322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3aef4f0be0364f461cbf8d084add55647775f705ca011344adcd716ba88893e`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:268a2553b83bc434f37017e1b8faf2084e8578ce0adaf7ff48f90c856361a640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:0831d74c4536fcf32559efc45387d3c9e86b73298e03eca7365e511205594ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (100001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc6e48be2b2670b9aa821717cbc52bdf388a660d63e36b64e81844f3a811ef2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae520f817f8cab06dd90a7dd53cf0f5913b476bbf6ffb463664d14028482b4c`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 6.7 MB (6663469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f5f6b5a16642b2e7d600a78ccdb14667d4b733c7c67e70d0a34452a74c4b5b`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d09603a0a7affbe9365e383b9441ffe05ca55e340cded8251f267a5f909ced`  
		Last Modified: Fri, 16 May 2025 19:09:37 GMT  
		Size: 63.6 MB (63616620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddb6ae1b11404986ad7cab5ef50d3f063229042eb15b212c2e6df5a7f633995`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96604f7f2839a5948435ec73b7302b4ed49d6b55846cd167beabfe1c67f07189`  
		Last Modified: Fri, 16 May 2025 19:09:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:5d2b290f04c945829b3e9bb07ef592aa47b41e0ee615ebd1e868c9f1765b0f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096fedc4b5d1bdc4329142f4db5c21abc14647db78b832289ce5f15457adf15c`

```dockerfile
```

-	Layers:
	-	`sha256:9a19028d33d179c531cdff08009d86f0f5345b13ab2665008b0c8d9a89339fd0`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 2.2 MB (2203288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f59d10de0920ee5c0b5c0354cc5381868cf5aae0c9c0884d39e6742e41165d3`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:86c3040da8a31671b4a8723820f1fd058dd6daaf4e104ae676cdd35a6c1bfc1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92545538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d4c0472559b432bd42cf220d9af4838c7a6b9e1db0478075582fc04529da76`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d3ffcca3dea02f4c8adcd31729621ed8d7e4b7531c23b8cac9775f570b5085`  
		Last Modified: Mon, 05 May 2025 21:30:45 GMT  
		Size: 6.7 MB (6674461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f74b4aeea550ca1632e75aa80f8fa8a2ccff90a4138e9f7d1c3d8333e53e3e`  
		Last Modified: Mon, 05 May 2025 21:30:44 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8e9105883f39dc1d6116059355f136f26bf486bf75708411cba6b55f073c60`  
		Last Modified: Fri, 16 May 2025 19:09:41 GMT  
		Size: 57.0 MB (57020072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8104228122b89805d5c0dc89a695746c7aca0dd1ef6c3b9d43ca679aa0e66ada`  
		Last Modified: Fri, 16 May 2025 19:09:40 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1db856ab0eb66e0cda8f05e476554e03272928b30687b330db9c0b95718e05`  
		Last Modified: Fri, 16 May 2025 19:09:40 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:bf122adb7f665faeabcaa74c5faa11d6b3858be55e644c790a846648ce95ff1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50ade38012f71c2132eb2363f019fd69211c4b0e9f4f862ba0f78d615b0097b`

```dockerfile
```

-	Layers:
	-	`sha256:75efb097e69e31f377df0f8ecfd45207e2aae47de9bc46fb465060a2c099729c`  
		Last Modified: Fri, 16 May 2025 19:09:40 GMT  
		Size: 2.2 MB (2204370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c3b555aecfe9bc0b48dde231eb7f206df331fe649a5179b17a3c63dd969899e`  
		Last Modified: Fri, 16 May 2025 19:09:39 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.0-core`

```console
$ docker pull influxdb@sha256:9aa9e65e851b7bf5f8573765c86dedcf106f6c1c4540e68526c9fc5908d58b64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.0-core` - linux; amd64

```console
$ docker pull influxdb@sha256:0541f1915c0365e216e5c7c9ad359dfd431d659a48ea38fa1b7efe221f971b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97916361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56191da4e4fcb680e5fd37a29a1cc1fbad49e1cc4a48dfac85c1519027fd874`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45d233bca13463d087d78f8628ee0e48246bb2260ddc2e1753b8edf7a60465e`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 6.7 MB (6663446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2335e5ccc6e74199b81cac14d25ef86c600701f0cb179af4909be93c76c0b85`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2929d11995a5be55a68d56cea52f4a5524a83f19a5064bd79181045de67784`  
		Last Modified: Fri, 16 May 2025 19:09:44 GMT  
		Size: 61.5 MB (61531262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b996a11e64194691cec83263137edbf2d5ac286dd80cfba6e8ac9f61e23ccab`  
		Last Modified: Fri, 16 May 2025 19:09:43 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09920d7411dc2b83cd2ba0f66828d637a672c098969a3a96038f742659eb227b`  
		Last Modified: Fri, 16 May 2025 19:09:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4366db6a68771db7c80db70c86d8d352d1700165eaf74db8151308928ef8d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70985cac70f460065e4f4404b8a8792f8871d12d05656a0cce1b4fe5785780f4`

```dockerfile
```

-	Layers:
	-	`sha256:3b47a22f93be6a7ff58cd3e2658f9e3e7024019f24a496b4b7aa3ff56b7799dc`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 2.2 MB (2203240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9822b6a3d8b69e8a72ef5bb1ed07e7e811727df146971621810ba146ae8919`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.0-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:672c4a4221b3406da630526e426d4e4b172cb72179262e990e6a88f1d5099f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90509144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2005ef240f1a4c466d0784802963fa2b166ace199af5fc927753457eb3efaee0`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d3ffcca3dea02f4c8adcd31729621ed8d7e4b7531c23b8cac9775f570b5085`  
		Last Modified: Mon, 05 May 2025 21:30:45 GMT  
		Size: 6.7 MB (6674461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f74b4aeea550ca1632e75aa80f8fa8a2ccff90a4138e9f7d1c3d8333e53e3e`  
		Last Modified: Mon, 05 May 2025 21:30:44 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07863461f8e1c5ae19e31f7cd33f989a24208a6e83bbd372b715442c76c7b68d`  
		Last Modified: Fri, 16 May 2025 19:09:16 GMT  
		Size: 55.0 MB (54983680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e77c07210f0fc32bc01a1f689f570f68d1684537afb8272a0a54dbf781f4b8`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5425d10b3656e5aa3b699869d3b14e9890737e5953d97f93c95130ae739417`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3fceef544916459184e06b503c25120d859ee98e6327290ee166e5af44b15f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d106116f0cda0f646738472152eb611a392c3f18d5c2694d15c0d276d62ff03d`

```dockerfile
```

-	Layers:
	-	`sha256:71235520c5b8db6cbc081b11126bd944131d82b49f898244ed2ecd97aadc285b`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 2.2 MB (2204322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3aef4f0be0364f461cbf8d084add55647775f705ca011344adcd716ba88893e`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.0-enterprise`

```console
$ docker pull influxdb@sha256:268a2553b83bc434f37017e1b8faf2084e8578ce0adaf7ff48f90c856361a640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.0-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:0831d74c4536fcf32559efc45387d3c9e86b73298e03eca7365e511205594ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (100001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc6e48be2b2670b9aa821717cbc52bdf388a660d63e36b64e81844f3a811ef2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae520f817f8cab06dd90a7dd53cf0f5913b476bbf6ffb463664d14028482b4c`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 6.7 MB (6663469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f5f6b5a16642b2e7d600a78ccdb14667d4b733c7c67e70d0a34452a74c4b5b`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d09603a0a7affbe9365e383b9441ffe05ca55e340cded8251f267a5f909ced`  
		Last Modified: Fri, 16 May 2025 19:09:37 GMT  
		Size: 63.6 MB (63616620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddb6ae1b11404986ad7cab5ef50d3f063229042eb15b212c2e6df5a7f633995`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96604f7f2839a5948435ec73b7302b4ed49d6b55846cd167beabfe1c67f07189`  
		Last Modified: Fri, 16 May 2025 19:09:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:5d2b290f04c945829b3e9bb07ef592aa47b41e0ee615ebd1e868c9f1765b0f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096fedc4b5d1bdc4329142f4db5c21abc14647db78b832289ce5f15457adf15c`

```dockerfile
```

-	Layers:
	-	`sha256:9a19028d33d179c531cdff08009d86f0f5345b13ab2665008b0c8d9a89339fd0`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 2.2 MB (2203288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f59d10de0920ee5c0b5c0354cc5381868cf5aae0c9c0884d39e6742e41165d3`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:86c3040da8a31671b4a8723820f1fd058dd6daaf4e104ae676cdd35a6c1bfc1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92545538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d4c0472559b432bd42cf220d9af4838c7a6b9e1db0478075582fc04529da76`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d3ffcca3dea02f4c8adcd31729621ed8d7e4b7531c23b8cac9775f570b5085`  
		Last Modified: Mon, 05 May 2025 21:30:45 GMT  
		Size: 6.7 MB (6674461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f74b4aeea550ca1632e75aa80f8fa8a2ccff90a4138e9f7d1c3d8333e53e3e`  
		Last Modified: Mon, 05 May 2025 21:30:44 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8e9105883f39dc1d6116059355f136f26bf486bf75708411cba6b55f073c60`  
		Last Modified: Fri, 16 May 2025 19:09:41 GMT  
		Size: 57.0 MB (57020072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8104228122b89805d5c0dc89a695746c7aca0dd1ef6c3b9d43ca679aa0e66ada`  
		Last Modified: Fri, 16 May 2025 19:09:40 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1db856ab0eb66e0cda8f05e476554e03272928b30687b330db9c0b95718e05`  
		Last Modified: Fri, 16 May 2025 19:09:40 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:bf122adb7f665faeabcaa74c5faa11d6b3858be55e644c790a846648ce95ff1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50ade38012f71c2132eb2363f019fd69211c4b0e9f4f862ba0f78d615b0097b`

```dockerfile
```

-	Layers:
	-	`sha256:75efb097e69e31f377df0f8ecfd45207e2aae47de9bc46fb465060a2c099729c`  
		Last Modified: Fri, 16 May 2025 19:09:40 GMT  
		Size: 2.2 MB (2204370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c3b555aecfe9bc0b48dde231eb7f206df331fe649a5179b17a3c63dd969899e`  
		Last Modified: Fri, 16 May 2025 19:09:39 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.0.3-core`

```console
$ docker pull influxdb@sha256:9aa9e65e851b7bf5f8573765c86dedcf106f6c1c4540e68526c9fc5908d58b64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.0.3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:0541f1915c0365e216e5c7c9ad359dfd431d659a48ea38fa1b7efe221f971b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97916361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56191da4e4fcb680e5fd37a29a1cc1fbad49e1cc4a48dfac85c1519027fd874`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45d233bca13463d087d78f8628ee0e48246bb2260ddc2e1753b8edf7a60465e`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 6.7 MB (6663446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2335e5ccc6e74199b81cac14d25ef86c600701f0cb179af4909be93c76c0b85`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2929d11995a5be55a68d56cea52f4a5524a83f19a5064bd79181045de67784`  
		Last Modified: Fri, 16 May 2025 19:09:44 GMT  
		Size: 61.5 MB (61531262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b996a11e64194691cec83263137edbf2d5ac286dd80cfba6e8ac9f61e23ccab`  
		Last Modified: Fri, 16 May 2025 19:09:43 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09920d7411dc2b83cd2ba0f66828d637a672c098969a3a96038f742659eb227b`  
		Last Modified: Fri, 16 May 2025 19:09:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.0.3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4366db6a68771db7c80db70c86d8d352d1700165eaf74db8151308928ef8d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70985cac70f460065e4f4404b8a8792f8871d12d05656a0cce1b4fe5785780f4`

```dockerfile
```

-	Layers:
	-	`sha256:3b47a22f93be6a7ff58cd3e2658f9e3e7024019f24a496b4b7aa3ff56b7799dc`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 2.2 MB (2203240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9822b6a3d8b69e8a72ef5bb1ed07e7e811727df146971621810ba146ae8919`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.0.3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:672c4a4221b3406da630526e426d4e4b172cb72179262e990e6a88f1d5099f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90509144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2005ef240f1a4c466d0784802963fa2b166ace199af5fc927753457eb3efaee0`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d3ffcca3dea02f4c8adcd31729621ed8d7e4b7531c23b8cac9775f570b5085`  
		Last Modified: Mon, 05 May 2025 21:30:45 GMT  
		Size: 6.7 MB (6674461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f74b4aeea550ca1632e75aa80f8fa8a2ccff90a4138e9f7d1c3d8333e53e3e`  
		Last Modified: Mon, 05 May 2025 21:30:44 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07863461f8e1c5ae19e31f7cd33f989a24208a6e83bbd372b715442c76c7b68d`  
		Last Modified: Fri, 16 May 2025 19:09:16 GMT  
		Size: 55.0 MB (54983680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e77c07210f0fc32bc01a1f689f570f68d1684537afb8272a0a54dbf781f4b8`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5425d10b3656e5aa3b699869d3b14e9890737e5953d97f93c95130ae739417`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.0.3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3fceef544916459184e06b503c25120d859ee98e6327290ee166e5af44b15f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d106116f0cda0f646738472152eb611a392c3f18d5c2694d15c0d276d62ff03d`

```dockerfile
```

-	Layers:
	-	`sha256:71235520c5b8db6cbc081b11126bd944131d82b49f898244ed2ecd97aadc285b`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 2.2 MB (2204322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3aef4f0be0364f461cbf8d084add55647775f705ca011344adcd716ba88893e`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.0.3-enterprise`

```console
$ docker pull influxdb@sha256:268a2553b83bc434f37017e1b8faf2084e8578ce0adaf7ff48f90c856361a640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.0.3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:0831d74c4536fcf32559efc45387d3c9e86b73298e03eca7365e511205594ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (100001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc6e48be2b2670b9aa821717cbc52bdf388a660d63e36b64e81844f3a811ef2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae520f817f8cab06dd90a7dd53cf0f5913b476bbf6ffb463664d14028482b4c`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 6.7 MB (6663469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f5f6b5a16642b2e7d600a78ccdb14667d4b733c7c67e70d0a34452a74c4b5b`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d09603a0a7affbe9365e383b9441ffe05ca55e340cded8251f267a5f909ced`  
		Last Modified: Fri, 16 May 2025 19:09:37 GMT  
		Size: 63.6 MB (63616620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddb6ae1b11404986ad7cab5ef50d3f063229042eb15b212c2e6df5a7f633995`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96604f7f2839a5948435ec73b7302b4ed49d6b55846cd167beabfe1c67f07189`  
		Last Modified: Fri, 16 May 2025 19:09:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.0.3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:5d2b290f04c945829b3e9bb07ef592aa47b41e0ee615ebd1e868c9f1765b0f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096fedc4b5d1bdc4329142f4db5c21abc14647db78b832289ce5f15457adf15c`

```dockerfile
```

-	Layers:
	-	`sha256:9a19028d33d179c531cdff08009d86f0f5345b13ab2665008b0c8d9a89339fd0`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 2.2 MB (2203288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f59d10de0920ee5c0b5c0354cc5381868cf5aae0c9c0884d39e6742e41165d3`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.0.3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:86c3040da8a31671b4a8723820f1fd058dd6daaf4e104ae676cdd35a6c1bfc1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92545538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d4c0472559b432bd42cf220d9af4838c7a6b9e1db0478075582fc04529da76`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d3ffcca3dea02f4c8adcd31729621ed8d7e4b7531c23b8cac9775f570b5085`  
		Last Modified: Mon, 05 May 2025 21:30:45 GMT  
		Size: 6.7 MB (6674461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f74b4aeea550ca1632e75aa80f8fa8a2ccff90a4138e9f7d1c3d8333e53e3e`  
		Last Modified: Mon, 05 May 2025 21:30:44 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8e9105883f39dc1d6116059355f136f26bf486bf75708411cba6b55f073c60`  
		Last Modified: Fri, 16 May 2025 19:09:41 GMT  
		Size: 57.0 MB (57020072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8104228122b89805d5c0dc89a695746c7aca0dd1ef6c3b9d43ca679aa0e66ada`  
		Last Modified: Fri, 16 May 2025 19:09:40 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1db856ab0eb66e0cda8f05e476554e03272928b30687b330db9c0b95718e05`  
		Last Modified: Fri, 16 May 2025 19:09:40 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.0.3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:bf122adb7f665faeabcaa74c5faa11d6b3858be55e644c790a846648ce95ff1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50ade38012f71c2132eb2363f019fd69211c4b0e9f4f862ba0f78d615b0097b`

```dockerfile
```

-	Layers:
	-	`sha256:75efb097e69e31f377df0f8ecfd45207e2aae47de9bc46fb465060a2c099729c`  
		Last Modified: Fri, 16 May 2025 19:09:40 GMT  
		Size: 2.2 MB (2204370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c3b555aecfe9bc0b48dde231eb7f206df331fe649a5179b17a3c63dd969899e`  
		Last Modified: Fri, 16 May 2025 19:09:39 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:a7a9e96c9bfc443a79d13e2b1989dc43608eb5b6c06fec6d30651ca5f8219330
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cbee5988f47dfa92bea7f72ff9e0fb07ba7956ead0141dc2ab27245b31f4f105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92785945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ade717ac7e624b9847ff64fa2b0f29775c53f8ea1418f8ec9c486ffc444719a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 21 May 2025 19:23:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b4da6257d4dab81f7ea9b217e8990fa02b532b487dc09f66cfe66b7a5ab1b7`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f227616a4b65630020272b1a4736c45d2072fea1f6ae56d8987f001bff1868e5`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 9.7 MB (9668254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28153e71486f54b7e2d6898878271446058952c9919aaad4310fd5662e14073`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 5.8 MB (5820951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17da966601b69ee27cf7e07f71e8d3a293465f510f662a95761c204c476039`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f351545292c8d4b32b561f37f2761b8143e35ea7b2aed6ada764d91675953e2`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 50.1 MB (50115457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec39c678e278ff055d4d22e8402129df928caa4a2647ff3024e97721f0f5943`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 23.5 MB (23546414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428d400809cb7ad31d35a7f2d948c8121b3f7499c617f94eb95080f6705d2c6`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195b609b670962adf4a4fd55112b8f3ee09ab9b864b63db78893c7e7b6de06aa`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213bcca749f51ef7f5ebe65ef3ee91941b8ead606c2179e2247bba98e5d1ba1`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:07a190e7a4e44a2d2349ddf22bcf6a411cb327788d87cbe24dfbfb319e2346ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.5 KB (949513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0face7c412448d24ef27a189fc81813532f5930f3f6a820e3311b431cb71a2`

```dockerfile
```

-	Layers:
	-	`sha256:dc8858c4baeaf5b780566e1f56dac4769e4c5fb4a00452d59c94970c80b6638d`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 918.5 KB (918468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15b588c6b6124a1aa918ae48f879aa8e721ecd2db834e3c78af76a20738c283`  
		Last Modified: Wed, 21 May 2025 21:01:33 GMT  
		Size: 31.0 KB (31045 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:acd117211c431790fc6d016c91eec85d13c132bf2179149dd9c1163fd5b36f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89567348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f25c6a394b54e0d7afd6e4960b11cc3c7389d6a99abd4edc658192b2ed4782b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 21 May 2025 19:23:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c8ed1b411bf87e31d51dcd5e11ad29b842c6ac23d29867f58c9b6657217f9`  
		Last Modified: Tue, 06 May 2025 02:07:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7581744a5f8b851a37b006b9f70c0dfc1aabfbbf6e54e0d468d11332b9a89155`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 9.8 MB (9790275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8e2420533fb94a98c3c0cea702d65af3aac200564d71bf02039933d45752c4`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d98ff612225a614c58f5f650b55a20d2a5f607933c56ec0b343dc54d39316`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9943be5d4ecac40794357058ec1ead2ffe57b93ad82f1c046f9490950fb8be`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 48.0 MB (48016208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592941019971dc33dba5c666bebc57139662a00acd86e6dc6e85310542b62a90`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 22.2 MB (22197933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a652dc6c421b2c1298eb71f3a1a77ad5317359d42f97d2ba7e0256166f7908`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c5c55779859032454928168c0eaf5620289e22d09443a4c303e920fbc0f25e`  
		Last Modified: Wed, 21 May 2025 21:02:37 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c5a87a5ee69568a4bb3e3c7fbcb83b0bd9250e68ef8618525ab0df87a7c0`  
		Last Modified: Wed, 21 May 2025 21:02:38 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:729a0121b69401596161e2c26bec6508731ab99a75514774f24c6af6bfc18323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.0 KB (948960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c122a9ee58ab54b906e11b0f4efc6fa24ec9862171d48194a1c13655341895`

```dockerfile
```

-	Layers:
	-	`sha256:5f2a9ab7569906dc8b16cb3c30fa1f29afe85dc187f764fa5f1821fc5d6848ec`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 917.7 KB (917719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f4f5e2584d7feb4ec7fc289bad890abb4f9f813f7c20ca231fb580b0db01d6d`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 31.2 KB (31241 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:core`

```console
$ docker pull influxdb@sha256:9aa9e65e851b7bf5f8573765c86dedcf106f6c1c4540e68526c9fc5908d58b64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:0541f1915c0365e216e5c7c9ad359dfd431d659a48ea38fa1b7efe221f971b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97916361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56191da4e4fcb680e5fd37a29a1cc1fbad49e1cc4a48dfac85c1519027fd874`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45d233bca13463d087d78f8628ee0e48246bb2260ddc2e1753b8edf7a60465e`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 6.7 MB (6663446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2335e5ccc6e74199b81cac14d25ef86c600701f0cb179af4909be93c76c0b85`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2929d11995a5be55a68d56cea52f4a5524a83f19a5064bd79181045de67784`  
		Last Modified: Fri, 16 May 2025 19:09:44 GMT  
		Size: 61.5 MB (61531262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b996a11e64194691cec83263137edbf2d5ac286dd80cfba6e8ac9f61e23ccab`  
		Last Modified: Fri, 16 May 2025 19:09:43 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09920d7411dc2b83cd2ba0f66828d637a672c098969a3a96038f742659eb227b`  
		Last Modified: Fri, 16 May 2025 19:09:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4366db6a68771db7c80db70c86d8d352d1700165eaf74db8151308928ef8d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70985cac70f460065e4f4404b8a8792f8871d12d05656a0cce1b4fe5785780f4`

```dockerfile
```

-	Layers:
	-	`sha256:3b47a22f93be6a7ff58cd3e2658f9e3e7024019f24a496b4b7aa3ff56b7799dc`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 2.2 MB (2203240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9822b6a3d8b69e8a72ef5bb1ed07e7e811727df146971621810ba146ae8919`  
		Last Modified: Fri, 16 May 2025 19:09:42 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:672c4a4221b3406da630526e426d4e4b172cb72179262e990e6a88f1d5099f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90509144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2005ef240f1a4c466d0784802963fa2b166ace199af5fc927753457eb3efaee0`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d3ffcca3dea02f4c8adcd31729621ed8d7e4b7531c23b8cac9775f570b5085`  
		Last Modified: Mon, 05 May 2025 21:30:45 GMT  
		Size: 6.7 MB (6674461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f74b4aeea550ca1632e75aa80f8fa8a2ccff90a4138e9f7d1c3d8333e53e3e`  
		Last Modified: Mon, 05 May 2025 21:30:44 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07863461f8e1c5ae19e31f7cd33f989a24208a6e83bbd372b715442c76c7b68d`  
		Last Modified: Fri, 16 May 2025 19:09:16 GMT  
		Size: 55.0 MB (54983680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e77c07210f0fc32bc01a1f689f570f68d1684537afb8272a0a54dbf781f4b8`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5425d10b3656e5aa3b699869d3b14e9890737e5953d97f93c95130ae739417`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3fceef544916459184e06b503c25120d859ee98e6327290ee166e5af44b15f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d106116f0cda0f646738472152eb611a392c3f18d5c2694d15c0d276d62ff03d`

```dockerfile
```

-	Layers:
	-	`sha256:71235520c5b8db6cbc081b11126bd944131d82b49f898244ed2ecd97aadc285b`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 2.2 MB (2204322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3aef4f0be0364f461cbf8d084add55647775f705ca011344adcd716ba88893e`  
		Last Modified: Fri, 16 May 2025 19:09:15 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:268a2553b83bc434f37017e1b8faf2084e8578ce0adaf7ff48f90c856361a640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:0831d74c4536fcf32559efc45387d3c9e86b73298e03eca7365e511205594ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (100001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc6e48be2b2670b9aa821717cbc52bdf388a660d63e36b64e81844f3a811ef2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae520f817f8cab06dd90a7dd53cf0f5913b476bbf6ffb463664d14028482b4c`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 6.7 MB (6663469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f5f6b5a16642b2e7d600a78ccdb14667d4b733c7c67e70d0a34452a74c4b5b`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d09603a0a7affbe9365e383b9441ffe05ca55e340cded8251f267a5f909ced`  
		Last Modified: Fri, 16 May 2025 19:09:37 GMT  
		Size: 63.6 MB (63616620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddb6ae1b11404986ad7cab5ef50d3f063229042eb15b212c2e6df5a7f633995`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96604f7f2839a5948435ec73b7302b4ed49d6b55846cd167beabfe1c67f07189`  
		Last Modified: Fri, 16 May 2025 19:09:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:5d2b290f04c945829b3e9bb07ef592aa47b41e0ee615ebd1e868c9f1765b0f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096fedc4b5d1bdc4329142f4db5c21abc14647db78b832289ce5f15457adf15c`

```dockerfile
```

-	Layers:
	-	`sha256:9a19028d33d179c531cdff08009d86f0f5345b13ab2665008b0c8d9a89339fd0`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 2.2 MB (2203288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f59d10de0920ee5c0b5c0354cc5381868cf5aae0c9c0884d39e6742e41165d3`  
		Last Modified: Fri, 16 May 2025 19:09:36 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:86c3040da8a31671b4a8723820f1fd058dd6daaf4e104ae676cdd35a6c1bfc1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92545538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d4c0472559b432bd42cf220d9af4838c7a6b9e1db0478075582fc04529da76`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d3ffcca3dea02f4c8adcd31729621ed8d7e4b7531c23b8cac9775f570b5085`  
		Last Modified: Mon, 05 May 2025 21:30:45 GMT  
		Size: 6.7 MB (6674461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f74b4aeea550ca1632e75aa80f8fa8a2ccff90a4138e9f7d1c3d8333e53e3e`  
		Last Modified: Mon, 05 May 2025 21:30:44 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8e9105883f39dc1d6116059355f136f26bf486bf75708411cba6b55f073c60`  
		Last Modified: Fri, 16 May 2025 19:09:41 GMT  
		Size: 57.0 MB (57020072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8104228122b89805d5c0dc89a695746c7aca0dd1ef6c3b9d43ca679aa0e66ada`  
		Last Modified: Fri, 16 May 2025 19:09:40 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1db856ab0eb66e0cda8f05e476554e03272928b30687b330db9c0b95718e05`  
		Last Modified: Fri, 16 May 2025 19:09:40 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:bf122adb7f665faeabcaa74c5faa11d6b3858be55e644c790a846648ce95ff1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50ade38012f71c2132eb2363f019fd69211c4b0e9f4f862ba0f78d615b0097b`

```dockerfile
```

-	Layers:
	-	`sha256:75efb097e69e31f377df0f8ecfd45207e2aae47de9bc46fb465060a2c099729c`  
		Last Modified: Fri, 16 May 2025 19:09:40 GMT  
		Size: 2.2 MB (2204370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c3b555aecfe9bc0b48dde231eb7f206df331fe649a5179b17a3c63dd969899e`  
		Last Modified: Fri, 16 May 2025 19:09:39 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:c33ac14af66fee77fe5ba14d7ae3b7d7bdc53186cc589eceb413af9f02ca01a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:7be7e75f358cc9a41498b774a217457862e26b9fb0add2fb807cc8eeff8b09b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168645172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2def43b479b5213296cf94cc546f6d13f0b60f6891d9ba5034f5fb93f82c87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 21 May 2025 19:23:38 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV GOSU_VER=1.16
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e42863fbf917dba1d766836b81770e15967448a3c6410d92e950ddecac6c55`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 9.8 MB (9790933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfbdcc44decf955f1d649b2ee7fb1dbfa1c71998d36496387259861082068cf`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dbeb28e9b9a5ac6bd7dc5f4e1a0492b48dee1b297b7960b9dbb5e70cfd316f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619522457ecb94cbc0e36611bbb2312d35b8ca38bac40596c4e5965a64ff6e6f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 1.0 MB (1006372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d3e2d4d64dbe43902a5d0f793e7bef3eea64d5a22f519ea3c4f36b8a78144b`  
		Last Modified: Wed, 21 May 2025 21:01:37 GMT  
		Size: 100.2 MB (100242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701cad0e28464a9b1c3f5196d8bfcdc50fd2bec501bb8fe30f5b0c3f1bb7fcb7`  
		Last Modified: Wed, 21 May 2025 21:01:37 GMT  
		Size: 23.5 MB (23546398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c58b87f333a4d73eea79083aa2294f7753b04c402a321e6098ef7a67dab54`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6393554df92840606b3ffe8e897b394b7ce2b681cffd41f3e170a9446dc089`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc25c80f073d68bad44122268fd1a57631febec15ee6b544d34975ce4773ec4`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:31ffdab1dcfa7b7027482c046340e0e4e3d3d5f746b81f0e5e25c81d8fe2bef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2902904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47429ba26e292482bceec4cdf8dbb0dca3795338f22c3030a890ac85d4ee8df`

```dockerfile
```

-	Layers:
	-	`sha256:b80c4678d52151bdba2ddadbec502eaf3df048dad8cdd7e73316f85c619a910c`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 2.9 MB (2869086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef63408be21053676231c89cbda0f54072a30c09521bb38c546f3823423a68f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 33.8 KB (33818 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0839cb088f4a243f06560a4851d14ee7522263cce0b700cf84b53dd97ca900ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162301307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4045d580c6b33dc7f3056070fb3056024446dedf2f454fb9ac18669087e55c06`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 21 May 2025 19:23:38 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV GOSU_VER=1.16
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b410a06ce4fcda8c631e50621e6543d50ed900c819663b8e8c41c7f7ac89053`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 9.6 MB (9588509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de0fff97c4cf200ca210ae20785978cda6a042a650e28db59b324b44f41f905`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806918d354e310d08b135e40f2e2d26fcd65062af8700b837f4aa84de0482de6`  
		Last Modified: Wed, 21 May 2025 21:02:06 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dd02a48352d53c118b216ffe4dbce8cea9676dd3da4bebf4dcefc7d299a03c`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 936.1 KB (936100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc6e61093af6624558cddc2362654c606748ecb54cee1a3486c6098cdbfed22`  
		Last Modified: Wed, 21 May 2025 21:02:11 GMT  
		Size: 96.0 MB (96038376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae02942e730c824aa6fbe30374d5af1dd7d72e7c8c4c9a0298374f5c6962c87c`  
		Last Modified: Wed, 21 May 2025 21:02:09 GMT  
		Size: 22.2 MB (22197938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b32a406b9d356f60656a71f8e36b9f9bcf243eaf723901c78828482765101a`  
		Last Modified: Wed, 21 May 2025 21:02:08 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9872dc5e700b80dd89f142c8e61e7c3f60a789e35de74d0c0f4321b48245b58`  
		Last Modified: Wed, 21 May 2025 21:02:08 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f917e572fef7a9039d0ba795a86b841215a450065b9e2e783189157ef6e19122`  
		Last Modified: Wed, 21 May 2025 21:02:09 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:f0906a5dd25bedffed8866016cdbe9b64eeb5e6c3d11c522f74a73e616785680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2902315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ceac7e7fd2dc69af9be74f65c2a4737611300d774979a37d6dc13f6695244d`

```dockerfile
```

-	Layers:
	-	`sha256:1e76d058079ee2ce737fe5009b78a9362df4797f206fcf557ce706df337fde24`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 2.9 MB (2868314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f554075615356b4d24f3930e6ac1ae2742ffae4bbd677ce1846d300062b29382`  
		Last Modified: Wed, 21 May 2025 21:02:06 GMT  
		Size: 34.0 KB (34001 bytes)  
		MIME: application/vnd.in-toto+json
