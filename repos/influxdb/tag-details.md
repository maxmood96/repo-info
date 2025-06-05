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
-	[`influxdb:3.1-core`](#influxdb31-core)
-	[`influxdb:3.1-enterprise`](#influxdb31-enterprise)
-	[`influxdb:3.1.0-core`](#influxdb310-core)
-	[`influxdb:3.1.0-enterprise`](#influxdb310-enterprise)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:core`](#influxdbcore)
-	[`influxdb:enterprise`](#influxdbenterprise)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:8270c03d379b092877bd5fc98e7c8eeb4753f091c8d11b977ae4d1b6aae384d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f44d3f5d2874c99b0af28100ac068b5162a9d367bd877fdfca6a64bd75381f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108958214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b9e120b6cfb217062c6406a6d7e6ab17d4f3f161d082b2f0ae7642e44f081c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 21 May 2025 19:23:38 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbf6a2d5ea8ac2cf1562a78ecd022f3299e4dafc0947d9f9697f59177b89052`  
		Last Modified: Tue, 03 Jun 2025 21:32:00 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc79c131d6532ee7edc725b72e6ed13e94033d253f179eebb82d5d1b8186b7`  
		Last Modified: Tue, 03 Jun 2025 21:32:03 GMT  
		Size: 39.4 MB (39439600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0463b422f1cf5b640540ea0689b3990ac7fd800854a8a1f61d0ae8cd8d759349`  
		Last Modified: Tue, 03 Jun 2025 21:32:00 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e436d2e804a7dee2d12e6a59d21416d11ca3e2fdac1dc3957dfbc39da2a95e`  
		Last Modified: Tue, 03 Jun 2025 21:32:02 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc47f33351374435a50aed83d9ba8577a13e5546cde3a381be3d1504cf92c96`  
		Last Modified: Tue, 03 Jun 2025 13:42:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:2a8c91326118d5dad761a8a8cbba3fbde3cd6c859bad407d9a7896d3cd8e2f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4680418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7583a958ea58da2a8712991651fb8c3814da9c4e338fca56ce3eb43899ce2e9`

```dockerfile
```

-	Layers:
	-	`sha256:488b8173cbfd68dba36a35c88025e62c9fd275d7bb29e61783db4f4a1d16aa4c`  
		Last Modified: Thu, 05 Jun 2025 01:08:11 GMT  
		Size: 4.7 MB (4665710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67b4ec4635b3fe6552ee57ee6ded63f0a3c062bdec09cb80afb84f8027affbf1`  
		Last Modified: Thu, 05 Jun 2025 01:08:10 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c981537527a695b8c20b6027e59d150b12110fc841db76dca1309d531060204c`  
		Last Modified: Fri, 14 Feb 2025 22:33:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe95b0d50fd108a7bab7229bf48c4d6f15d501d181e060aa9d75c5733498b45a`  
		Last Modified: Fri, 14 Feb 2025 22:33:58 GMT  
		Size: 1.2 MB (1226185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44173060551cc5ccb97812e53b623aa03ebd2405605f40c08c828ec1348fbce4`  
		Last Modified: Fri, 14 Feb 2025 22:34:00 GMT  
		Size: 39.4 MB (39379880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd95c0fb0fc1a1fe7c4dc1bac921311d6b89557c3b1a21520add3766f2d79b1d`  
		Last Modified: Fri, 14 Feb 2025 22:33:58 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2c3ee9de55100bff4c1fc71b7158bd83eb790d8173d9e4eabcc4d912accb3d`  
		Last Modified: Fri, 14 Feb 2025 22:33:58 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d857fb73ed049778a398a1c483940b544aa66d0b1548085c55a0f6e4c983671f`  
		Last Modified: Fri, 14 Feb 2025 22:33:59 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:20:17 GMT  
		Size: 755.6 KB (755627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9539fc66665e5ef5dbcf98abd6782b4bb32862e6c51158c4d525f8a3acd705da`  
		Last Modified: Fri, 14 Feb 2025 21:20:17 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:a85bd6251aa8a729043f00007d944100bf034adb28e575b3a9695c2a8f236c52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:f1bed52c481e64fcd3ce151e259328b633e51efe9b4ed6eb98e230a01a667349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88157420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d198d7d7ec8e7eb06f60bc918f3b0daab89f20df4a4dd44bd67837759075ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 21 May 2025 19:23:38 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e641ae5b5f6d4ba29572b4cf70d958dcff0be4735002ebd0f435852441a9e7b`  
		Last Modified: Tue, 03 Jun 2025 21:33:52 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b47ef2742bde9781b189b0060aa749aee40565a4ca82c3df9d3bca2ab70a8a`  
		Last Modified: Tue, 03 Jun 2025 21:33:53 GMT  
		Size: 18.6 MB (18640014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f7e3f0279c90f16dad987fb2e1ee7dcc81f6d7d059a07d2a64a44952110bcc`  
		Last Modified: Tue, 03 Jun 2025 21:33:52 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564933e4f4c39b42dd7cd50aebc5b2116d8f69d9157d6a4dbd7fc876ec86fc9b`  
		Last Modified: Tue, 03 Jun 2025 21:33:53 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:a09b826cba5f0dd731648b45939122fa027c8fa1a5c17c21e41ad9ec691bc165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4602757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4632e4274c6454019bb475b1365c929079edbbf2a2512726079109c3eb8435d8`

```dockerfile
```

-	Layers:
	-	`sha256:d8f0728a4d8a2c7651a9d003b10167e01aaa9faad63366157935bbdea1f360e0`  
		Last Modified: Wed, 21 May 2025 23:40:23 GMT  
		Size: 4.6 MB (4589690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01d9bcc84f96164dd80c88310fc7fbe3e7d0b13ce9838cb4185b6b8cf28717f`  
		Last Modified: Wed, 21 May 2025 23:40:23 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb5c8cdbec35edc43e48ac5677234575ad99cf8e483ecb8687d5419d5b425d`  
		Last Modified: Fri, 14 Feb 2025 22:35:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8e09bdbba52f1107efa5e5ba96ff16880584254227de593d5e9327a809f95`  
		Last Modified: Fri, 14 Feb 2025 22:35:54 GMT  
		Size: 1.2 MB (1226193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d9a6ef6450631c9e70c6a4ac06fd7f6a159ce59e4615829510b0c3cc0bb69b`  
		Last Modified: Fri, 14 Feb 2025 22:35:57 GMT  
		Size: 18.6 MB (18596363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c171bf24072ac133ca0666ed07f4bab8ca9f5e785f8726e5b6b22a6bcdafb7`  
		Last Modified: Fri, 14 Feb 2025 22:35:55 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb43bdb4aca4dfbb93ec902aaf20f61ea9ce655828dae6308ce794bb52b39c4`  
		Last Modified: Fri, 14 Feb 2025 22:35:55 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:20:21 GMT  
		Size: 679.5 KB (679511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f792b8250d838c0cf30993d65d8457974cc3309d67893a5bd86b44cb832c6098`  
		Last Modified: Fri, 14 Feb 2025 21:20:22 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.8-data`

```console
$ docker pull influxdb@sha256:8270c03d379b092877bd5fc98e7c8eeb4753f091c8d11b977ae4d1b6aae384d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f44d3f5d2874c99b0af28100ac068b5162a9d367bd877fdfca6a64bd75381f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108958214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b9e120b6cfb217062c6406a6d7e6ab17d4f3f161d082b2f0ae7642e44f081c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 21 May 2025 19:23:38 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbf6a2d5ea8ac2cf1562a78ecd022f3299e4dafc0947d9f9697f59177b89052`  
		Last Modified: Tue, 03 Jun 2025 21:32:00 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc79c131d6532ee7edc725b72e6ed13e94033d253f179eebb82d5d1b8186b7`  
		Last Modified: Tue, 03 Jun 2025 21:32:03 GMT  
		Size: 39.4 MB (39439600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0463b422f1cf5b640540ea0689b3990ac7fd800854a8a1f61d0ae8cd8d759349`  
		Last Modified: Tue, 03 Jun 2025 21:32:00 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e436d2e804a7dee2d12e6a59d21416d11ca3e2fdac1dc3957dfbc39da2a95e`  
		Last Modified: Tue, 03 Jun 2025 21:32:02 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc47f33351374435a50aed83d9ba8577a13e5546cde3a381be3d1504cf92c96`  
		Last Modified: Tue, 03 Jun 2025 13:42:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:2a8c91326118d5dad761a8a8cbba3fbde3cd6c859bad407d9a7896d3cd8e2f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4680418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7583a958ea58da2a8712991651fb8c3814da9c4e338fca56ce3eb43899ce2e9`

```dockerfile
```

-	Layers:
	-	`sha256:488b8173cbfd68dba36a35c88025e62c9fd275d7bb29e61783db4f4a1d16aa4c`  
		Last Modified: Thu, 05 Jun 2025 01:08:11 GMT  
		Size: 4.7 MB (4665710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67b4ec4635b3fe6552ee57ee6ded63f0a3c062bdec09cb80afb84f8027affbf1`  
		Last Modified: Thu, 05 Jun 2025 01:08:10 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c981537527a695b8c20b6027e59d150b12110fc841db76dca1309d531060204c`  
		Last Modified: Fri, 14 Feb 2025 22:33:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe95b0d50fd108a7bab7229bf48c4d6f15d501d181e060aa9d75c5733498b45a`  
		Last Modified: Fri, 14 Feb 2025 22:33:58 GMT  
		Size: 1.2 MB (1226185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44173060551cc5ccb97812e53b623aa03ebd2405605f40c08c828ec1348fbce4`  
		Last Modified: Fri, 14 Feb 2025 22:34:00 GMT  
		Size: 39.4 MB (39379880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd95c0fb0fc1a1fe7c4dc1bac921311d6b89557c3b1a21520add3766f2d79b1d`  
		Last Modified: Fri, 14 Feb 2025 22:33:58 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2c3ee9de55100bff4c1fc71b7158bd83eb790d8173d9e4eabcc4d912accb3d`  
		Last Modified: Fri, 14 Feb 2025 22:33:58 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d857fb73ed049778a398a1c483940b544aa66d0b1548085c55a0f6e4c983671f`  
		Last Modified: Fri, 14 Feb 2025 22:33:59 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:20:17 GMT  
		Size: 755.6 KB (755627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9539fc66665e5ef5dbcf98abd6782b4bb32862e6c51158c4d525f8a3acd705da`  
		Last Modified: Fri, 14 Feb 2025 21:20:17 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.10.8-meta`

```console
$ docker pull influxdb@sha256:a85bd6251aa8a729043f00007d944100bf034adb28e575b3a9695c2a8f236c52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:f1bed52c481e64fcd3ce151e259328b633e51efe9b4ed6eb98e230a01a667349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88157420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d198d7d7ec8e7eb06f60bc918f3b0daab89f20df4a4dd44bd67837759075ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 21 May 2025 19:23:38 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e641ae5b5f6d4ba29572b4cf70d958dcff0be4735002ebd0f435852441a9e7b`  
		Last Modified: Tue, 03 Jun 2025 21:33:52 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b47ef2742bde9781b189b0060aa749aee40565a4ca82c3df9d3bca2ab70a8a`  
		Last Modified: Tue, 03 Jun 2025 21:33:53 GMT  
		Size: 18.6 MB (18640014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f7e3f0279c90f16dad987fb2e1ee7dcc81f6d7d059a07d2a64a44952110bcc`  
		Last Modified: Tue, 03 Jun 2025 21:33:52 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564933e4f4c39b42dd7cd50aebc5b2116d8f69d9157d6a4dbd7fc876ec86fc9b`  
		Last Modified: Tue, 03 Jun 2025 21:33:53 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:a09b826cba5f0dd731648b45939122fa027c8fa1a5c17c21e41ad9ec691bc165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4602757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4632e4274c6454019bb475b1365c929079edbbf2a2512726079109c3eb8435d8`

```dockerfile
```

-	Layers:
	-	`sha256:d8f0728a4d8a2c7651a9d003b10167e01aaa9faad63366157935bbdea1f360e0`  
		Last Modified: Wed, 21 May 2025 23:40:23 GMT  
		Size: 4.6 MB (4589690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01d9bcc84f96164dd80c88310fc7fbe3e7d0b13ce9838cb4185b6b8cf28717f`  
		Last Modified: Wed, 21 May 2025 23:40:23 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb5c8cdbec35edc43e48ac5677234575ad99cf8e483ecb8687d5419d5b425d`  
		Last Modified: Fri, 14 Feb 2025 22:35:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8e09bdbba52f1107efa5e5ba96ff16880584254227de593d5e9327a809f95`  
		Last Modified: Fri, 14 Feb 2025 22:35:54 GMT  
		Size: 1.2 MB (1226193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d9a6ef6450631c9e70c6a4ac06fd7f6a159ce59e4615829510b0c3cc0bb69b`  
		Last Modified: Fri, 14 Feb 2025 22:35:57 GMT  
		Size: 18.6 MB (18596363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c171bf24072ac133ca0666ed07f4bab8ca9f5e785f8726e5b6b22a6bcdafb7`  
		Last Modified: Fri, 14 Feb 2025 22:35:55 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb43bdb4aca4dfbb93ec902aaf20f61ea9ce655828dae6308ce794bb52b39c4`  
		Last Modified: Fri, 14 Feb 2025 22:35:55 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:20:21 GMT  
		Size: 679.5 KB (679511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f792b8250d838c0cf30993d65d8457974cc3309d67893a5bd86b44cb832c6098`  
		Last Modified: Fri, 14 Feb 2025 21:20:22 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11`

```console
$ docker pull influxdb@sha256:f8be1f772fe0ee6f39456280c1df149274bb6808d1be5a54d394ee54cde2b13e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:9c35b76a52ac003bb1e885a870355e298e3a8f63a6b9edcf4f43af256785d69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116158328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18e92d7be70e67baa547ed3d7b40ab1503a696113f2dfcea3f2d7db9edc7026`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 21 May 2025 19:23:38 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
USER influxdb
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f6081745c045ec77e9e1fa3fc18646ff59c3f7299a3521a9f4e37496d81885`  
		Last Modified: Tue, 03 Jun 2025 13:39:46 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a139339f6ab016e27e13df6d898fe6c232867514003b409e728ea350cc0729`  
		Last Modified: Tue, 03 Jun 2025 13:49:48 GMT  
		Size: 43.7 MB (43651541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304aac6ae51f8a23ddc3d8f2f51a57ce2cde18650f6555ecdeedfbd261fa096a`  
		Last Modified: Tue, 03 Jun 2025 13:42:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c199006e6947fe8376e7fcf89daeb1d0e00a226f968d81681bb25cb2338fc8`  
		Last Modified: Tue, 03 Jun 2025 13:42:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc47f33351374435a50aed83d9ba8577a13e5546cde3a381be3d1504cf92c96`  
		Last Modified: Tue, 03 Jun 2025 13:42:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:7ec73ce3f86b85048b529930148793b87986c711d145d47783688dac546eb4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec3a93d03f1326df6e1d14f377bdb86429861d4e016416f30fc58cbb559f3df`

```dockerfile
```

-	Layers:
	-	`sha256:663016539b58dc2762de84707c9f0a7c38705f53c7d54b6aba8763cdd9aa799e`  
		Last Modified: Thu, 05 Jun 2025 11:28:43 GMT  
		Size: 4.9 MB (4912448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62fb8c4d4e497c944b88567a6eace3bc23bdfda0f73f251068a6b9975e121172`  
		Last Modified: Thu, 05 Jun 2025 11:28:45 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:08d55a308d1d5ae149ef852ceac8b69da5c0b78f60862bea24b68de8528b0144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113000809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954bf2d07ad5caba738166648910024295abb1c8df49d26c935f1ba600bfa6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 21 May 2025 19:23:38 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
USER influxdb
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a8315385242d1d7ed00b9b26d3aee7f7327b635c12c8b4e2718171d6f32904`  
		Last Modified: Tue, 03 Jun 2025 13:56:22 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf27056cc96ff1052003b8778535377c992872e9536399c4942924191c1abd1`  
		Last Modified: Tue, 03 Jun 2025 13:56:39 GMT  
		Size: 41.1 MB (41119323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df259a20a4c9fd043b3c5ed299de62e5690119f11d6df9b424d632ce4dca31f7`  
		Last Modified: Tue, 03 Jun 2025 13:56:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35d41c533cf81a905f528f68fc355c19c014d83372ff338c56186e4f017ad1`  
		Last Modified: Tue, 03 Jun 2025 13:56:37 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa86bf8b96df0167c9ab6c0cd2cf6424f304abf209fb01bbd8ec1c11b6a29a`  
		Last Modified: Tue, 03 Jun 2025 13:56:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:d59742de0bd72db34df9b853b6608e79554e793c4ac091780c72f2094a975a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c168035e73b4dba24c52914eb6c73d522f283fcbb9285a0cd0b4266c0a13978`

```dockerfile
```

-	Layers:
	-	`sha256:95edccfa6877f089e828d365ddc0d7a270985a1be27c6ec4ce7cd9409cb0e44d`  
		Last Modified: Thu, 05 Jun 2025 11:28:45 GMT  
		Size: 4.9 MB (4911913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfcf57260da9d60377d2e04e409c81977dea23dd8f93217a24b408336f8e49ca`  
		Last Modified: Thu, 05 Jun 2025 11:28:47 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2430b91d27c94577a29aa4a63bc67b9a6bdb38f557ff03f2f47fe9fc4912a6e6`  
		Last Modified: Fri, 14 Feb 2025 21:20:46 GMT  
		Size: 1.2 MB (1226180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccd48b38856008daab1f21e8835b3d7b372598317d42820fc3f047db607ccec`  
		Last Modified: Fri, 14 Feb 2025 21:20:48 GMT  
		Size: 38.1 MB (38068218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94026e2b0d6f99fed3dedfb812a03fd046e8373145be2b2e4aee6b44295f325`  
		Last Modified: Fri, 14 Feb 2025 21:20:47 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfc22a651b18903f12176ed3447abf101612d8f6c009dde4beb5d65b864ff40`  
		Last Modified: Fri, 14 Feb 2025 21:20:47 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff30a98894f91ab375651dec55dbdaa6676482eba3ae74a247a1227bf992e1e`  
		Last Modified: Fri, 14 Feb 2025 21:20:48 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02c49477a92d638620b098485571f719849cc4a14d1a0bbbf9475ac5036c368`  
		Last Modified: Fri, 14 Feb 2025 21:20:49 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:20:28 GMT  
		Size: 743.3 KB (743321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f642c9f83ff2a959cec65a14ea556a5c772b8a03eecfc06b77b2212dd3f8fc78`  
		Last Modified: Fri, 14 Feb 2025 21:20:29 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e30a0c587fbc2e84c1b8c55a170ea149c6f6fb91469699f82a5d44e4dad9fdf`  
		Last Modified: Sat, 15 Feb 2025 09:18:20 GMT  
		Size: 1.3 MB (1307075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aedc2e6ed32b6b172146ed1536e1bc4675e2368a442a55fcbc77d582da9ded`  
		Last Modified: Sat, 15 Feb 2025 09:18:22 GMT  
		Size: 35.5 MB (35545506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f6a37ff4f04b2e3f6d6663dc1ad32dca8556db22f6aba5fa140293e06b8be6`  
		Last Modified: Sat, 15 Feb 2025 09:18:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e42b050238199a9cf809362968a20163c7d745329b332b4c122d9810b828e2`  
		Last Modified: Sat, 15 Feb 2025 09:18:23 GMT  
		Size: 995.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afc13286215e26f9388e94e989e8e7f25e3ba851d010c09add249a03c7801ee`  
		Last Modified: Sat, 15 Feb 2025 09:18:23 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644f23186760a8bda37888b6b2a4baf18413763b0df806f478204d981fb50ef4`  
		Last Modified: Sat, 15 Feb 2025 09:18:24 GMT  
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
		Last Modified: Sat, 15 Feb 2025 03:20:23 GMT  
		Size: 742.5 KB (742548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b1bc5d6ee15c6f1c9cb67454a907a5fafdc070f8a6cfd9143ff759f6ff93bd`  
		Last Modified: Sat, 15 Feb 2025 03:20:23 GMT  
		Size: 18.0 KB (17984 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:191a6a43ab3f0df53d9114370c8a6255ccd2efefe15871789c68f48adac0982f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:88565463c063725a0767b346a0d1c397b9f4a27bb824e15c713e74e816facbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111686726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6a1c5aa907fcb609aeea67536614e3e1ff76d1444524a8cac79edfc9cee74a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Wed, 21 May 2025 19:23:38 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea0d0d8518a8abb507c1c1f8848acf6bda32f7e3a92bd89de26ddd51d4a18cc`  
		Last Modified: Tue, 03 Jun 2025 21:35:41 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62590ca4a361feedc7ca878d537fd9b2d955c265a7e3cf70f5a45705b6f3012d`  
		Last Modified: Tue, 03 Jun 2025 21:35:43 GMT  
		Size: 39.2 MB (39179288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a3720d1c7e49bb139b98e68b023b0806fec0e1f9675980b9df459f9fe765bf`  
		Last Modified: Tue, 03 Jun 2025 21:35:41 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2352797ca35b81f033e84c396fde8c7d43075cef9ba47766f64d5a4952dff058`  
		Last Modified: Tue, 03 Jun 2025 21:35:43 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d8cef0ec440de11cc6d12eca5c6f3c55b854d4dec675973ab666b9b7f566a0`  
		Last Modified: Tue, 03 Jun 2025 21:35:43 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:5b35e79b7bb00e5004b80bf30f85eaff73b9adffb540491433b70fe8e599e720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4549395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53fd67e793c2c63b87d9169059f6ee90f1cb3635c6010a387266a9ec773673c`

```dockerfile
```

-	Layers:
	-	`sha256:e7ccc061dc847b3b66176b83e8f67949be6cf4a05f56d728fe96711e0765666a`  
		Last Modified: Wed, 21 May 2025 23:40:33 GMT  
		Size: 4.5 MB (4534688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bde0f7169d31d9fc1d821007f59d77dc3bcd3355df151bb04a75f8e6857b366`  
		Last Modified: Wed, 21 May 2025 23:40:33 GMT  
		Size: 14.7 KB (14707 bytes)  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d5b5d68d9f3f80ff363fb8fe3e7a2685990aa9ec18892b275d90a98637fd17`  
		Last Modified: Fri, 14 Feb 2025 21:20:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41957e5bb968a4cefc35246db18ec3931c853e733e93c5deb740f35f7e84c2e`  
		Last Modified: Fri, 14 Feb 2025 22:38:01 GMT  
		Size: 1.2 MB (1226185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468f4a21923f4bd549c35732446830e62e956dc03cdfd2c2d232f42d0e5009eb`  
		Last Modified: Fri, 14 Feb 2025 22:38:04 GMT  
		Size: 39.1 MB (39123831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb276187bda5db3e631d8724e8f410f96a6fec1390f6e75843194034f808c84`  
		Last Modified: Fri, 14 Feb 2025 22:38:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850540575a0c377c0f3b7ae91868304b5c287a5cb70ace26bbe032383b2c56ea`  
		Last Modified: Fri, 14 Feb 2025 22:38:02 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfd23d02f8457ddfcf7d4ccf1c6bb08ad6f3a8477e528e6a15a319acf3a2815`  
		Last Modified: Fri, 14 Feb 2025 22:38:02 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:20:32 GMT  
		Size: 753.9 KB (753866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9454c17edf183df5c9482191597585786c035bd37719a2898cd15830eb5307de`  
		Last Modified: Fri, 14 Feb 2025 21:20:32 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:ec7aabe307c301c30b5c84a3183f8bf7d9692b2c664ac991495677e9ed3c58d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:78a646c72a24c064c4fc629df9fdd01d2a030b38a8b8a75bfcf6d8e0aa922b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90842809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dd649ee56f245ae5ba45c0245549c58b7feff0387edda68e616f327952010b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Wed, 21 May 2025 19:23:38 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ff50dac0b60c61e3f208089d0bdb169219a52c9f966a8a9c726b08d65a7131`  
		Last Modified: Tue, 03 Jun 2025 21:37:39 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d1075191495374d278cccce1a169df1216308a6501cb4e894404e424f09a8e`  
		Last Modified: Tue, 03 Jun 2025 21:37:41 GMT  
		Size: 18.3 MB (18336578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341d9611206bcf2b17e222fe111c20a4f43d91e736e1c44417feba67b308e529`  
		Last Modified: Tue, 03 Jun 2025 21:37:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe66ddd7b7ccfcfb8661e5ad4ac0ea03b7aaaf60fddf203ba9065f71067005c9`  
		Last Modified: Tue, 03 Jun 2025 21:37:41 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:0d1ddbf322c8975edec4b256a4ff106cc9ba35cdad1c6b6b51682c3cecb69204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d77c0cbf7e37e0450255f2f03166ebaed2af5fc42bbbae1b5d228419dedac2`

```dockerfile
```

-	Layers:
	-	`sha256:162e00800135c98d09eb438e234dbeafc196ede45c5981b54e2da959c2ac7c07`  
		Last Modified: Wed, 21 May 2025 23:40:26 GMT  
		Size: 4.5 MB (4459659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77a57150a0f00a1a7182cb36b1bcd65deb64c9709afec8f68a1ec8f0fdcbe84a`  
		Last Modified: Wed, 21 May 2025 23:40:26 GMT  
		Size: 13.1 KB (13067 bytes)  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4179006b77d77220705fbc7483a58da67581ebd4d5bf829d0980b8db79003f1e`  
		Last Modified: Fri, 14 Feb 2025 22:40:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58f9f665d3c04d6bfaac3ce80ba636ce75ab95470cc0f20d90698dbf0e48a21`  
		Last Modified: Fri, 14 Feb 2025 22:40:10 GMT  
		Size: 1.2 MB (1226190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d69749d5bf90de3587c4ee4cb6bc93c8c06657a9a43bd45349ecbe7e28000`  
		Last Modified: Fri, 14 Feb 2025 22:40:10 GMT  
		Size: 18.3 MB (18290145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b217b49bcf8d231ad0be29e90559a86cf71a7c69d87fbcde6ea9fdc9ce890ed2`  
		Last Modified: Fri, 14 Feb 2025 22:40:10 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e590cc10505815ce504cb35c5a54e6ce48745e9056cf6b663c353770b5eeb6a0`  
		Last Modified: Fri, 14 Feb 2025 22:40:10 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:20:38 GMT  
		Size: 679.4 KB (679371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f443301cf502af1ad2d1bf6dc40192ee84a3ae01f7351cb118a6d2f8c6ff619`  
		Last Modified: Fri, 14 Feb 2025 21:20:38 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8`

```console
$ docker pull influxdb@sha256:f8be1f772fe0ee6f39456280c1df149274bb6808d1be5a54d394ee54cde2b13e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:9c35b76a52ac003bb1e885a870355e298e3a8f63a6b9edcf4f43af256785d69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116158328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18e92d7be70e67baa547ed3d7b40ab1503a696113f2dfcea3f2d7db9edc7026`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 21 May 2025 19:23:38 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
USER influxdb
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f6081745c045ec77e9e1fa3fc18646ff59c3f7299a3521a9f4e37496d81885`  
		Last Modified: Tue, 03 Jun 2025 13:39:46 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a139339f6ab016e27e13df6d898fe6c232867514003b409e728ea350cc0729`  
		Last Modified: Tue, 03 Jun 2025 13:49:48 GMT  
		Size: 43.7 MB (43651541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304aac6ae51f8a23ddc3d8f2f51a57ce2cde18650f6555ecdeedfbd261fa096a`  
		Last Modified: Tue, 03 Jun 2025 13:42:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c199006e6947fe8376e7fcf89daeb1d0e00a226f968d81681bb25cb2338fc8`  
		Last Modified: Tue, 03 Jun 2025 13:42:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc47f33351374435a50aed83d9ba8577a13e5546cde3a381be3d1504cf92c96`  
		Last Modified: Tue, 03 Jun 2025 13:42:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:7ec73ce3f86b85048b529930148793b87986c711d145d47783688dac546eb4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec3a93d03f1326df6e1d14f377bdb86429861d4e016416f30fc58cbb559f3df`

```dockerfile
```

-	Layers:
	-	`sha256:663016539b58dc2762de84707c9f0a7c38705f53c7d54b6aba8763cdd9aa799e`  
		Last Modified: Thu, 05 Jun 2025 11:28:43 GMT  
		Size: 4.9 MB (4912448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62fb8c4d4e497c944b88567a6eace3bc23bdfda0f73f251068a6b9975e121172`  
		Last Modified: Thu, 05 Jun 2025 11:28:45 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:08d55a308d1d5ae149ef852ceac8b69da5c0b78f60862bea24b68de8528b0144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113000809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3954bf2d07ad5caba738166648910024295abb1c8df49d26c935f1ba600bfa6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 21 May 2025 19:23:38 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
USER influxdb
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a8315385242d1d7ed00b9b26d3aee7f7327b635c12c8b4e2718171d6f32904`  
		Last Modified: Tue, 03 Jun 2025 13:56:22 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf27056cc96ff1052003b8778535377c992872e9536399c4942924191c1abd1`  
		Last Modified: Tue, 03 Jun 2025 13:56:39 GMT  
		Size: 41.1 MB (41119323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df259a20a4c9fd043b3c5ed299de62e5690119f11d6df9b424d632ce4dca31f7`  
		Last Modified: Tue, 03 Jun 2025 13:56:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35d41c533cf81a905f528f68fc355c19c014d83372ff338c56186e4f017ad1`  
		Last Modified: Tue, 03 Jun 2025 13:56:37 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa86bf8b96df0167c9ab6c0cd2cf6424f304abf209fb01bbd8ec1c11b6a29a`  
		Last Modified: Tue, 03 Jun 2025 13:56:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:d59742de0bd72db34df9b853b6608e79554e793c4ac091780c72f2094a975a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c168035e73b4dba24c52914eb6c73d522f283fcbb9285a0cd0b4266c0a13978`

```dockerfile
```

-	Layers:
	-	`sha256:95edccfa6877f089e828d365ddc0d7a270985a1be27c6ec4ce7cd9409cb0e44d`  
		Last Modified: Thu, 05 Jun 2025 11:28:45 GMT  
		Size: 4.9 MB (4911913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfcf57260da9d60377d2e04e409c81977dea23dd8f93217a24b408336f8e49ca`  
		Last Modified: Thu, 05 Jun 2025 11:28:47 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2430b91d27c94577a29aa4a63bc67b9a6bdb38f557ff03f2f47fe9fc4912a6e6`  
		Last Modified: Fri, 14 Feb 2025 21:20:46 GMT  
		Size: 1.2 MB (1226180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccd48b38856008daab1f21e8835b3d7b372598317d42820fc3f047db607ccec`  
		Last Modified: Fri, 14 Feb 2025 21:20:48 GMT  
		Size: 38.1 MB (38068218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94026e2b0d6f99fed3dedfb812a03fd046e8373145be2b2e4aee6b44295f325`  
		Last Modified: Fri, 14 Feb 2025 21:20:47 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfc22a651b18903f12176ed3447abf101612d8f6c009dde4beb5d65b864ff40`  
		Last Modified: Fri, 14 Feb 2025 21:20:47 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff30a98894f91ab375651dec55dbdaa6676482eba3ae74a247a1227bf992e1e`  
		Last Modified: Fri, 14 Feb 2025 21:20:48 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02c49477a92d638620b098485571f719849cc4a14d1a0bbbf9475ac5036c368`  
		Last Modified: Fri, 14 Feb 2025 21:20:49 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:20:28 GMT  
		Size: 743.3 KB (743321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f642c9f83ff2a959cec65a14ea556a5c772b8a03eecfc06b77b2212dd3f8fc78`  
		Last Modified: Fri, 14 Feb 2025 21:20:29 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e30a0c587fbc2e84c1b8c55a170ea149c6f6fb91469699f82a5d44e4dad9fdf`  
		Last Modified: Sat, 15 Feb 2025 09:18:20 GMT  
		Size: 1.3 MB (1307075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aedc2e6ed32b6b172146ed1536e1bc4675e2368a442a55fcbc77d582da9ded`  
		Last Modified: Sat, 15 Feb 2025 09:18:22 GMT  
		Size: 35.5 MB (35545506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f6a37ff4f04b2e3f6d6663dc1ad32dca8556db22f6aba5fa140293e06b8be6`  
		Last Modified: Sat, 15 Feb 2025 09:18:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e42b050238199a9cf809362968a20163c7d745329b332b4c122d9810b828e2`  
		Last Modified: Sat, 15 Feb 2025 09:18:23 GMT  
		Size: 995.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afc13286215e26f9388e94e989e8e7f25e3ba851d010c09add249a03c7801ee`  
		Last Modified: Sat, 15 Feb 2025 09:18:23 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644f23186760a8bda37888b6b2a4baf18413763b0df806f478204d981fb50ef4`  
		Last Modified: Sat, 15 Feb 2025 09:18:24 GMT  
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
		Last Modified: Sat, 15 Feb 2025 03:20:23 GMT  
		Size: 742.5 KB (742548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b1bc5d6ee15c6f1c9cb67454a907a5fafdc070f8a6cfd9143ff759f6ff93bd`  
		Last Modified: Sat, 15 Feb 2025 03:20:23 GMT  
		Size: 18.0 KB (17984 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-data`

```console
$ docker pull influxdb@sha256:191a6a43ab3f0df53d9114370c8a6255ccd2efefe15871789c68f48adac0982f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:88565463c063725a0767b346a0d1c397b9f4a27bb824e15c713e74e816facbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111686726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6a1c5aa907fcb609aeea67536614e3e1ff76d1444524a8cac79edfc9cee74a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Wed, 21 May 2025 19:23:38 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea0d0d8518a8abb507c1c1f8848acf6bda32f7e3a92bd89de26ddd51d4a18cc`  
		Last Modified: Tue, 03 Jun 2025 21:35:41 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62590ca4a361feedc7ca878d537fd9b2d955c265a7e3cf70f5a45705b6f3012d`  
		Last Modified: Tue, 03 Jun 2025 21:35:43 GMT  
		Size: 39.2 MB (39179288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a3720d1c7e49bb139b98e68b023b0806fec0e1f9675980b9df459f9fe765bf`  
		Last Modified: Tue, 03 Jun 2025 21:35:41 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2352797ca35b81f033e84c396fde8c7d43075cef9ba47766f64d5a4952dff058`  
		Last Modified: Tue, 03 Jun 2025 21:35:43 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d8cef0ec440de11cc6d12eca5c6f3c55b854d4dec675973ab666b9b7f566a0`  
		Last Modified: Tue, 03 Jun 2025 21:35:43 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:5b35e79b7bb00e5004b80bf30f85eaff73b9adffb540491433b70fe8e599e720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4549395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53fd67e793c2c63b87d9169059f6ee90f1cb3635c6010a387266a9ec773673c`

```dockerfile
```

-	Layers:
	-	`sha256:e7ccc061dc847b3b66176b83e8f67949be6cf4a05f56d728fe96711e0765666a`  
		Last Modified: Wed, 21 May 2025 23:40:33 GMT  
		Size: 4.5 MB (4534688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bde0f7169d31d9fc1d821007f59d77dc3bcd3355df151bb04a75f8e6857b366`  
		Last Modified: Wed, 21 May 2025 23:40:33 GMT  
		Size: 14.7 KB (14707 bytes)  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d5b5d68d9f3f80ff363fb8fe3e7a2685990aa9ec18892b275d90a98637fd17`  
		Last Modified: Fri, 14 Feb 2025 21:20:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41957e5bb968a4cefc35246db18ec3931c853e733e93c5deb740f35f7e84c2e`  
		Last Modified: Fri, 14 Feb 2025 22:38:01 GMT  
		Size: 1.2 MB (1226185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468f4a21923f4bd549c35732446830e62e956dc03cdfd2c2d232f42d0e5009eb`  
		Last Modified: Fri, 14 Feb 2025 22:38:04 GMT  
		Size: 39.1 MB (39123831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb276187bda5db3e631d8724e8f410f96a6fec1390f6e75843194034f808c84`  
		Last Modified: Fri, 14 Feb 2025 22:38:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850540575a0c377c0f3b7ae91868304b5c287a5cb70ace26bbe032383b2c56ea`  
		Last Modified: Fri, 14 Feb 2025 22:38:02 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfd23d02f8457ddfcf7d4ccf1c6bb08ad6f3a8477e528e6a15a319acf3a2815`  
		Last Modified: Fri, 14 Feb 2025 22:38:02 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:20:32 GMT  
		Size: 753.9 KB (753866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9454c17edf183df5c9482191597585786c035bd37719a2898cd15830eb5307de`  
		Last Modified: Fri, 14 Feb 2025 21:20:32 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-meta`

```console
$ docker pull influxdb@sha256:ec7aabe307c301c30b5c84a3183f8bf7d9692b2c664ac991495677e9ed3c58d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:78a646c72a24c064c4fc629df9fdd01d2a030b38a8b8a75bfcf6d8e0aa922b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90842809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dd649ee56f245ae5ba45c0245549c58b7feff0387edda68e616f327952010b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Wed, 21 May 2025 19:23:38 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ff50dac0b60c61e3f208089d0bdb169219a52c9f966a8a9c726b08d65a7131`  
		Last Modified: Tue, 03 Jun 2025 21:37:39 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d1075191495374d278cccce1a169df1216308a6501cb4e894404e424f09a8e`  
		Last Modified: Tue, 03 Jun 2025 21:37:41 GMT  
		Size: 18.3 MB (18336578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341d9611206bcf2b17e222fe111c20a4f43d91e736e1c44417feba67b308e529`  
		Last Modified: Tue, 03 Jun 2025 21:37:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe66ddd7b7ccfcfb8661e5ad4ac0ea03b7aaaf60fddf203ba9065f71067005c9`  
		Last Modified: Tue, 03 Jun 2025 21:37:41 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:0d1ddbf322c8975edec4b256a4ff106cc9ba35cdad1c6b6b51682c3cecb69204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d77c0cbf7e37e0450255f2f03166ebaed2af5fc42bbbae1b5d228419dedac2`

```dockerfile
```

-	Layers:
	-	`sha256:162e00800135c98d09eb438e234dbeafc196ede45c5981b54e2da959c2ac7c07`  
		Last Modified: Wed, 21 May 2025 23:40:26 GMT  
		Size: 4.5 MB (4459659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77a57150a0f00a1a7182cb36b1bcd65deb64c9709afec8f68a1ec8f0fdcbe84a`  
		Last Modified: Wed, 21 May 2025 23:40:26 GMT  
		Size: 13.1 KB (13067 bytes)  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4179006b77d77220705fbc7483a58da67581ebd4d5bf829d0980b8db79003f1e`  
		Last Modified: Fri, 14 Feb 2025 22:40:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58f9f665d3c04d6bfaac3ce80ba636ce75ab95470cc0f20d90698dbf0e48a21`  
		Last Modified: Fri, 14 Feb 2025 22:40:10 GMT  
		Size: 1.2 MB (1226190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d69749d5bf90de3587c4ee4cb6bc93c8c06657a9a43bd45349ecbe7e28000`  
		Last Modified: Fri, 14 Feb 2025 22:40:10 GMT  
		Size: 18.3 MB (18290145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b217b49bcf8d231ad0be29e90559a86cf71a7c69d87fbcde6ea9fdc9ce890ed2`  
		Last Modified: Fri, 14 Feb 2025 22:40:10 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e590cc10505815ce504cb35c5a54e6ce48745e9056cf6b663c353770b5eeb6a0`  
		Last Modified: Fri, 14 Feb 2025 22:40:10 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:20:38 GMT  
		Size: 679.4 KB (679371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f443301cf502af1ad2d1bf6dc40192ee84a3ae01f7351cb118a6d2f8c6ff619`  
		Last Modified: Fri, 14 Feb 2025 21:20:38 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:d4d96a93b3d238fa2577916e501304cc32a206efd9f1eb163f18e9d21b3983a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:549a15b5f66acff43b670a6d2182829dae27abe6456ff80ff8af9b958750fcc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168642983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff72781800ab8302b2b10d8eea3ff3a54bf61c1fa388fa7a1c4cdcac1aa8f828`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f36ae94f40a7aa5fd6bca9f3c08cf4719e80d591037c7a4b94d1539744a8fb`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 9.8 MB (9791034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe37dd6f8888efc5da91f2f29534eed01e10e2cb86c784254b43db36562dc8c`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6efd9c01e056a7294fa312b86336fe6f439b89bc5129eee70623703ccf7aa8`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a8e265719c2793ca28cadc5376391c897c89f6726e101bad2a7c247f364ffb`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394da5cd13ce2b03effce819aa590edf6649db4afc44de6c21df01bddf11bf94`  
		Last Modified: Tue, 03 Jun 2025 13:30:56 GMT  
		Size: 100.2 MB (100242960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d10ee91c71ce63c26fa20756e8e9073885a91e3759cfebceae9a440a7f4706`  
		Last Modified: Tue, 03 Jun 2025 13:33:07 GMT  
		Size: 23.5 MB (23546404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d829ed22f9224c3579e98603469332a0cc2aaa54e20430745ff2ac440dc1fc8`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead9edcf8ee593eeb009b7e83c7049aa141da36206ea7a4e016b9f9c17244e6b`  
		Last Modified: Tue, 03 Jun 2025 13:30:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc84b868a5d32847815f5cede5ad639bd1f4a8e9468c81ac4d8e8d82e610f3d1`  
		Last Modified: Tue, 03 Jun 2025 13:30:46 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:279a20561406f515dbce4a46eef0013bf0d169fee238b91c177703aeb5ee4f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2903032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d571e2519980a093a8966be30679f80d3c3907038a74d7b7624d81b2e2d13e4b`

```dockerfile
```

-	Layers:
	-	`sha256:8c2886d35940c270ee63e635039d82c1202bdc2159aecf8a884b355111d7a7b5`  
		Last Modified: Wed, 04 Jun 2025 02:29:58 GMT  
		Size: 2.9 MB (2869214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206a20f20680f68235164eecb4834095f5cfe784f61caf8e675da45390e333cb`  
		Last Modified: Wed, 04 Jun 2025 02:30:16 GMT  
		Size: 33.8 KB (33818 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:86bb738da2c4ece12e0cd4753d41a1d164eaedf778c960fff7ae9acef9961b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162300102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a961c9d0be3a43097e88ce7a44a554a8286cb7200e4ed38c72d18eed7f0120a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fb2485b7c4399692ff0f858e85a493f7520a8d7a7c0fea3fdb10af035ca4db`  
		Last Modified: Tue, 03 Jun 2025 13:32:48 GMT  
		Size: 9.6 MB (9588655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a652ae87fbc6c53da5a0254038a21966076bf080aca8e2d28ba72b5d420d5f9`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 5.5 MB (5463794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f002cc60651d1b940830c2474392559655131840a6ee05d3fa3ad46043e8d717`  
		Last Modified: Tue, 03 Jun 2025 13:32:49 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2659eb1f1bde104f3c076174116ef9f4048e77b37a35cb0084f845af628f08`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110b9d474b0a3bc25d10ea3255f2a23ffce66575ff780d6882a1a7123a73c313`  
		Last Modified: Tue, 03 Jun 2025 13:33:06 GMT  
		Size: 96.0 MB (96038373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd6afc77b240651bd89398eb9b69f97346e697cc5cb0b9f4ff0edbed4f17fca`  
		Last Modified: Tue, 03 Jun 2025 13:32:53 GMT  
		Size: 22.2 MB (22197938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aac4036678859e629ddc5174b7ee3f6f51cd04b7985d07ac05b27028ed0816`  
		Last Modified: Tue, 03 Jun 2025 13:32:51 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc68c4f14fa754f1b66375f3dcd348c039bdb940b5430a4b9c3eaab2018d16c`  
		Last Modified: Tue, 03 Jun 2025 13:32:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940c0915463d99c5f92547a5c658ec36fe7e548d303c2319b315bb21e85d671`  
		Last Modified: Tue, 03 Jun 2025 13:32:53 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:123be7ccf66e93ac0b6f0960dafa5a2f75c89c5d8bffd23e4124b8918be6d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2902443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e621672e616043de6a8903502ee7f1a98c758bdba5fe9fbfc5c68be6e40653`

```dockerfile
```

-	Layers:
	-	`sha256:8dde95519976874c08bc5ae53076ab1ce50b41c1f5a3d97f4bab939a4f6d24b2`  
		Last Modified: Wed, 04 Jun 2025 02:53:09 GMT  
		Size: 2.9 MB (2868442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca8ec741f51106258a1e51e9c3c07486d7942d4641b3f09816b959c83077987`  
		Last Modified: Wed, 04 Jun 2025 02:53:21 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b4da6257d4dab81f7ea9b217e8990fa02b532b487dc09f66cfe66b7a5ab1b7`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f227616a4b65630020272b1a4736c45d2072fea1f6ae56d8987f001bff1868e5`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 9.7 MB (9668254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28153e71486f54b7e2d6898878271446058952c9919aaad4310fd5662e14073`  
		Last Modified: Tue, 03 Jun 2025 13:35:12 GMT  
		Size: 5.8 MB (5820951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17da966601b69ee27cf7e07f71e8d3a293465f510f662a95761c204c476039`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f351545292c8d4b32b561f37f2761b8143e35ea7b2aed6ada764d91675953e2`  
		Last Modified: Tue, 03 Jun 2025 13:35:16 GMT  
		Size: 50.1 MB (50115457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec39c678e278ff055d4d22e8402129df928caa4a2647ff3024e97721f0f5943`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 23.5 MB (23546414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428d400809cb7ad31d35a7f2d948c8121b3f7499c617f94eb95080f6705d2c6`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195b609b670962adf4a4fd55112b8f3ee09ab9b864b63db78893c7e7b6de06aa`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213bcca749f51ef7f5ebe65ef3ee91941b8ead606c2179e2247bba98e5d1ba1`  
		Last Modified: Tue, 03 Jun 2025 13:35:14 GMT  
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
		Last Modified: Wed, 04 Jun 2025 00:38:08 GMT  
		Size: 918.5 KB (918468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15b588c6b6124a1aa918ae48f879aa8e721ecd2db834e3c78af76a20738c283`  
		Last Modified: Wed, 04 Jun 2025 00:38:22 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c8ed1b411bf87e31d51dcd5e11ad29b842c6ac23d29867f58c9b6657217f9`  
		Last Modified: Thu, 08 May 2025 17:16:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7581744a5f8b851a37b006b9f70c0dfc1aabfbbf6e54e0d468d11332b9a89155`  
		Last Modified: Tue, 03 Jun 2025 13:33:06 GMT  
		Size: 9.8 MB (9790275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8e2420533fb94a98c3c0cea702d65af3aac200564d71bf02039933d45752c4`  
		Last Modified: Tue, 03 Jun 2025 13:32:59 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d98ff612225a614c58f5f650b55a20d2a5f607933c56ec0b343dc54d39316`  
		Last Modified: Tue, 03 Jun 2025 13:32:59 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9943be5d4ecac40794357058ec1ead2ffe57b93ad82f1c046f9490950fb8be`  
		Last Modified: Tue, 03 Jun 2025 13:33:07 GMT  
		Size: 48.0 MB (48016208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592941019971dc33dba5c666bebc57139662a00acd86e6dc6e85310542b62a90`  
		Last Modified: Tue, 03 Jun 2025 13:33:08 GMT  
		Size: 22.2 MB (22197933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a652dc6c421b2c1298eb71f3a1a77ad5317359d42f97d2ba7e0256166f7908`  
		Last Modified: Tue, 03 Jun 2025 13:33:10 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c5c55779859032454928168c0eaf5620289e22d09443a4c303e920fbc0f25e`  
		Last Modified: Tue, 03 Jun 2025 13:33:10 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c5a87a5ee69568a4bb3e3c7fbcb83b0bd9250e68ef8618525ab0df87a7c0`  
		Last Modified: Tue, 03 Jun 2025 13:33:11 GMT  
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
		Last Modified: Wed, 04 Jun 2025 02:56:34 GMT  
		Size: 917.7 KB (917719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f4f5e2584d7feb4ec7fc289bad890abb4f9f813f7c20ca231fb580b0db01d6d`  
		Last Modified: Wed, 04 Jun 2025 02:56:42 GMT  
		Size: 31.2 KB (31241 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:d4d96a93b3d238fa2577916e501304cc32a206efd9f1eb163f18e9d21b3983a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:549a15b5f66acff43b670a6d2182829dae27abe6456ff80ff8af9b958750fcc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168642983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff72781800ab8302b2b10d8eea3ff3a54bf61c1fa388fa7a1c4cdcac1aa8f828`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f36ae94f40a7aa5fd6bca9f3c08cf4719e80d591037c7a4b94d1539744a8fb`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 9.8 MB (9791034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe37dd6f8888efc5da91f2f29534eed01e10e2cb86c784254b43db36562dc8c`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6efd9c01e056a7294fa312b86336fe6f439b89bc5129eee70623703ccf7aa8`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a8e265719c2793ca28cadc5376391c897c89f6726e101bad2a7c247f364ffb`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394da5cd13ce2b03effce819aa590edf6649db4afc44de6c21df01bddf11bf94`  
		Last Modified: Tue, 03 Jun 2025 13:30:56 GMT  
		Size: 100.2 MB (100242960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d10ee91c71ce63c26fa20756e8e9073885a91e3759cfebceae9a440a7f4706`  
		Last Modified: Tue, 03 Jun 2025 13:33:07 GMT  
		Size: 23.5 MB (23546404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d829ed22f9224c3579e98603469332a0cc2aaa54e20430745ff2ac440dc1fc8`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead9edcf8ee593eeb009b7e83c7049aa141da36206ea7a4e016b9f9c17244e6b`  
		Last Modified: Tue, 03 Jun 2025 13:30:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc84b868a5d32847815f5cede5ad639bd1f4a8e9468c81ac4d8e8d82e610f3d1`  
		Last Modified: Tue, 03 Jun 2025 13:30:46 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:279a20561406f515dbce4a46eef0013bf0d169fee238b91c177703aeb5ee4f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2903032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d571e2519980a093a8966be30679f80d3c3907038a74d7b7624d81b2e2d13e4b`

```dockerfile
```

-	Layers:
	-	`sha256:8c2886d35940c270ee63e635039d82c1202bdc2159aecf8a884b355111d7a7b5`  
		Last Modified: Wed, 04 Jun 2025 02:29:58 GMT  
		Size: 2.9 MB (2869214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206a20f20680f68235164eecb4834095f5cfe784f61caf8e675da45390e333cb`  
		Last Modified: Wed, 04 Jun 2025 02:30:16 GMT  
		Size: 33.8 KB (33818 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:86bb738da2c4ece12e0cd4753d41a1d164eaedf778c960fff7ae9acef9961b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162300102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a961c9d0be3a43097e88ce7a44a554a8286cb7200e4ed38c72d18eed7f0120a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fb2485b7c4399692ff0f858e85a493f7520a8d7a7c0fea3fdb10af035ca4db`  
		Last Modified: Tue, 03 Jun 2025 13:32:48 GMT  
		Size: 9.6 MB (9588655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a652ae87fbc6c53da5a0254038a21966076bf080aca8e2d28ba72b5d420d5f9`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 5.5 MB (5463794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f002cc60651d1b940830c2474392559655131840a6ee05d3fa3ad46043e8d717`  
		Last Modified: Tue, 03 Jun 2025 13:32:49 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2659eb1f1bde104f3c076174116ef9f4048e77b37a35cb0084f845af628f08`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110b9d474b0a3bc25d10ea3255f2a23ffce66575ff780d6882a1a7123a73c313`  
		Last Modified: Tue, 03 Jun 2025 13:33:06 GMT  
		Size: 96.0 MB (96038373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd6afc77b240651bd89398eb9b69f97346e697cc5cb0b9f4ff0edbed4f17fca`  
		Last Modified: Tue, 03 Jun 2025 13:32:53 GMT  
		Size: 22.2 MB (22197938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aac4036678859e629ddc5174b7ee3f6f51cd04b7985d07ac05b27028ed0816`  
		Last Modified: Tue, 03 Jun 2025 13:32:51 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc68c4f14fa754f1b66375f3dcd348c039bdb940b5430a4b9c3eaab2018d16c`  
		Last Modified: Tue, 03 Jun 2025 13:32:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940c0915463d99c5f92547a5c658ec36fe7e548d303c2319b315bb21e85d671`  
		Last Modified: Tue, 03 Jun 2025 13:32:53 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:123be7ccf66e93ac0b6f0960dafa5a2f75c89c5d8bffd23e4124b8918be6d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2902443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e621672e616043de6a8903502ee7f1a98c758bdba5fe9fbfc5c68be6e40653`

```dockerfile
```

-	Layers:
	-	`sha256:8dde95519976874c08bc5ae53076ab1ce50b41c1f5a3d97f4bab939a4f6d24b2`  
		Last Modified: Wed, 04 Jun 2025 02:53:09 GMT  
		Size: 2.9 MB (2868442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca8ec741f51106258a1e51e9c3c07486d7942d4641b3f09816b959c83077987`  
		Last Modified: Wed, 04 Jun 2025 02:53:21 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b4da6257d4dab81f7ea9b217e8990fa02b532b487dc09f66cfe66b7a5ab1b7`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f227616a4b65630020272b1a4736c45d2072fea1f6ae56d8987f001bff1868e5`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 9.7 MB (9668254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28153e71486f54b7e2d6898878271446058952c9919aaad4310fd5662e14073`  
		Last Modified: Tue, 03 Jun 2025 13:35:12 GMT  
		Size: 5.8 MB (5820951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17da966601b69ee27cf7e07f71e8d3a293465f510f662a95761c204c476039`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f351545292c8d4b32b561f37f2761b8143e35ea7b2aed6ada764d91675953e2`  
		Last Modified: Tue, 03 Jun 2025 13:35:16 GMT  
		Size: 50.1 MB (50115457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec39c678e278ff055d4d22e8402129df928caa4a2647ff3024e97721f0f5943`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 23.5 MB (23546414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428d400809cb7ad31d35a7f2d948c8121b3f7499c617f94eb95080f6705d2c6`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195b609b670962adf4a4fd55112b8f3ee09ab9b864b63db78893c7e7b6de06aa`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213bcca749f51ef7f5ebe65ef3ee91941b8ead606c2179e2247bba98e5d1ba1`  
		Last Modified: Tue, 03 Jun 2025 13:35:14 GMT  
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
		Last Modified: Wed, 04 Jun 2025 00:38:08 GMT  
		Size: 918.5 KB (918468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15b588c6b6124a1aa918ae48f879aa8e721ecd2db834e3c78af76a20738c283`  
		Last Modified: Wed, 04 Jun 2025 00:38:22 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c8ed1b411bf87e31d51dcd5e11ad29b842c6ac23d29867f58c9b6657217f9`  
		Last Modified: Thu, 08 May 2025 17:16:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7581744a5f8b851a37b006b9f70c0dfc1aabfbbf6e54e0d468d11332b9a89155`  
		Last Modified: Tue, 03 Jun 2025 13:33:06 GMT  
		Size: 9.8 MB (9790275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8e2420533fb94a98c3c0cea702d65af3aac200564d71bf02039933d45752c4`  
		Last Modified: Tue, 03 Jun 2025 13:32:59 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d98ff612225a614c58f5f650b55a20d2a5f607933c56ec0b343dc54d39316`  
		Last Modified: Tue, 03 Jun 2025 13:32:59 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9943be5d4ecac40794357058ec1ead2ffe57b93ad82f1c046f9490950fb8be`  
		Last Modified: Tue, 03 Jun 2025 13:33:07 GMT  
		Size: 48.0 MB (48016208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592941019971dc33dba5c666bebc57139662a00acd86e6dc6e85310542b62a90`  
		Last Modified: Tue, 03 Jun 2025 13:33:08 GMT  
		Size: 22.2 MB (22197933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a652dc6c421b2c1298eb71f3a1a77ad5317359d42f97d2ba7e0256166f7908`  
		Last Modified: Tue, 03 Jun 2025 13:33:10 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c5c55779859032454928168c0eaf5620289e22d09443a4c303e920fbc0f25e`  
		Last Modified: Tue, 03 Jun 2025 13:33:10 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c5a87a5ee69568a4bb3e3c7fbcb83b0bd9250e68ef8618525ab0df87a7c0`  
		Last Modified: Tue, 03 Jun 2025 13:33:11 GMT  
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
		Last Modified: Wed, 04 Jun 2025 02:56:34 GMT  
		Size: 917.7 KB (917719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f4f5e2584d7feb4ec7fc289bad890abb4f9f813f7c20ca231fb580b0db01d6d`  
		Last Modified: Wed, 04 Jun 2025 02:56:42 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b4da6257d4dab81f7ea9b217e8990fa02b532b487dc09f66cfe66b7a5ab1b7`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f227616a4b65630020272b1a4736c45d2072fea1f6ae56d8987f001bff1868e5`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 9.7 MB (9668254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28153e71486f54b7e2d6898878271446058952c9919aaad4310fd5662e14073`  
		Last Modified: Tue, 03 Jun 2025 13:35:12 GMT  
		Size: 5.8 MB (5820951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17da966601b69ee27cf7e07f71e8d3a293465f510f662a95761c204c476039`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f351545292c8d4b32b561f37f2761b8143e35ea7b2aed6ada764d91675953e2`  
		Last Modified: Tue, 03 Jun 2025 13:35:16 GMT  
		Size: 50.1 MB (50115457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec39c678e278ff055d4d22e8402129df928caa4a2647ff3024e97721f0f5943`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 23.5 MB (23546414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428d400809cb7ad31d35a7f2d948c8121b3f7499c617f94eb95080f6705d2c6`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195b609b670962adf4a4fd55112b8f3ee09ab9b864b63db78893c7e7b6de06aa`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213bcca749f51ef7f5ebe65ef3ee91941b8ead606c2179e2247bba98e5d1ba1`  
		Last Modified: Tue, 03 Jun 2025 13:35:14 GMT  
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
		Last Modified: Wed, 04 Jun 2025 00:38:08 GMT  
		Size: 918.5 KB (918468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15b588c6b6124a1aa918ae48f879aa8e721ecd2db834e3c78af76a20738c283`  
		Last Modified: Wed, 04 Jun 2025 00:38:22 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c8ed1b411bf87e31d51dcd5e11ad29b842c6ac23d29867f58c9b6657217f9`  
		Last Modified: Thu, 08 May 2025 17:16:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7581744a5f8b851a37b006b9f70c0dfc1aabfbbf6e54e0d468d11332b9a89155`  
		Last Modified: Tue, 03 Jun 2025 13:33:06 GMT  
		Size: 9.8 MB (9790275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8e2420533fb94a98c3c0cea702d65af3aac200564d71bf02039933d45752c4`  
		Last Modified: Tue, 03 Jun 2025 13:32:59 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d98ff612225a614c58f5f650b55a20d2a5f607933c56ec0b343dc54d39316`  
		Last Modified: Tue, 03 Jun 2025 13:32:59 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9943be5d4ecac40794357058ec1ead2ffe57b93ad82f1c046f9490950fb8be`  
		Last Modified: Tue, 03 Jun 2025 13:33:07 GMT  
		Size: 48.0 MB (48016208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592941019971dc33dba5c666bebc57139662a00acd86e6dc6e85310542b62a90`  
		Last Modified: Tue, 03 Jun 2025 13:33:08 GMT  
		Size: 22.2 MB (22197933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a652dc6c421b2c1298eb71f3a1a77ad5317359d42f97d2ba7e0256166f7908`  
		Last Modified: Tue, 03 Jun 2025 13:33:10 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c5c55779859032454928168c0eaf5620289e22d09443a4c303e920fbc0f25e`  
		Last Modified: Tue, 03 Jun 2025 13:33:10 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c5a87a5ee69568a4bb3e3c7fbcb83b0bd9250e68ef8618525ab0df87a7c0`  
		Last Modified: Tue, 03 Jun 2025 13:33:11 GMT  
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
		Last Modified: Wed, 04 Jun 2025 02:56:34 GMT  
		Size: 917.7 KB (917719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f4f5e2584d7feb4ec7fc289bad890abb4f9f813f7c20ca231fb580b0db01d6d`  
		Last Modified: Wed, 04 Jun 2025 02:56:42 GMT  
		Size: 31.2 KB (31241 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12`

```console
$ docker pull influxdb@sha256:d4d96a93b3d238fa2577916e501304cc32a206efd9f1eb163f18e9d21b3983a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:549a15b5f66acff43b670a6d2182829dae27abe6456ff80ff8af9b958750fcc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168642983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff72781800ab8302b2b10d8eea3ff3a54bf61c1fa388fa7a1c4cdcac1aa8f828`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f36ae94f40a7aa5fd6bca9f3c08cf4719e80d591037c7a4b94d1539744a8fb`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 9.8 MB (9791034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe37dd6f8888efc5da91f2f29534eed01e10e2cb86c784254b43db36562dc8c`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6efd9c01e056a7294fa312b86336fe6f439b89bc5129eee70623703ccf7aa8`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a8e265719c2793ca28cadc5376391c897c89f6726e101bad2a7c247f364ffb`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394da5cd13ce2b03effce819aa590edf6649db4afc44de6c21df01bddf11bf94`  
		Last Modified: Tue, 03 Jun 2025 13:30:56 GMT  
		Size: 100.2 MB (100242960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d10ee91c71ce63c26fa20756e8e9073885a91e3759cfebceae9a440a7f4706`  
		Last Modified: Tue, 03 Jun 2025 13:33:07 GMT  
		Size: 23.5 MB (23546404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d829ed22f9224c3579e98603469332a0cc2aaa54e20430745ff2ac440dc1fc8`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead9edcf8ee593eeb009b7e83c7049aa141da36206ea7a4e016b9f9c17244e6b`  
		Last Modified: Tue, 03 Jun 2025 13:30:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc84b868a5d32847815f5cede5ad639bd1f4a8e9468c81ac4d8e8d82e610f3d1`  
		Last Modified: Tue, 03 Jun 2025 13:30:46 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:279a20561406f515dbce4a46eef0013bf0d169fee238b91c177703aeb5ee4f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2903032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d571e2519980a093a8966be30679f80d3c3907038a74d7b7624d81b2e2d13e4b`

```dockerfile
```

-	Layers:
	-	`sha256:8c2886d35940c270ee63e635039d82c1202bdc2159aecf8a884b355111d7a7b5`  
		Last Modified: Wed, 04 Jun 2025 02:29:58 GMT  
		Size: 2.9 MB (2869214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206a20f20680f68235164eecb4834095f5cfe784f61caf8e675da45390e333cb`  
		Last Modified: Wed, 04 Jun 2025 02:30:16 GMT  
		Size: 33.8 KB (33818 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:86bb738da2c4ece12e0cd4753d41a1d164eaedf778c960fff7ae9acef9961b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162300102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a961c9d0be3a43097e88ce7a44a554a8286cb7200e4ed38c72d18eed7f0120a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fb2485b7c4399692ff0f858e85a493f7520a8d7a7c0fea3fdb10af035ca4db`  
		Last Modified: Tue, 03 Jun 2025 13:32:48 GMT  
		Size: 9.6 MB (9588655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a652ae87fbc6c53da5a0254038a21966076bf080aca8e2d28ba72b5d420d5f9`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 5.5 MB (5463794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f002cc60651d1b940830c2474392559655131840a6ee05d3fa3ad46043e8d717`  
		Last Modified: Tue, 03 Jun 2025 13:32:49 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2659eb1f1bde104f3c076174116ef9f4048e77b37a35cb0084f845af628f08`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110b9d474b0a3bc25d10ea3255f2a23ffce66575ff780d6882a1a7123a73c313`  
		Last Modified: Tue, 03 Jun 2025 13:33:06 GMT  
		Size: 96.0 MB (96038373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd6afc77b240651bd89398eb9b69f97346e697cc5cb0b9f4ff0edbed4f17fca`  
		Last Modified: Tue, 03 Jun 2025 13:32:53 GMT  
		Size: 22.2 MB (22197938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aac4036678859e629ddc5174b7ee3f6f51cd04b7985d07ac05b27028ed0816`  
		Last Modified: Tue, 03 Jun 2025 13:32:51 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc68c4f14fa754f1b66375f3dcd348c039bdb940b5430a4b9c3eaab2018d16c`  
		Last Modified: Tue, 03 Jun 2025 13:32:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940c0915463d99c5f92547a5c658ec36fe7e548d303c2319b315bb21e85d671`  
		Last Modified: Tue, 03 Jun 2025 13:32:53 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:123be7ccf66e93ac0b6f0960dafa5a2f75c89c5d8bffd23e4124b8918be6d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2902443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e621672e616043de6a8903502ee7f1a98c758bdba5fe9fbfc5c68be6e40653`

```dockerfile
```

-	Layers:
	-	`sha256:8dde95519976874c08bc5ae53076ab1ce50b41c1f5a3d97f4bab939a4f6d24b2`  
		Last Modified: Wed, 04 Jun 2025 02:53:09 GMT  
		Size: 2.9 MB (2868442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca8ec741f51106258a1e51e9c3c07486d7942d4641b3f09816b959c83077987`  
		Last Modified: Wed, 04 Jun 2025 02:53:21 GMT  
		Size: 34.0 KB (34001 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:62276b5841c54271f8f61aa75754dd094ac8889e0e3df13143eb2efa2f3436e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:a7f5988e704d20af512ded712e606675ddaf213929c6d556ed4caf6ba96ae6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100472165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c592d615a3cb3965f7cdc670ca7b02f97b5eb3ada619180fb3cd5521a9ddf5c`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415828e81f66be2d39a188fc960aba46954c3db258660e742ff52cf4f0e6e60a`  
		Last Modified: Tue, 03 Jun 2025 13:35:48 GMT  
		Size: 6.7 MB (6664721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe12f1647cb94de2de19506a5b5f51d03a7359f84d56e4483311b111e817822`  
		Last Modified: Tue, 03 Jun 2025 13:35:47 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2a04f802fa083a74f8c76eae857e4a46d9021994d9c8b81b17e5929a013aea`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 64.1 MB (64087981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409bd07e13d183155e74480126a33360af6dc221228aec11ce46ed5d63e4d085`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af136bf052559a168911c3e729ed692d08d6955e245b953ff8f74ef2d3fc27b`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:0066ef00ebea27639b9dd8243b8df17185d184e3d34f919bec1c58becb539708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c305bffc31d1939e6029089f0fcf3a4434b505f29362598d4928a585b92a1037`

```dockerfile
```

-	Layers:
	-	`sha256:166b502ace1381b5ebd32cc82d5f50fb91c3ef2dc426578038d59b38a602010c`  
		Last Modified: Tue, 03 Jun 2025 20:03:47 GMT  
		Size: 2.2 MB (2203212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c78f2b9c924919852429713a045188114cae36757f3f7fe3ded6ae8974935f5`  
		Last Modified: Tue, 03 Jun 2025 20:03:47 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d565003cd08557d0d4885c62452d14520b7a774c4d41dbbf5ef01f90e73d3872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93633161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bfb7469d2a672c94d3864b417bf6b936cd9bfb8bbe6d32561d346aae6bcf31`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482dc2248542ad585f759b15b9f85e27167e3c6c47fc1456d4412f92d2b4a423`  
		Last Modified: Tue, 03 Jun 2025 14:03:42 GMT  
		Size: 6.7 MB (6675420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3847e841b0f506b2979520cb832f1496a88ad872d8e318581cdfd88d37e32130`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2c137e0375813389bf40bbfad44d45608abbe59734689ac532f1a5dbbff8b2`  
		Last Modified: Tue, 03 Jun 2025 14:03:45 GMT  
		Size: 58.1 MB (58101718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae24e95b9f166b6b3ebea08eea7d717d0b5ca7fcf87788dfe0bb16b97363fa2`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d9d3678a4dd2eb245fa14e1668a4c4c9d47b581a58ec40dc4ab45d5c4ada5a`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:cf543f2c8896e9aaba2f986fb765bd7cc039cf463f2b89099bc76705c99716fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad13c9d3b48bdc61723f1a4d050e2e7131853eca29770774ece2748ab9be4c4f`

```dockerfile
```

-	Layers:
	-	`sha256:5d98149c039782896eafba0c7a3ee345f167cffbdd64264d8e263d7823c5b2a0`  
		Last Modified: Tue, 03 Jun 2025 20:04:11 GMT  
		Size: 2.2 MB (2204294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d15e75bb0d6561c16162f2f9cd0f555ac48770a99d3d2150b35f7f78f029d90`  
		Last Modified: Tue, 03 Jun 2025 20:04:10 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:a1944483af83406ee1b2ebdb66f20a704c311571dedc92aeacd46de46895dae2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6f8ea6dcb55362b0d132b7f69922d834a13d1e7922bcaa8278f412ba0e6f5888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103272989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0b28dfdebea55635b41ec4b137cc3865c987f2b3a8328a0255651a0f5f283c`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c21a2128df4c0b3a1a2a3a7451bc55de7acd7667af0c240008a2de740bc3c21`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 6.7 MB (6664721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcf4966be8170f2e514212b42f0941cc3bc0884771a3c37f15ecdd9ae506cfd`  
		Last Modified: Tue, 03 Jun 2025 13:30:49 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cddcd3193a56e570adb2aae85fd9003a155a3a33efd539baf6472a26926b660`  
		Last Modified: Tue, 03 Jun 2025 13:30:54 GMT  
		Size: 66.9 MB (66888800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf62a59e48bd026bbd4e6e1f76ee899422645120d9f727cf59f86f3c7cba7d`  
		Last Modified: Tue, 03 Jun 2025 13:30:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc677efed44bfe802ade6813bf557d4176a30e17bb52c80f5a55a9d22c92269`  
		Last Modified: Tue, 03 Jun 2025 13:30:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:58c92711cc95e02318be2536aeccb756ce6e1136ec91c1e9195f8ae0fbbdccc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fc48d31a60cdcceafb5c3e408e1a4ad7ba8c8020ed845f9605aa013ac4852b`

```dockerfile
```

-	Layers:
	-	`sha256:023afb9e0f1e8d258db1fea55efffc04398e06410645b1ad839a17868498398e`  
		Last Modified: Tue, 03 Jun 2025 04:16:32 GMT  
		Size: 2.2 MB (2203260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f205c8b6ef888b50c090dc278e429864438a6d7b54fd3a3a6fbe7282bc257604`  
		Last Modified: Tue, 03 Jun 2025 04:16:32 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0d46086d38d16ef0418a77551f66e98c4f0bc7def594ade4dfd8e306be7137a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96342836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed042af4efe792b6203b9912a6223ac97a8d63fd8ed3aa8637115fa29a7691c1`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482dc2248542ad585f759b15b9f85e27167e3c6c47fc1456d4412f92d2b4a423`  
		Last Modified: Tue, 03 Jun 2025 14:03:42 GMT  
		Size: 6.7 MB (6675420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3847e841b0f506b2979520cb832f1496a88ad872d8e318581cdfd88d37e32130`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0106ae4bd1103da267a53ff4c048e62ecef7db2fcb452a6c74ce27945668f30`  
		Last Modified: Wed, 04 Jun 2025 22:07:44 GMT  
		Size: 60.8 MB (60811392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4884da03c76b48c397891bc34311b85ab0cca07eeaf61d6b6b81934e4aaee98`  
		Last Modified: Wed, 04 Jun 2025 22:07:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b35ef54277f35c139de5974a56f262e8582bf12a894585bba1f4eeaaa8e78`  
		Last Modified: Wed, 04 Jun 2025 22:07:40 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:13e8eaf97e06b3b355143f925096df823e5b447cd38b28c06ec822022d6c5b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1231ac25bf1aa055daca3e539da2e9b1d62df97a0f2d57ebbb707f2a60d162`

```dockerfile
```

-	Layers:
	-	`sha256:7f47cbda60f3efe2c6e1d3784f949e1b989b02a85779b81e8ac82f01e6de6cf3`  
		Last Modified: Tue, 03 Jun 2025 05:02:22 GMT  
		Size: 2.2 MB (2204342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c50a2c70c3ed841e71420dc663de62301a6502ce16099cb4ee109e41d3debb3`  
		Last Modified: Tue, 03 Jun 2025 05:02:21 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.1-core`

```console
$ docker pull influxdb@sha256:62276b5841c54271f8f61aa75754dd094ac8889e0e3df13143eb2efa2f3436e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.1-core` - linux; amd64

```console
$ docker pull influxdb@sha256:a7f5988e704d20af512ded712e606675ddaf213929c6d556ed4caf6ba96ae6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100472165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c592d615a3cb3965f7cdc670ca7b02f97b5eb3ada619180fb3cd5521a9ddf5c`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415828e81f66be2d39a188fc960aba46954c3db258660e742ff52cf4f0e6e60a`  
		Last Modified: Tue, 03 Jun 2025 13:35:48 GMT  
		Size: 6.7 MB (6664721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe12f1647cb94de2de19506a5b5f51d03a7359f84d56e4483311b111e817822`  
		Last Modified: Tue, 03 Jun 2025 13:35:47 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2a04f802fa083a74f8c76eae857e4a46d9021994d9c8b81b17e5929a013aea`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 64.1 MB (64087981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409bd07e13d183155e74480126a33360af6dc221228aec11ce46ed5d63e4d085`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af136bf052559a168911c3e729ed692d08d6955e245b953ff8f74ef2d3fc27b`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.1-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:0066ef00ebea27639b9dd8243b8df17185d184e3d34f919bec1c58becb539708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c305bffc31d1939e6029089f0fcf3a4434b505f29362598d4928a585b92a1037`

```dockerfile
```

-	Layers:
	-	`sha256:166b502ace1381b5ebd32cc82d5f50fb91c3ef2dc426578038d59b38a602010c`  
		Last Modified: Tue, 03 Jun 2025 20:03:47 GMT  
		Size: 2.2 MB (2203212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c78f2b9c924919852429713a045188114cae36757f3f7fe3ded6ae8974935f5`  
		Last Modified: Tue, 03 Jun 2025 20:03:47 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.1-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d565003cd08557d0d4885c62452d14520b7a774c4d41dbbf5ef01f90e73d3872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93633161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bfb7469d2a672c94d3864b417bf6b936cd9bfb8bbe6d32561d346aae6bcf31`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482dc2248542ad585f759b15b9f85e27167e3c6c47fc1456d4412f92d2b4a423`  
		Last Modified: Tue, 03 Jun 2025 14:03:42 GMT  
		Size: 6.7 MB (6675420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3847e841b0f506b2979520cb832f1496a88ad872d8e318581cdfd88d37e32130`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2c137e0375813389bf40bbfad44d45608abbe59734689ac532f1a5dbbff8b2`  
		Last Modified: Tue, 03 Jun 2025 14:03:45 GMT  
		Size: 58.1 MB (58101718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae24e95b9f166b6b3ebea08eea7d717d0b5ca7fcf87788dfe0bb16b97363fa2`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d9d3678a4dd2eb245fa14e1668a4c4c9d47b581a58ec40dc4ab45d5c4ada5a`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.1-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:cf543f2c8896e9aaba2f986fb765bd7cc039cf463f2b89099bc76705c99716fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad13c9d3b48bdc61723f1a4d050e2e7131853eca29770774ece2748ab9be4c4f`

```dockerfile
```

-	Layers:
	-	`sha256:5d98149c039782896eafba0c7a3ee345f167cffbdd64264d8e263d7823c5b2a0`  
		Last Modified: Tue, 03 Jun 2025 20:04:11 GMT  
		Size: 2.2 MB (2204294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d15e75bb0d6561c16162f2f9cd0f555ac48770a99d3d2150b35f7f78f029d90`  
		Last Modified: Tue, 03 Jun 2025 20:04:10 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.1-enterprise`

```console
$ docker pull influxdb@sha256:a1944483af83406ee1b2ebdb66f20a704c311571dedc92aeacd46de46895dae2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.1-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6f8ea6dcb55362b0d132b7f69922d834a13d1e7922bcaa8278f412ba0e6f5888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103272989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0b28dfdebea55635b41ec4b137cc3865c987f2b3a8328a0255651a0f5f283c`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c21a2128df4c0b3a1a2a3a7451bc55de7acd7667af0c240008a2de740bc3c21`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 6.7 MB (6664721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcf4966be8170f2e514212b42f0941cc3bc0884771a3c37f15ecdd9ae506cfd`  
		Last Modified: Tue, 03 Jun 2025 13:30:49 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cddcd3193a56e570adb2aae85fd9003a155a3a33efd539baf6472a26926b660`  
		Last Modified: Tue, 03 Jun 2025 13:30:54 GMT  
		Size: 66.9 MB (66888800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf62a59e48bd026bbd4e6e1f76ee899422645120d9f727cf59f86f3c7cba7d`  
		Last Modified: Tue, 03 Jun 2025 13:30:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc677efed44bfe802ade6813bf557d4176a30e17bb52c80f5a55a9d22c92269`  
		Last Modified: Tue, 03 Jun 2025 13:30:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.1-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:58c92711cc95e02318be2536aeccb756ce6e1136ec91c1e9195f8ae0fbbdccc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fc48d31a60cdcceafb5c3e408e1a4ad7ba8c8020ed845f9605aa013ac4852b`

```dockerfile
```

-	Layers:
	-	`sha256:023afb9e0f1e8d258db1fea55efffc04398e06410645b1ad839a17868498398e`  
		Last Modified: Tue, 03 Jun 2025 04:16:32 GMT  
		Size: 2.2 MB (2203260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f205c8b6ef888b50c090dc278e429864438a6d7b54fd3a3a6fbe7282bc257604`  
		Last Modified: Tue, 03 Jun 2025 04:16:32 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.1-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0d46086d38d16ef0418a77551f66e98c4f0bc7def594ade4dfd8e306be7137a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96342836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed042af4efe792b6203b9912a6223ac97a8d63fd8ed3aa8637115fa29a7691c1`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482dc2248542ad585f759b15b9f85e27167e3c6c47fc1456d4412f92d2b4a423`  
		Last Modified: Tue, 03 Jun 2025 14:03:42 GMT  
		Size: 6.7 MB (6675420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3847e841b0f506b2979520cb832f1496a88ad872d8e318581cdfd88d37e32130`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0106ae4bd1103da267a53ff4c048e62ecef7db2fcb452a6c74ce27945668f30`  
		Last Modified: Wed, 04 Jun 2025 22:07:44 GMT  
		Size: 60.8 MB (60811392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4884da03c76b48c397891bc34311b85ab0cca07eeaf61d6b6b81934e4aaee98`  
		Last Modified: Wed, 04 Jun 2025 22:07:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b35ef54277f35c139de5974a56f262e8582bf12a894585bba1f4eeaaa8e78`  
		Last Modified: Wed, 04 Jun 2025 22:07:40 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.1-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:13e8eaf97e06b3b355143f925096df823e5b447cd38b28c06ec822022d6c5b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1231ac25bf1aa055daca3e539da2e9b1d62df97a0f2d57ebbb707f2a60d162`

```dockerfile
```

-	Layers:
	-	`sha256:7f47cbda60f3efe2c6e1d3784f949e1b989b02a85779b81e8ac82f01e6de6cf3`  
		Last Modified: Tue, 03 Jun 2025 05:02:22 GMT  
		Size: 2.2 MB (2204342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c50a2c70c3ed841e71420dc663de62301a6502ce16099cb4ee109e41d3debb3`  
		Last Modified: Tue, 03 Jun 2025 05:02:21 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.1.0-core`

```console
$ docker pull influxdb@sha256:62276b5841c54271f8f61aa75754dd094ac8889e0e3df13143eb2efa2f3436e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.1.0-core` - linux; amd64

```console
$ docker pull influxdb@sha256:a7f5988e704d20af512ded712e606675ddaf213929c6d556ed4caf6ba96ae6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100472165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c592d615a3cb3965f7cdc670ca7b02f97b5eb3ada619180fb3cd5521a9ddf5c`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415828e81f66be2d39a188fc960aba46954c3db258660e742ff52cf4f0e6e60a`  
		Last Modified: Tue, 03 Jun 2025 13:35:48 GMT  
		Size: 6.7 MB (6664721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe12f1647cb94de2de19506a5b5f51d03a7359f84d56e4483311b111e817822`  
		Last Modified: Tue, 03 Jun 2025 13:35:47 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2a04f802fa083a74f8c76eae857e4a46d9021994d9c8b81b17e5929a013aea`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 64.1 MB (64087981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409bd07e13d183155e74480126a33360af6dc221228aec11ce46ed5d63e4d085`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af136bf052559a168911c3e729ed692d08d6955e245b953ff8f74ef2d3fc27b`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.1.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:0066ef00ebea27639b9dd8243b8df17185d184e3d34f919bec1c58becb539708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c305bffc31d1939e6029089f0fcf3a4434b505f29362598d4928a585b92a1037`

```dockerfile
```

-	Layers:
	-	`sha256:166b502ace1381b5ebd32cc82d5f50fb91c3ef2dc426578038d59b38a602010c`  
		Last Modified: Tue, 03 Jun 2025 20:03:47 GMT  
		Size: 2.2 MB (2203212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c78f2b9c924919852429713a045188114cae36757f3f7fe3ded6ae8974935f5`  
		Last Modified: Tue, 03 Jun 2025 20:03:47 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.1.0-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d565003cd08557d0d4885c62452d14520b7a774c4d41dbbf5ef01f90e73d3872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93633161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bfb7469d2a672c94d3864b417bf6b936cd9bfb8bbe6d32561d346aae6bcf31`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482dc2248542ad585f759b15b9f85e27167e3c6c47fc1456d4412f92d2b4a423`  
		Last Modified: Tue, 03 Jun 2025 14:03:42 GMT  
		Size: 6.7 MB (6675420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3847e841b0f506b2979520cb832f1496a88ad872d8e318581cdfd88d37e32130`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2c137e0375813389bf40bbfad44d45608abbe59734689ac532f1a5dbbff8b2`  
		Last Modified: Tue, 03 Jun 2025 14:03:45 GMT  
		Size: 58.1 MB (58101718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae24e95b9f166b6b3ebea08eea7d717d0b5ca7fcf87788dfe0bb16b97363fa2`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d9d3678a4dd2eb245fa14e1668a4c4c9d47b581a58ec40dc4ab45d5c4ada5a`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.1.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:cf543f2c8896e9aaba2f986fb765bd7cc039cf463f2b89099bc76705c99716fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad13c9d3b48bdc61723f1a4d050e2e7131853eca29770774ece2748ab9be4c4f`

```dockerfile
```

-	Layers:
	-	`sha256:5d98149c039782896eafba0c7a3ee345f167cffbdd64264d8e263d7823c5b2a0`  
		Last Modified: Tue, 03 Jun 2025 20:04:11 GMT  
		Size: 2.2 MB (2204294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d15e75bb0d6561c16162f2f9cd0f555ac48770a99d3d2150b35f7f78f029d90`  
		Last Modified: Tue, 03 Jun 2025 20:04:10 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.1.0-enterprise`

```console
$ docker pull influxdb@sha256:a1944483af83406ee1b2ebdb66f20a704c311571dedc92aeacd46de46895dae2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.1.0-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6f8ea6dcb55362b0d132b7f69922d834a13d1e7922bcaa8278f412ba0e6f5888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103272989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0b28dfdebea55635b41ec4b137cc3865c987f2b3a8328a0255651a0f5f283c`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c21a2128df4c0b3a1a2a3a7451bc55de7acd7667af0c240008a2de740bc3c21`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 6.7 MB (6664721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcf4966be8170f2e514212b42f0941cc3bc0884771a3c37f15ecdd9ae506cfd`  
		Last Modified: Tue, 03 Jun 2025 13:30:49 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cddcd3193a56e570adb2aae85fd9003a155a3a33efd539baf6472a26926b660`  
		Last Modified: Tue, 03 Jun 2025 13:30:54 GMT  
		Size: 66.9 MB (66888800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf62a59e48bd026bbd4e6e1f76ee899422645120d9f727cf59f86f3c7cba7d`  
		Last Modified: Tue, 03 Jun 2025 13:30:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc677efed44bfe802ade6813bf557d4176a30e17bb52c80f5a55a9d22c92269`  
		Last Modified: Tue, 03 Jun 2025 13:30:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.1.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:58c92711cc95e02318be2536aeccb756ce6e1136ec91c1e9195f8ae0fbbdccc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fc48d31a60cdcceafb5c3e408e1a4ad7ba8c8020ed845f9605aa013ac4852b`

```dockerfile
```

-	Layers:
	-	`sha256:023afb9e0f1e8d258db1fea55efffc04398e06410645b1ad839a17868498398e`  
		Last Modified: Tue, 03 Jun 2025 04:16:32 GMT  
		Size: 2.2 MB (2203260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f205c8b6ef888b50c090dc278e429864438a6d7b54fd3a3a6fbe7282bc257604`  
		Last Modified: Tue, 03 Jun 2025 04:16:32 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.1.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0d46086d38d16ef0418a77551f66e98c4f0bc7def594ade4dfd8e306be7137a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96342836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed042af4efe792b6203b9912a6223ac97a8d63fd8ed3aa8637115fa29a7691c1`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482dc2248542ad585f759b15b9f85e27167e3c6c47fc1456d4412f92d2b4a423`  
		Last Modified: Tue, 03 Jun 2025 14:03:42 GMT  
		Size: 6.7 MB (6675420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3847e841b0f506b2979520cb832f1496a88ad872d8e318581cdfd88d37e32130`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0106ae4bd1103da267a53ff4c048e62ecef7db2fcb452a6c74ce27945668f30`  
		Last Modified: Wed, 04 Jun 2025 22:07:44 GMT  
		Size: 60.8 MB (60811392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4884da03c76b48c397891bc34311b85ab0cca07eeaf61d6b6b81934e4aaee98`  
		Last Modified: Wed, 04 Jun 2025 22:07:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b35ef54277f35c139de5974a56f262e8582bf12a894585bba1f4eeaaa8e78`  
		Last Modified: Wed, 04 Jun 2025 22:07:40 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.1.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:13e8eaf97e06b3b355143f925096df823e5b447cd38b28c06ec822022d6c5b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1231ac25bf1aa055daca3e539da2e9b1d62df97a0f2d57ebbb707f2a60d162`

```dockerfile
```

-	Layers:
	-	`sha256:7f47cbda60f3efe2c6e1d3784f949e1b989b02a85779b81e8ac82f01e6de6cf3`  
		Last Modified: Tue, 03 Jun 2025 05:02:22 GMT  
		Size: 2.2 MB (2204342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c50a2c70c3ed841e71420dc663de62301a6502ce16099cb4ee109e41d3debb3`  
		Last Modified: Tue, 03 Jun 2025 05:02:21 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b4da6257d4dab81f7ea9b217e8990fa02b532b487dc09f66cfe66b7a5ab1b7`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f227616a4b65630020272b1a4736c45d2072fea1f6ae56d8987f001bff1868e5`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 9.7 MB (9668254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28153e71486f54b7e2d6898878271446058952c9919aaad4310fd5662e14073`  
		Last Modified: Tue, 03 Jun 2025 13:35:12 GMT  
		Size: 5.8 MB (5820951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17da966601b69ee27cf7e07f71e8d3a293465f510f662a95761c204c476039`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f351545292c8d4b32b561f37f2761b8143e35ea7b2aed6ada764d91675953e2`  
		Last Modified: Tue, 03 Jun 2025 13:35:16 GMT  
		Size: 50.1 MB (50115457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec39c678e278ff055d4d22e8402129df928caa4a2647ff3024e97721f0f5943`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 23.5 MB (23546414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428d400809cb7ad31d35a7f2d948c8121b3f7499c617f94eb95080f6705d2c6`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195b609b670962adf4a4fd55112b8f3ee09ab9b864b63db78893c7e7b6de06aa`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213bcca749f51ef7f5ebe65ef3ee91941b8ead606c2179e2247bba98e5d1ba1`  
		Last Modified: Tue, 03 Jun 2025 13:35:14 GMT  
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
		Last Modified: Wed, 04 Jun 2025 00:38:08 GMT  
		Size: 918.5 KB (918468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15b588c6b6124a1aa918ae48f879aa8e721ecd2db834e3c78af76a20738c283`  
		Last Modified: Wed, 04 Jun 2025 00:38:22 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c8ed1b411bf87e31d51dcd5e11ad29b842c6ac23d29867f58c9b6657217f9`  
		Last Modified: Thu, 08 May 2025 17:16:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7581744a5f8b851a37b006b9f70c0dfc1aabfbbf6e54e0d468d11332b9a89155`  
		Last Modified: Tue, 03 Jun 2025 13:33:06 GMT  
		Size: 9.8 MB (9790275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8e2420533fb94a98c3c0cea702d65af3aac200564d71bf02039933d45752c4`  
		Last Modified: Tue, 03 Jun 2025 13:32:59 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d98ff612225a614c58f5f650b55a20d2a5f607933c56ec0b343dc54d39316`  
		Last Modified: Tue, 03 Jun 2025 13:32:59 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9943be5d4ecac40794357058ec1ead2ffe57b93ad82f1c046f9490950fb8be`  
		Last Modified: Tue, 03 Jun 2025 13:33:07 GMT  
		Size: 48.0 MB (48016208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592941019971dc33dba5c666bebc57139662a00acd86e6dc6e85310542b62a90`  
		Last Modified: Tue, 03 Jun 2025 13:33:08 GMT  
		Size: 22.2 MB (22197933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a652dc6c421b2c1298eb71f3a1a77ad5317359d42f97d2ba7e0256166f7908`  
		Last Modified: Tue, 03 Jun 2025 13:33:10 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c5c55779859032454928168c0eaf5620289e22d09443a4c303e920fbc0f25e`  
		Last Modified: Tue, 03 Jun 2025 13:33:10 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c5a87a5ee69568a4bb3e3c7fbcb83b0bd9250e68ef8618525ab0df87a7c0`  
		Last Modified: Tue, 03 Jun 2025 13:33:11 GMT  
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
		Last Modified: Wed, 04 Jun 2025 02:56:34 GMT  
		Size: 917.7 KB (917719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f4f5e2584d7feb4ec7fc289bad890abb4f9f813f7c20ca231fb580b0db01d6d`  
		Last Modified: Wed, 04 Jun 2025 02:56:42 GMT  
		Size: 31.2 KB (31241 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:core`

```console
$ docker pull influxdb@sha256:62276b5841c54271f8f61aa75754dd094ac8889e0e3df13143eb2efa2f3436e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:a7f5988e704d20af512ded712e606675ddaf213929c6d556ed4caf6ba96ae6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100472165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c592d615a3cb3965f7cdc670ca7b02f97b5eb3ada619180fb3cd5521a9ddf5c`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415828e81f66be2d39a188fc960aba46954c3db258660e742ff52cf4f0e6e60a`  
		Last Modified: Tue, 03 Jun 2025 13:35:48 GMT  
		Size: 6.7 MB (6664721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe12f1647cb94de2de19506a5b5f51d03a7359f84d56e4483311b111e817822`  
		Last Modified: Tue, 03 Jun 2025 13:35:47 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2a04f802fa083a74f8c76eae857e4a46d9021994d9c8b81b17e5929a013aea`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 64.1 MB (64087981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409bd07e13d183155e74480126a33360af6dc221228aec11ce46ed5d63e4d085`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af136bf052559a168911c3e729ed692d08d6955e245b953ff8f74ef2d3fc27b`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:0066ef00ebea27639b9dd8243b8df17185d184e3d34f919bec1c58becb539708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c305bffc31d1939e6029089f0fcf3a4434b505f29362598d4928a585b92a1037`

```dockerfile
```

-	Layers:
	-	`sha256:166b502ace1381b5ebd32cc82d5f50fb91c3ef2dc426578038d59b38a602010c`  
		Last Modified: Tue, 03 Jun 2025 20:03:47 GMT  
		Size: 2.2 MB (2203212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c78f2b9c924919852429713a045188114cae36757f3f7fe3ded6ae8974935f5`  
		Last Modified: Tue, 03 Jun 2025 20:03:47 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d565003cd08557d0d4885c62452d14520b7a774c4d41dbbf5ef01f90e73d3872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93633161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bfb7469d2a672c94d3864b417bf6b936cd9bfb8bbe6d32561d346aae6bcf31`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482dc2248542ad585f759b15b9f85e27167e3c6c47fc1456d4412f92d2b4a423`  
		Last Modified: Tue, 03 Jun 2025 14:03:42 GMT  
		Size: 6.7 MB (6675420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3847e841b0f506b2979520cb832f1496a88ad872d8e318581cdfd88d37e32130`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2c137e0375813389bf40bbfad44d45608abbe59734689ac532f1a5dbbff8b2`  
		Last Modified: Tue, 03 Jun 2025 14:03:45 GMT  
		Size: 58.1 MB (58101718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae24e95b9f166b6b3ebea08eea7d717d0b5ca7fcf87788dfe0bb16b97363fa2`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d9d3678a4dd2eb245fa14e1668a4c4c9d47b581a58ec40dc4ab45d5c4ada5a`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:cf543f2c8896e9aaba2f986fb765bd7cc039cf463f2b89099bc76705c99716fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad13c9d3b48bdc61723f1a4d050e2e7131853eca29770774ece2748ab9be4c4f`

```dockerfile
```

-	Layers:
	-	`sha256:5d98149c039782896eafba0c7a3ee345f167cffbdd64264d8e263d7823c5b2a0`  
		Last Modified: Tue, 03 Jun 2025 20:04:11 GMT  
		Size: 2.2 MB (2204294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d15e75bb0d6561c16162f2f9cd0f555ac48770a99d3d2150b35f7f78f029d90`  
		Last Modified: Tue, 03 Jun 2025 20:04:10 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:a1944483af83406ee1b2ebdb66f20a704c311571dedc92aeacd46de46895dae2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6f8ea6dcb55362b0d132b7f69922d834a13d1e7922bcaa8278f412ba0e6f5888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103272989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0b28dfdebea55635b41ec4b137cc3865c987f2b3a8328a0255651a0f5f283c`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c21a2128df4c0b3a1a2a3a7451bc55de7acd7667af0c240008a2de740bc3c21`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 6.7 MB (6664721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcf4966be8170f2e514212b42f0941cc3bc0884771a3c37f15ecdd9ae506cfd`  
		Last Modified: Tue, 03 Jun 2025 13:30:49 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cddcd3193a56e570adb2aae85fd9003a155a3a33efd539baf6472a26926b660`  
		Last Modified: Tue, 03 Jun 2025 13:30:54 GMT  
		Size: 66.9 MB (66888800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf62a59e48bd026bbd4e6e1f76ee899422645120d9f727cf59f86f3c7cba7d`  
		Last Modified: Tue, 03 Jun 2025 13:30:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc677efed44bfe802ade6813bf557d4176a30e17bb52c80f5a55a9d22c92269`  
		Last Modified: Tue, 03 Jun 2025 13:30:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:58c92711cc95e02318be2536aeccb756ce6e1136ec91c1e9195f8ae0fbbdccc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fc48d31a60cdcceafb5c3e408e1a4ad7ba8c8020ed845f9605aa013ac4852b`

```dockerfile
```

-	Layers:
	-	`sha256:023afb9e0f1e8d258db1fea55efffc04398e06410645b1ad839a17868498398e`  
		Last Modified: Tue, 03 Jun 2025 04:16:32 GMT  
		Size: 2.2 MB (2203260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f205c8b6ef888b50c090dc278e429864438a6d7b54fd3a3a6fbe7282bc257604`  
		Last Modified: Tue, 03 Jun 2025 04:16:32 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0d46086d38d16ef0418a77551f66e98c4f0bc7def594ade4dfd8e306be7137a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96342836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed042af4efe792b6203b9912a6223ac97a8d63fd8ed3aa8637115fa29a7691c1`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482dc2248542ad585f759b15b9f85e27167e3c6c47fc1456d4412f92d2b4a423`  
		Last Modified: Tue, 03 Jun 2025 14:03:42 GMT  
		Size: 6.7 MB (6675420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3847e841b0f506b2979520cb832f1496a88ad872d8e318581cdfd88d37e32130`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0106ae4bd1103da267a53ff4c048e62ecef7db2fcb452a6c74ce27945668f30`  
		Last Modified: Wed, 04 Jun 2025 22:07:44 GMT  
		Size: 60.8 MB (60811392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4884da03c76b48c397891bc34311b85ab0cca07eeaf61d6b6b81934e4aaee98`  
		Last Modified: Wed, 04 Jun 2025 22:07:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b35ef54277f35c139de5974a56f262e8582bf12a894585bba1f4eeaaa8e78`  
		Last Modified: Wed, 04 Jun 2025 22:07:40 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:13e8eaf97e06b3b355143f925096df823e5b447cd38b28c06ec822022d6c5b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1231ac25bf1aa055daca3e539da2e9b1d62df97a0f2d57ebbb707f2a60d162`

```dockerfile
```

-	Layers:
	-	`sha256:7f47cbda60f3efe2c6e1d3784f949e1b989b02a85779b81e8ac82f01e6de6cf3`  
		Last Modified: Tue, 03 Jun 2025 05:02:22 GMT  
		Size: 2.2 MB (2204342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c50a2c70c3ed841e71420dc663de62301a6502ce16099cb4ee109e41d3debb3`  
		Last Modified: Tue, 03 Jun 2025 05:02:21 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:d4d96a93b3d238fa2577916e501304cc32a206efd9f1eb163f18e9d21b3983a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:549a15b5f66acff43b670a6d2182829dae27abe6456ff80ff8af9b958750fcc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168642983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff72781800ab8302b2b10d8eea3ff3a54bf61c1fa388fa7a1c4cdcac1aa8f828`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f36ae94f40a7aa5fd6bca9f3c08cf4719e80d591037c7a4b94d1539744a8fb`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 9.8 MB (9791034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe37dd6f8888efc5da91f2f29534eed01e10e2cb86c784254b43db36562dc8c`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6efd9c01e056a7294fa312b86336fe6f439b89bc5129eee70623703ccf7aa8`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a8e265719c2793ca28cadc5376391c897c89f6726e101bad2a7c247f364ffb`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394da5cd13ce2b03effce819aa590edf6649db4afc44de6c21df01bddf11bf94`  
		Last Modified: Tue, 03 Jun 2025 13:30:56 GMT  
		Size: 100.2 MB (100242960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d10ee91c71ce63c26fa20756e8e9073885a91e3759cfebceae9a440a7f4706`  
		Last Modified: Tue, 03 Jun 2025 13:33:07 GMT  
		Size: 23.5 MB (23546404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d829ed22f9224c3579e98603469332a0cc2aaa54e20430745ff2ac440dc1fc8`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead9edcf8ee593eeb009b7e83c7049aa141da36206ea7a4e016b9f9c17244e6b`  
		Last Modified: Tue, 03 Jun 2025 13:30:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc84b868a5d32847815f5cede5ad639bd1f4a8e9468c81ac4d8e8d82e610f3d1`  
		Last Modified: Tue, 03 Jun 2025 13:30:46 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:279a20561406f515dbce4a46eef0013bf0d169fee238b91c177703aeb5ee4f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2903032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d571e2519980a093a8966be30679f80d3c3907038a74d7b7624d81b2e2d13e4b`

```dockerfile
```

-	Layers:
	-	`sha256:8c2886d35940c270ee63e635039d82c1202bdc2159aecf8a884b355111d7a7b5`  
		Last Modified: Wed, 04 Jun 2025 02:29:58 GMT  
		Size: 2.9 MB (2869214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206a20f20680f68235164eecb4834095f5cfe784f61caf8e675da45390e333cb`  
		Last Modified: Wed, 04 Jun 2025 02:30:16 GMT  
		Size: 33.8 KB (33818 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:86bb738da2c4ece12e0cd4753d41a1d164eaedf778c960fff7ae9acef9961b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162300102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a961c9d0be3a43097e88ce7a44a554a8286cb7200e4ed38c72d18eed7f0120a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fb2485b7c4399692ff0f858e85a493f7520a8d7a7c0fea3fdb10af035ca4db`  
		Last Modified: Tue, 03 Jun 2025 13:32:48 GMT  
		Size: 9.6 MB (9588655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a652ae87fbc6c53da5a0254038a21966076bf080aca8e2d28ba72b5d420d5f9`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 5.5 MB (5463794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f002cc60651d1b940830c2474392559655131840a6ee05d3fa3ad46043e8d717`  
		Last Modified: Tue, 03 Jun 2025 13:32:49 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2659eb1f1bde104f3c076174116ef9f4048e77b37a35cb0084f845af628f08`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110b9d474b0a3bc25d10ea3255f2a23ffce66575ff780d6882a1a7123a73c313`  
		Last Modified: Tue, 03 Jun 2025 13:33:06 GMT  
		Size: 96.0 MB (96038373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd6afc77b240651bd89398eb9b69f97346e697cc5cb0b9f4ff0edbed4f17fca`  
		Last Modified: Tue, 03 Jun 2025 13:32:53 GMT  
		Size: 22.2 MB (22197938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aac4036678859e629ddc5174b7ee3f6f51cd04b7985d07ac05b27028ed0816`  
		Last Modified: Tue, 03 Jun 2025 13:32:51 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc68c4f14fa754f1b66375f3dcd348c039bdb940b5430a4b9c3eaab2018d16c`  
		Last Modified: Tue, 03 Jun 2025 13:32:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940c0915463d99c5f92547a5c658ec36fe7e548d303c2319b315bb21e85d671`  
		Last Modified: Tue, 03 Jun 2025 13:32:53 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:123be7ccf66e93ac0b6f0960dafa5a2f75c89c5d8bffd23e4124b8918be6d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2902443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e621672e616043de6a8903502ee7f1a98c758bdba5fe9fbfc5c68be6e40653`

```dockerfile
```

-	Layers:
	-	`sha256:8dde95519976874c08bc5ae53076ab1ce50b41c1f5a3d97f4bab939a4f6d24b2`  
		Last Modified: Wed, 04 Jun 2025 02:53:09 GMT  
		Size: 2.9 MB (2868442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca8ec741f51106258a1e51e9c3c07486d7942d4641b3f09816b959c83077987`  
		Last Modified: Wed, 04 Jun 2025 02:53:21 GMT  
		Size: 34.0 KB (34001 bytes)  
		MIME: application/vnd.in-toto+json
