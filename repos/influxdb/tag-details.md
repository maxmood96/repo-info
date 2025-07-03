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
-	[`influxdb:3.2-core`](#influxdb32-core)
-	[`influxdb:3.2-enterprise`](#influxdb32-enterprise)
-	[`influxdb:3.2.1-core`](#influxdb321-core)
-	[`influxdb:3.2.1-enterprise`](#influxdb321-enterprise)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:core`](#influxdbcore)
-	[`influxdb:enterprise`](#influxdbenterprise)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:e99bb0ae8386fe259cf282df399d67838c0d21258f124c18e7711cf0de499117
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:3ac551570cc98fc16a79ed43106134963af7de7c307750e75c4f4c71cc0ac629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108963313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663fd3ef9a3ed2211bca0d4dfd36d499c07b644bc78c5851c9d30554693e293`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Tue, 24 Jun 2025 22:21:26 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66f8bd3d13f53c85a80646350ed31fd5f9b2e89d3f4ca0c29229da7ac5d120d`  
		Last Modified: Tue, 01 Jul 2025 04:29:51 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7a1cccc3ad4e9719dded4c66ee0b4542f90caf62ee023126568b289b46fa58`  
		Last Modified: Tue, 01 Jul 2025 13:47:49 GMT  
		Size: 39.4 MB (39439598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6852ec91750a420ecc94dfc477755e1ca3eb6bc119a63821fd6be2e7128ad2a0`  
		Last Modified: Tue, 01 Jul 2025 04:30:18 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2702c8906114fc11200fc17a9ce1e40bafcfefde8ce8970dc2b9beb4d49eb7`  
		Last Modified: Tue, 01 Jul 2025 04:30:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d399295ea575b278b52007c3fe1ff14d21523c1fd1d79359ec68b85a32bc9f80`  
		Last Modified: Tue, 01 Jul 2025 13:47:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:50a5e201144486724f5adb4485cab799ef5abbb0300bfce9c557a69669d62f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4799034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7233bcc4a42ede02eebd063880d94200e017460a1ab7a4bac4e4fc3cff7ca3bd`

```dockerfile
```

-	Layers:
	-	`sha256:4a2d60e9aa5c34929bfef02bdd1ebdfe3b7810949f04ef0f8548721ff82772dc`  
		Last Modified: Tue, 01 Jul 2025 05:20:19 GMT  
		Size: 4.8 MB (4784326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17714fb5876c6c78c2ebf1a231d25090688f8e1ab5e63813b4772a065b6963d`  
		Last Modified: Tue, 01 Jul 2025 05:20:19 GMT  
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
$ docker pull influxdb@sha256:4c09ca519d39121bf6de3e8284dbd962636444cfa064d882dfb886c94775d158
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:95276eeb061bf6677729ff4050de7fd6b7416485f5fbe177afd0727417434890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88162543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b125367c680e5fe3b79a4634590227832fab9a7661ca8d99ca0a0e2d5c3cf40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Tue, 24 Jun 2025 22:21:26 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08532df0d960b0d2d4557c70589596aac09036d72b0ba71d2ea106d5e22bc1a5`  
		Last Modified: Tue, 01 Jul 2025 03:22:23 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762ee3cdd37fba5504449e2314f418ff25d0aa723072342d9d024a747d248ad2`  
		Last Modified: Tue, 01 Jul 2025 03:22:25 GMT  
		Size: 18.6 MB (18640046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c35384cd7389a47ef3f06f4bbdf915c9677a341e175a591f56a4a0ded736c42`  
		Last Modified: Tue, 01 Jul 2025 03:22:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f42a28178a3ab88d52707aa644a691bc9ec6d7e8ad444f8ad40473ff0d58e0c`  
		Last Modified: Tue, 01 Jul 2025 03:22:24 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:929eac7fe4da8a9fa7b9533f7fe42e9d7ee0252df7f55a4714f8fc9ea859f27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92df10cc7fb26b9f863f7c140f5f07d31d095fb58aef6ea54a079d49c4fb9b6a`

```dockerfile
```

-	Layers:
	-	`sha256:009bee9a1dad906cbb0ed209e339f5113e79b8bf9a255c532455484897c578a3`  
		Last Modified: Tue, 01 Jul 2025 05:20:24 GMT  
		Size: 4.7 MB (4708306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27a64e66cdfca24c5b545cdf8b5f951a99f34416f15d1d735b176f4439288836`  
		Last Modified: Tue, 01 Jul 2025 05:20:25 GMT  
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
$ docker pull influxdb@sha256:e99bb0ae8386fe259cf282df399d67838c0d21258f124c18e7711cf0de499117
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:3ac551570cc98fc16a79ed43106134963af7de7c307750e75c4f4c71cc0ac629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108963313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663fd3ef9a3ed2211bca0d4dfd36d499c07b644bc78c5851c9d30554693e293`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Tue, 24 Jun 2025 22:21:26 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66f8bd3d13f53c85a80646350ed31fd5f9b2e89d3f4ca0c29229da7ac5d120d`  
		Last Modified: Tue, 01 Jul 2025 04:29:51 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7a1cccc3ad4e9719dded4c66ee0b4542f90caf62ee023126568b289b46fa58`  
		Last Modified: Tue, 01 Jul 2025 13:47:49 GMT  
		Size: 39.4 MB (39439598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6852ec91750a420ecc94dfc477755e1ca3eb6bc119a63821fd6be2e7128ad2a0`  
		Last Modified: Tue, 01 Jul 2025 04:30:18 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2702c8906114fc11200fc17a9ce1e40bafcfefde8ce8970dc2b9beb4d49eb7`  
		Last Modified: Tue, 01 Jul 2025 04:30:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d399295ea575b278b52007c3fe1ff14d21523c1fd1d79359ec68b85a32bc9f80`  
		Last Modified: Tue, 01 Jul 2025 13:47:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:50a5e201144486724f5adb4485cab799ef5abbb0300bfce9c557a69669d62f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4799034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7233bcc4a42ede02eebd063880d94200e017460a1ab7a4bac4e4fc3cff7ca3bd`

```dockerfile
```

-	Layers:
	-	`sha256:4a2d60e9aa5c34929bfef02bdd1ebdfe3b7810949f04ef0f8548721ff82772dc`  
		Last Modified: Tue, 01 Jul 2025 05:20:19 GMT  
		Size: 4.8 MB (4784326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17714fb5876c6c78c2ebf1a231d25090688f8e1ab5e63813b4772a065b6963d`  
		Last Modified: Tue, 01 Jul 2025 05:20:19 GMT  
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
$ docker pull influxdb@sha256:4c09ca519d39121bf6de3e8284dbd962636444cfa064d882dfb886c94775d158
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:95276eeb061bf6677729ff4050de7fd6b7416485f5fbe177afd0727417434890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88162543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b125367c680e5fe3b79a4634590227832fab9a7661ca8d99ca0a0e2d5c3cf40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Tue, 24 Jun 2025 22:21:26 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08532df0d960b0d2d4557c70589596aac09036d72b0ba71d2ea106d5e22bc1a5`  
		Last Modified: Tue, 01 Jul 2025 03:22:23 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762ee3cdd37fba5504449e2314f418ff25d0aa723072342d9d024a747d248ad2`  
		Last Modified: Tue, 01 Jul 2025 03:22:25 GMT  
		Size: 18.6 MB (18640046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c35384cd7389a47ef3f06f4bbdf915c9677a341e175a591f56a4a0ded736c42`  
		Last Modified: Tue, 01 Jul 2025 03:22:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f42a28178a3ab88d52707aa644a691bc9ec6d7e8ad444f8ad40473ff0d58e0c`  
		Last Modified: Tue, 01 Jul 2025 03:22:24 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:929eac7fe4da8a9fa7b9533f7fe42e9d7ee0252df7f55a4714f8fc9ea859f27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92df10cc7fb26b9f863f7c140f5f07d31d095fb58aef6ea54a079d49c4fb9b6a`

```dockerfile
```

-	Layers:
	-	`sha256:009bee9a1dad906cbb0ed209e339f5113e79b8bf9a255c532455484897c578a3`  
		Last Modified: Tue, 01 Jul 2025 05:20:24 GMT  
		Size: 4.7 MB (4708306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27a64e66cdfca24c5b545cdf8b5f951a99f34416f15d1d735b176f4439288836`  
		Last Modified: Tue, 01 Jul 2025 05:20:25 GMT  
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
$ docker pull influxdb@sha256:75b6f00cf1b143e519ab091c1de34639014f6473c15944d3c18a4efe20e52315
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:16f54469b516faca67f9fb80ac0f75c3e0be65f98d9e08c50cf33bef5ba14605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116169336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68bb880f64bcc43e755df42e5a02f5618e1dea3fd703344676c87dc165eb9d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 24 Jun 2025 22:21:26 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20e8eace4c0c8b7be4bee65c78bfd65c6fd0745f1f6db933e9380c08076539b`  
		Last Modified: Tue, 01 Jul 2025 03:22:16 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475e67fd9a8af71db78d4e2d9e284ec0af21bb6b5d287dd294ddabbc3d9f4fc9`  
		Last Modified: Tue, 01 Jul 2025 03:22:20 GMT  
		Size: 43.7 MB (43651446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f708d204947c9cfe29e39c24b24432ab955549b8beb9419ffe4a7bcb0266d`  
		Last Modified: Tue, 01 Jul 2025 03:22:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321d3aade0665e789b3f545e16228e8a01fe348c90bf4d882c6bffad234deaaa`  
		Last Modified: Tue, 01 Jul 2025 03:22:17 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c2454496d2954f0bbc2b1d32a3ef527be051d074de12f40351f568b27b0fa6`  
		Last Modified: Tue, 01 Jul 2025 03:22:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:9244ab686e70257a208d88d099e630862ee2e1d6df2b81fcce406629e7c61499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ece1665ae800306182b9a27ab4e212e92266e5276fb59af79856a4d9efbbdb`

```dockerfile
```

-	Layers:
	-	`sha256:a4429c9bb285d9fe8cf4f9491d451c2d557a835cf5cfa81123f0f6a5d7bb3ae5`  
		Last Modified: Tue, 01 Jul 2025 05:20:30 GMT  
		Size: 5.1 MB (5071847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d00d765840157eb2f0ed1792d9dc9dcbcedd17959071d709e75dc586752c7e6f`  
		Last Modified: Tue, 01 Jul 2025 05:20:31 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b750d0b58aa3663604acf39fafb7ced92eb4638dc0d93bbb7d69cb4ee76b49d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113018941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd80a184cd2aa5fb07e4fbbc2698a880475b2d814457ad266bfd2bdc9ef0162`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 24 Jun 2025 22:21:26 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed81b1c6d99b5ff7133d00f4150bec2c8cd37906b12e4ee37d2cd58bbb353555`  
		Last Modified: Tue, 01 Jul 2025 14:23:05 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cb140ed69e99ddfc606c0305e38ad3b54218eac4a2b551519410da455a7a97`  
		Last Modified: Tue, 01 Jul 2025 14:23:10 GMT  
		Size: 41.1 MB (41119237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d426ed41f5c5ab2072564efe48130a02002d4efd744c7e7962f6c2b4bd0235`  
		Last Modified: Tue, 01 Jul 2025 14:23:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5794d976e6e80e5cb5779c66485ec49872db5a3d44c71caa4b289857ea6558e`  
		Last Modified: Tue, 01 Jul 2025 14:23:06 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29335d2acc0ce04156fa5363c07ef1dbe2dc3e9c2b0ae74cb7fe3fbb2bf18e09`  
		Last Modified: Tue, 01 Jul 2025 14:23:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:9a174f3ec071331cb29afcd2dbc32aa795acbf58266e896a4c671f771560c3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2430d9582934df1e2a872f6ab7d1b2146730721039860790b8bf31c88c7c11a`

```dockerfile
```

-	Layers:
	-	`sha256:bb7a3888ff64f4de991508fbb96cc6b426f0a7ce7cd7585e28f53659a951b6a2`  
		Last Modified: Tue, 01 Jul 2025 17:20:25 GMT  
		Size: 5.1 MB (5071312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a1c81d10a757b25a65d253908c61e845a7fc6ff91b730de56a2676012ed02f5`  
		Last Modified: Tue, 01 Jul 2025 17:20:26 GMT  
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
$ docker pull influxdb@sha256:c226591eb403bd3f3e4b0f37767560d47da9ecb70b8e59a7e53435f4712c5629
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:401ae6cb95dfbc571a2d7c2beabfb992d70eea16c8d06e791a5f60a0b4b6c887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111697817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c059fc4c9a12f435c9f1de74e2eaa292bc4b36ce2c57a715b01869dab22780f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Tue, 24 Jun 2025 22:21:26 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93633f3ed459fd47f2739c524b6fc6bc9fb3d14c3f00a476e7386347b371b32f`  
		Last Modified: Tue, 01 Jul 2025 04:29:51 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0ca01351d272a2b60e9d01390332632a1604d2ad1e3ae8833b9b45ff2b8cc5`  
		Last Modified: Tue, 01 Jul 2025 13:47:48 GMT  
		Size: 39.2 MB (39179283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fed012671239fb217957b0fdfa7dc1819c24e336c95617dc7936445dd02326e`  
		Last Modified: Tue, 01 Jul 2025 04:29:54 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0a817f28139f50b48fbc8138c3f147fe2e16e48da6d6f35b42ceabb3ae79f`  
		Last Modified: Tue, 01 Jul 2025 13:47:50 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b713e01c96351ddde861e8c5329cafbdc2ccb84dd94e1b2fcdc57d70b2a41b0e`  
		Last Modified: Tue, 01 Jul 2025 04:30:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:b67687fc2e926c6bb0e88d95a99b090b91a59a05d502e5fbfae1bdd60d317fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf918f70158f0e4b30301b6cd9e013661d52ae61c5a5a2ef79cd2daf9f53c65`

```dockerfile
```

-	Layers:
	-	`sha256:c22431ed89042ba685c965c048e146c1cdae85cf0c8bf60eff1d87457a66bf1e`  
		Last Modified: Tue, 01 Jul 2025 05:20:35 GMT  
		Size: 4.7 MB (4661024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7738ef4d4fda343df13092fa81f1ebb68e4505808b8fe2e5d4682f82471bc6`  
		Last Modified: Tue, 01 Jul 2025 05:20:36 GMT  
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
$ docker pull influxdb@sha256:5243e1d41041fc58bfc853e6c796941ac42827d2b142b049e33b34ed957c69d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c538c7e8446699a1dd7d66aed8cbb77594c4f01669397aeed8b67de2a445c6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90853893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17bc62dfc6a4aae65aec71c9969280592fb6c131f9e9bf70de3c2a77b388e834`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Tue, 24 Jun 2025 22:21:26 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66f8bd3d13f53c85a80646350ed31fd5f9b2e89d3f4ca0c29229da7ac5d120d`  
		Last Modified: Tue, 01 Jul 2025 04:29:51 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c899dc1b5f3c11ca37140491bfa999211d45a89e4314324b94c457ec4b429568`  
		Last Modified: Tue, 01 Jul 2025 13:15:21 GMT  
		Size: 18.3 MB (18336571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b329dc4701b82f7839c027e1034e3df087cf3eba771b003bc114c5279405bd14`  
		Last Modified: Tue, 01 Jul 2025 04:29:54 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253f2d56b1ec3e6967d6c9ef45fcbd0a5192737351b92ae9b4cb21e2def29ff1`  
		Last Modified: Tue, 01 Jul 2025 04:30:00 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:8b7f743b912c684cd868c00b63b22704fc0edb12110a6c9dec5b899d3dc733fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4599062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242bab184e0d995b7ca508ba918d14f1cbd828967204d4e4213ae35642ad487a`

```dockerfile
```

-	Layers:
	-	`sha256:78ce6c9448fb750452d348d4201f991be0c80e53e2331755c90c2a2465bc6b02`  
		Last Modified: Tue, 01 Jul 2025 05:20:41 GMT  
		Size: 4.6 MB (4585995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe6e0dc863d239c88f6ac0c0c2d4464e26e899410ad167d15d8aeadab868c995`  
		Last Modified: Tue, 01 Jul 2025 05:20:42 GMT  
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
$ docker pull influxdb@sha256:75b6f00cf1b143e519ab091c1de34639014f6473c15944d3c18a4efe20e52315
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:16f54469b516faca67f9fb80ac0f75c3e0be65f98d9e08c50cf33bef5ba14605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116169336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68bb880f64bcc43e755df42e5a02f5618e1dea3fd703344676c87dc165eb9d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 24 Jun 2025 22:21:26 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20e8eace4c0c8b7be4bee65c78bfd65c6fd0745f1f6db933e9380c08076539b`  
		Last Modified: Tue, 01 Jul 2025 03:22:16 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475e67fd9a8af71db78d4e2d9e284ec0af21bb6b5d287dd294ddabbc3d9f4fc9`  
		Last Modified: Tue, 01 Jul 2025 03:22:20 GMT  
		Size: 43.7 MB (43651446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f708d204947c9cfe29e39c24b24432ab955549b8beb9419ffe4a7bcb0266d`  
		Last Modified: Tue, 01 Jul 2025 03:22:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321d3aade0665e789b3f545e16228e8a01fe348c90bf4d882c6bffad234deaaa`  
		Last Modified: Tue, 01 Jul 2025 03:22:17 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c2454496d2954f0bbc2b1d32a3ef527be051d074de12f40351f568b27b0fa6`  
		Last Modified: Tue, 01 Jul 2025 03:22:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:9244ab686e70257a208d88d099e630862ee2e1d6df2b81fcce406629e7c61499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ece1665ae800306182b9a27ab4e212e92266e5276fb59af79856a4d9efbbdb`

```dockerfile
```

-	Layers:
	-	`sha256:a4429c9bb285d9fe8cf4f9491d451c2d557a835cf5cfa81123f0f6a5d7bb3ae5`  
		Last Modified: Tue, 01 Jul 2025 05:20:30 GMT  
		Size: 5.1 MB (5071847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d00d765840157eb2f0ed1792d9dc9dcbcedd17959071d709e75dc586752c7e6f`  
		Last Modified: Tue, 01 Jul 2025 05:20:31 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b750d0b58aa3663604acf39fafb7ced92eb4638dc0d93bbb7d69cb4ee76b49d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113018941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd80a184cd2aa5fb07e4fbbc2698a880475b2d814457ad266bfd2bdc9ef0162`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 24 Jun 2025 22:21:26 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed81b1c6d99b5ff7133d00f4150bec2c8cd37906b12e4ee37d2cd58bbb353555`  
		Last Modified: Tue, 01 Jul 2025 14:23:05 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cb140ed69e99ddfc606c0305e38ad3b54218eac4a2b551519410da455a7a97`  
		Last Modified: Tue, 01 Jul 2025 14:23:10 GMT  
		Size: 41.1 MB (41119237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d426ed41f5c5ab2072564efe48130a02002d4efd744c7e7962f6c2b4bd0235`  
		Last Modified: Tue, 01 Jul 2025 14:23:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5794d976e6e80e5cb5779c66485ec49872db5a3d44c71caa4b289857ea6558e`  
		Last Modified: Tue, 01 Jul 2025 14:23:06 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29335d2acc0ce04156fa5363c07ef1dbe2dc3e9c2b0ae74cb7fe3fbb2bf18e09`  
		Last Modified: Tue, 01 Jul 2025 14:23:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:9a174f3ec071331cb29afcd2dbc32aa795acbf58266e896a4c671f771560c3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2430d9582934df1e2a872f6ab7d1b2146730721039860790b8bf31c88c7c11a`

```dockerfile
```

-	Layers:
	-	`sha256:bb7a3888ff64f4de991508fbb96cc6b426f0a7ce7cd7585e28f53659a951b6a2`  
		Last Modified: Tue, 01 Jul 2025 17:20:25 GMT  
		Size: 5.1 MB (5071312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a1c81d10a757b25a65d253908c61e845a7fc6ff91b730de56a2676012ed02f5`  
		Last Modified: Tue, 01 Jul 2025 17:20:26 GMT  
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
$ docker pull influxdb@sha256:c226591eb403bd3f3e4b0f37767560d47da9ecb70b8e59a7e53435f4712c5629
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:401ae6cb95dfbc571a2d7c2beabfb992d70eea16c8d06e791a5f60a0b4b6c887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111697817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c059fc4c9a12f435c9f1de74e2eaa292bc4b36ce2c57a715b01869dab22780f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Tue, 24 Jun 2025 22:21:26 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93633f3ed459fd47f2739c524b6fc6bc9fb3d14c3f00a476e7386347b371b32f`  
		Last Modified: Tue, 01 Jul 2025 04:29:51 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0ca01351d272a2b60e9d01390332632a1604d2ad1e3ae8833b9b45ff2b8cc5`  
		Last Modified: Tue, 01 Jul 2025 13:47:48 GMT  
		Size: 39.2 MB (39179283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fed012671239fb217957b0fdfa7dc1819c24e336c95617dc7936445dd02326e`  
		Last Modified: Tue, 01 Jul 2025 04:29:54 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0a817f28139f50b48fbc8138c3f147fe2e16e48da6d6f35b42ceabb3ae79f`  
		Last Modified: Tue, 01 Jul 2025 13:47:50 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b713e01c96351ddde861e8c5329cafbdc2ccb84dd94e1b2fcdc57d70b2a41b0e`  
		Last Modified: Tue, 01 Jul 2025 04:30:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:b67687fc2e926c6bb0e88d95a99b090b91a59a05d502e5fbfae1bdd60d317fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf918f70158f0e4b30301b6cd9e013661d52ae61c5a5a2ef79cd2daf9f53c65`

```dockerfile
```

-	Layers:
	-	`sha256:c22431ed89042ba685c965c048e146c1cdae85cf0c8bf60eff1d87457a66bf1e`  
		Last Modified: Tue, 01 Jul 2025 05:20:35 GMT  
		Size: 4.7 MB (4661024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7738ef4d4fda343df13092fa81f1ebb68e4505808b8fe2e5d4682f82471bc6`  
		Last Modified: Tue, 01 Jul 2025 05:20:36 GMT  
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
$ docker pull influxdb@sha256:5243e1d41041fc58bfc853e6c796941ac42827d2b142b049e33b34ed957c69d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c538c7e8446699a1dd7d66aed8cbb77594c4f01669397aeed8b67de2a445c6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90853893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17bc62dfc6a4aae65aec71c9969280592fb6c131f9e9bf70de3c2a77b388e834`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Tue, 24 Jun 2025 22:21:26 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66f8bd3d13f53c85a80646350ed31fd5f9b2e89d3f4ca0c29229da7ac5d120d`  
		Last Modified: Tue, 01 Jul 2025 04:29:51 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c899dc1b5f3c11ca37140491bfa999211d45a89e4314324b94c457ec4b429568`  
		Last Modified: Tue, 01 Jul 2025 13:15:21 GMT  
		Size: 18.3 MB (18336571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b329dc4701b82f7839c027e1034e3df087cf3eba771b003bc114c5279405bd14`  
		Last Modified: Tue, 01 Jul 2025 04:29:54 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253f2d56b1ec3e6967d6c9ef45fcbd0a5192737351b92ae9b4cb21e2def29ff1`  
		Last Modified: Tue, 01 Jul 2025 04:30:00 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:8b7f743b912c684cd868c00b63b22704fc0edb12110a6c9dec5b899d3dc733fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4599062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242bab184e0d995b7ca508ba918d14f1cbd828967204d4e4213ae35642ad487a`

```dockerfile
```

-	Layers:
	-	`sha256:78ce6c9448fb750452d348d4201f991be0c80e53e2331755c90c2a2465bc6b02`  
		Last Modified: Tue, 01 Jul 2025 05:20:41 GMT  
		Size: 4.6 MB (4585995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe6e0dc863d239c88f6ac0c0c2d4464e26e899410ad167d15d8aeadab868c995`  
		Last Modified: Tue, 01 Jul 2025 05:20:42 GMT  
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
$ docker pull influxdb@sha256:b2766b01a99b4f10054e622df3a7f69cbe41c3722efbdb710f62072b7919ff49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:1fb5b939298bb8ffa728c163cdc5678bc6ee68a6dfde9f13a5507ac1d5cb6799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157213959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4355848b856f8acdc24412629625c7248439e5df15cd10a16bc48b884cb986e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 24 Jun 2025 22:21:26 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV GOSU_VER=1.16
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dba06387eee7a6a1867978ffb3eb271fba52c239bee86389de9766c6be503bb`  
		Last Modified: Tue, 01 Jul 2025 02:27:25 GMT  
		Size: 9.8 MB (9793900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251ae7b28987c8c3564d52c6eea8512558a0bc90a552b81cd6b134d5b8d8d7fa`  
		Last Modified: Tue, 01 Jul 2025 02:27:25 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383d803099a2ac22de23042bf0b37804741628b7bf8071a89325ea088a25e316`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c622176d353333b2f9d79d771df07aee725480647e9403d20c9737655fa9b30b`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 1.0 MB (1006372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938f5ab719643314e090aa6ce65d9e50aead8cbfe6bc3a6af42482512c76e0d7`  
		Last Modified: Tue, 01 Jul 2025 02:27:29 GMT  
		Size: 100.2 MB (100242936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1233992fcb7a3053fe1e41b13effe04c6db0ad63472ce7d59e726dbd42f4619`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 11.8 MB (11773682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd863e2f53471dd98f640025131e115bdaffbcdcc2914ca22728fdfe1d50e664`  
		Last Modified: Tue, 01 Jul 2025 02:27:23 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01aa43ef8e9d4a982a027fbb398a3ea11e887e3c7813d7093775abdbdda1554`  
		Last Modified: Tue, 01 Jul 2025 02:27:23 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a289c46ced789334f801323191cef43221bb0a23cac3d77b416ef725ee5cbba4`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:1ee7e90cf7b7806932034fa772c55c1c4affdabcb0be0c12c0e64e20033f3ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51086f996265644b7a88339580660b76b5f7612f4edfb2dd18699c68b56374b1`

```dockerfile
```

-	Layers:
	-	`sha256:fb6090f40047df8bd26e817f0be7c2815179f7afd9e5d7be2debe0fd1b8eb1de`  
		Last Modified: Tue, 01 Jul 2025 05:20:51 GMT  
		Size: 3.0 MB (2979773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfcc750a77001d29d4bdd252583fb42d41c9024aa9f4c38f00aa372a99cf3413`  
		Last Modified: Tue, 01 Jul 2025 05:20:52 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8e42ef527af5083ae810e246067b2a3f6aa2277e56918a93fb06bd46031140c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151541719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6324acffea320bef2041e9c6a62cf579b505411efd0beffdd02e0662d79e1f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 24 Jun 2025 22:21:26 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV GOSU_VER=1.16
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a9750ced17eb9680c39392299667138966b00b1b8ba9964360f165d34aae01`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 9.6 MB (9590213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e2c1dd6de92d4b17bd420e8296ec5ce8e0be197ae85866ce510089f56810f2`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c215e349bdf9c4c6bd41276069ce530b4a9d7773dc7b224fcfe4c3e09b9b6ac7`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f99d0a91ff766c668b657b3c945795c80020cb8d054ee697cf07674f6df903`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 936.1 KB (936103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c2fa4831c1b6a310ff1261e99f9b42d128151317b5f5eac991034a5ecb21d5`  
		Last Modified: Tue, 01 Jul 2025 07:16:41 GMT  
		Size: 96.0 MB (96038367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6def7749394d2ac8cb71787fa688047c89e3e5fef367537bab1a51ddf408bf`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 11.1 MB (11098985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdc132259701de04ab9a4a64bb74425431c853ac20251882987c28a42a1d142`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034ec54bce93029ae930b80ea7e8dc06d7765dd5c473efdc32285b6eb3d6f803`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f046e46a8c615ae075557bb39ffc00094d3bf394f7ea9f46090669132b49b62`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:513a8211cdaaadf97a7adebd2ae5488fd379582a4bcdd149b884b4f9885a0c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e99790d93b535aad6c085ddb5f618f53566efe13ac414605591664f4279e2df`

```dockerfile
```

-	Layers:
	-	`sha256:12fcca2d0f365ddd3e6c3bd5f0c280b02f6897514f3cd9212b3c5ae8e94b0e0a`  
		Last Modified: Tue, 01 Jul 2025 08:20:29 GMT  
		Size: 3.0 MB (2979001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a55c0cda549b8659bcccfae409e8f85910e7dc92523672c92ebc96c2e64d9b9`  
		Last Modified: Tue, 01 Jul 2025 08:20:30 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:ef14203d7014ac9a0df4f087d186901ea7d19993410b35782f6c3c421738eb25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b45f9c1468673ddce3178e3254bfb69dd0d265681a3711f7098cdda9d7a1f200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81524834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81788ed40247fe21d02e4dfdfce4004e333e989cbd5d3a117fa38c4a93bd2bb0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a130cfd37d419a3c532882536eaedef1bafc0b27786d26fa8734031ed282f629`  
		Last Modified: Wed, 25 Jun 2025 23:44:30 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09084b588ed3780c8d765b3773a7c317059756fd8df728c13f22bdf245b1b49f`  
		Last Modified: Wed, 25 Jun 2025 23:44:32 GMT  
		Size: 9.8 MB (9828507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc32c4c9bf881a64da36b412e68bf1d7af5ef2aea99c52f8882707447b6bb59`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8febccab10f6832094ea40bf28d7483092b5c6f36981b07c850077eb6d04bca`  
		Last Modified: Wed, 25 Jun 2025 23:44:30 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bd30a1b2c851f704df2933dcd72d2b25030b43134eeaa6e0359024b9e1fa44`  
		Last Modified: Wed, 25 Jun 2025 23:44:34 GMT  
		Size: 50.1 MB (50115459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307e398e26d544491a6a8082cfa58950d96e7cf7e776834a9de75b66e871d57f`  
		Last Modified: Wed, 25 Jun 2025 23:44:32 GMT  
		Size: 11.8 MB (11773679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe528122573db93efd8e476a3a2411fa80e1baa481f1e2fa639faf2c4dc0af0a`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b06eabc35c9711191786d2e1fc0449aed0966236962b403b5cf99d113e9ff35`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb42a9c506c5101489ca7c4d7f830e77a6768f02f7a79f2e1ebeb4306408183e`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 6.3 KB (6278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e0958522dca232cad2433959de7371b5f471461905ee8e4d318ad5ea73472929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.9 KB (945914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21da3d2c4a5891c4cf6369823aa4d5113a83bf4d2bd5f206bdf0bba30d928fb3`

```dockerfile
```

-	Layers:
	-	`sha256:5aa61282ffe649196be805c68e3d4b428c7c3d3d3949a3647370a202fa81a660`  
		Last Modified: Thu, 26 Jun 2025 02:20:32 GMT  
		Size: 915.1 KB (915145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35d7696f6fb4c45e223cae84a36259ca39435b1c098643f0462f78f4a4b73662`  
		Last Modified: Thu, 26 Jun 2025 02:20:33 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:437f107bd5053d1dc3609ccc141c429a4c91745661cd5f3e8d3da8b53d43295b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78700300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082c94768c31433b98a8e8d7708517413d47bbe300bf26d775a2265161247fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed31da1742ff6f2fea4e2c1de2831020a3cde9f9a53cb6c20f68e2999f2ad29b`  
		Last Modified: Thu, 26 Jun 2025 04:33:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7119cfa8c39cc0ba46ceb95de3382a8b1afe1e640e270bd0878b201719355f7`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 9.8 MB (9793675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a4b10ba50366c9b86c4c5b71a8d4f2b32f50836d950e814246cbb581e78175`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 5.8 MB (5790439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bee941e7a71079f0cfc9ba5897ef41a20121d3ac8579786780e1ff261ee08a1`  
		Last Modified: Thu, 26 Jun 2025 04:33:34 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d33a71eef49e504ffbcfab1fffba83d18d4d0c83a4515dc0719571987ef418e`  
		Last Modified: Thu, 26 Jun 2025 04:33:39 GMT  
		Size: 48.0 MB (48016233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8426a334c0538e7372e25cef2c29432249dfd5a1d54ca201273c78f9f6fbc14b`  
		Last Modified: Thu, 26 Jun 2025 04:33:36 GMT  
		Size: 11.1 MB (11098967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d78e14eccf6f023ef8080b4032a96140dbf33cc42c4675d64363a7c6ce8fd0`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244bbeb63b7925964730c856045559927dbd13b09e092936221e87657608437a`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac072e09a3481d03deb00c3377298df5c0a5aed3f000f2d8bec5753b2b96faf`  
		Last Modified: Thu, 26 Jun 2025 04:33:34 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c44dfa3394146848d926ea117896a1d9a585d974009d658a307a59ca4411bbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.4 KB (945358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cc39b027c64fbe4a5158a785bddb8a3ee32c63cc63582bddc78251cc0a4cc3`

```dockerfile
```

-	Layers:
	-	`sha256:641b904a03efd6fa5e3efec3f8e6c911dccefa6e4a733e6165094d399569ae39`  
		Last Modified: Thu, 26 Jun 2025 05:20:33 GMT  
		Size: 914.4 KB (914396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92056d58af926d57bb5726daf2d449d247a66c377130463559bee61e740fb941`  
		Last Modified: Thu, 26 Jun 2025 05:20:34 GMT  
		Size: 31.0 KB (30962 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:b2766b01a99b4f10054e622df3a7f69cbe41c3722efbdb710f62072b7919ff49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:1fb5b939298bb8ffa728c163cdc5678bc6ee68a6dfde9f13a5507ac1d5cb6799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157213959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4355848b856f8acdc24412629625c7248439e5df15cd10a16bc48b884cb986e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 24 Jun 2025 22:21:26 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV GOSU_VER=1.16
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dba06387eee7a6a1867978ffb3eb271fba52c239bee86389de9766c6be503bb`  
		Last Modified: Tue, 01 Jul 2025 02:27:25 GMT  
		Size: 9.8 MB (9793900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251ae7b28987c8c3564d52c6eea8512558a0bc90a552b81cd6b134d5b8d8d7fa`  
		Last Modified: Tue, 01 Jul 2025 02:27:25 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383d803099a2ac22de23042bf0b37804741628b7bf8071a89325ea088a25e316`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c622176d353333b2f9d79d771df07aee725480647e9403d20c9737655fa9b30b`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 1.0 MB (1006372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938f5ab719643314e090aa6ce65d9e50aead8cbfe6bc3a6af42482512c76e0d7`  
		Last Modified: Tue, 01 Jul 2025 02:27:29 GMT  
		Size: 100.2 MB (100242936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1233992fcb7a3053fe1e41b13effe04c6db0ad63472ce7d59e726dbd42f4619`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 11.8 MB (11773682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd863e2f53471dd98f640025131e115bdaffbcdcc2914ca22728fdfe1d50e664`  
		Last Modified: Tue, 01 Jul 2025 02:27:23 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01aa43ef8e9d4a982a027fbb398a3ea11e887e3c7813d7093775abdbdda1554`  
		Last Modified: Tue, 01 Jul 2025 02:27:23 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a289c46ced789334f801323191cef43221bb0a23cac3d77b416ef725ee5cbba4`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:1ee7e90cf7b7806932034fa772c55c1c4affdabcb0be0c12c0e64e20033f3ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51086f996265644b7a88339580660b76b5f7612f4edfb2dd18699c68b56374b1`

```dockerfile
```

-	Layers:
	-	`sha256:fb6090f40047df8bd26e817f0be7c2815179f7afd9e5d7be2debe0fd1b8eb1de`  
		Last Modified: Tue, 01 Jul 2025 05:20:51 GMT  
		Size: 3.0 MB (2979773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfcc750a77001d29d4bdd252583fb42d41c9024aa9f4c38f00aa372a99cf3413`  
		Last Modified: Tue, 01 Jul 2025 05:20:52 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8e42ef527af5083ae810e246067b2a3f6aa2277e56918a93fb06bd46031140c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151541719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6324acffea320bef2041e9c6a62cf579b505411efd0beffdd02e0662d79e1f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 24 Jun 2025 22:21:26 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV GOSU_VER=1.16
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a9750ced17eb9680c39392299667138966b00b1b8ba9964360f165d34aae01`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 9.6 MB (9590213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e2c1dd6de92d4b17bd420e8296ec5ce8e0be197ae85866ce510089f56810f2`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c215e349bdf9c4c6bd41276069ce530b4a9d7773dc7b224fcfe4c3e09b9b6ac7`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f99d0a91ff766c668b657b3c945795c80020cb8d054ee697cf07674f6df903`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 936.1 KB (936103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c2fa4831c1b6a310ff1261e99f9b42d128151317b5f5eac991034a5ecb21d5`  
		Last Modified: Tue, 01 Jul 2025 07:16:41 GMT  
		Size: 96.0 MB (96038367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6def7749394d2ac8cb71787fa688047c89e3e5fef367537bab1a51ddf408bf`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 11.1 MB (11098985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdc132259701de04ab9a4a64bb74425431c853ac20251882987c28a42a1d142`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034ec54bce93029ae930b80ea7e8dc06d7765dd5c473efdc32285b6eb3d6f803`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f046e46a8c615ae075557bb39ffc00094d3bf394f7ea9f46090669132b49b62`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:513a8211cdaaadf97a7adebd2ae5488fd379582a4bcdd149b884b4f9885a0c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e99790d93b535aad6c085ddb5f618f53566efe13ac414605591664f4279e2df`

```dockerfile
```

-	Layers:
	-	`sha256:12fcca2d0f365ddd3e6c3bd5f0c280b02f6897514f3cd9212b3c5ae8e94b0e0a`  
		Last Modified: Tue, 01 Jul 2025 08:20:29 GMT  
		Size: 3.0 MB (2979001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a55c0cda549b8659bcccfae409e8f85910e7dc92523672c92ebc96c2e64d9b9`  
		Last Modified: Tue, 01 Jul 2025 08:20:30 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:ef14203d7014ac9a0df4f087d186901ea7d19993410b35782f6c3c421738eb25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b45f9c1468673ddce3178e3254bfb69dd0d265681a3711f7098cdda9d7a1f200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81524834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81788ed40247fe21d02e4dfdfce4004e333e989cbd5d3a117fa38c4a93bd2bb0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a130cfd37d419a3c532882536eaedef1bafc0b27786d26fa8734031ed282f629`  
		Last Modified: Wed, 25 Jun 2025 23:44:30 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09084b588ed3780c8d765b3773a7c317059756fd8df728c13f22bdf245b1b49f`  
		Last Modified: Wed, 25 Jun 2025 23:44:32 GMT  
		Size: 9.8 MB (9828507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc32c4c9bf881a64da36b412e68bf1d7af5ef2aea99c52f8882707447b6bb59`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8febccab10f6832094ea40bf28d7483092b5c6f36981b07c850077eb6d04bca`  
		Last Modified: Wed, 25 Jun 2025 23:44:30 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bd30a1b2c851f704df2933dcd72d2b25030b43134eeaa6e0359024b9e1fa44`  
		Last Modified: Wed, 25 Jun 2025 23:44:34 GMT  
		Size: 50.1 MB (50115459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307e398e26d544491a6a8082cfa58950d96e7cf7e776834a9de75b66e871d57f`  
		Last Modified: Wed, 25 Jun 2025 23:44:32 GMT  
		Size: 11.8 MB (11773679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe528122573db93efd8e476a3a2411fa80e1baa481f1e2fa639faf2c4dc0af0a`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b06eabc35c9711191786d2e1fc0449aed0966236962b403b5cf99d113e9ff35`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb42a9c506c5101489ca7c4d7f830e77a6768f02f7a79f2e1ebeb4306408183e`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 6.3 KB (6278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e0958522dca232cad2433959de7371b5f471461905ee8e4d318ad5ea73472929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.9 KB (945914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21da3d2c4a5891c4cf6369823aa4d5113a83bf4d2bd5f206bdf0bba30d928fb3`

```dockerfile
```

-	Layers:
	-	`sha256:5aa61282ffe649196be805c68e3d4b428c7c3d3d3949a3647370a202fa81a660`  
		Last Modified: Thu, 26 Jun 2025 02:20:32 GMT  
		Size: 915.1 KB (915145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35d7696f6fb4c45e223cae84a36259ca39435b1c098643f0462f78f4a4b73662`  
		Last Modified: Thu, 26 Jun 2025 02:20:33 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:437f107bd5053d1dc3609ccc141c429a4c91745661cd5f3e8d3da8b53d43295b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78700300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082c94768c31433b98a8e8d7708517413d47bbe300bf26d775a2265161247fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed31da1742ff6f2fea4e2c1de2831020a3cde9f9a53cb6c20f68e2999f2ad29b`  
		Last Modified: Thu, 26 Jun 2025 04:33:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7119cfa8c39cc0ba46ceb95de3382a8b1afe1e640e270bd0878b201719355f7`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 9.8 MB (9793675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a4b10ba50366c9b86c4c5b71a8d4f2b32f50836d950e814246cbb581e78175`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 5.8 MB (5790439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bee941e7a71079f0cfc9ba5897ef41a20121d3ac8579786780e1ff261ee08a1`  
		Last Modified: Thu, 26 Jun 2025 04:33:34 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d33a71eef49e504ffbcfab1fffba83d18d4d0c83a4515dc0719571987ef418e`  
		Last Modified: Thu, 26 Jun 2025 04:33:39 GMT  
		Size: 48.0 MB (48016233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8426a334c0538e7372e25cef2c29432249dfd5a1d54ca201273c78f9f6fbc14b`  
		Last Modified: Thu, 26 Jun 2025 04:33:36 GMT  
		Size: 11.1 MB (11098967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d78e14eccf6f023ef8080b4032a96140dbf33cc42c4675d64363a7c6ce8fd0`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244bbeb63b7925964730c856045559927dbd13b09e092936221e87657608437a`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac072e09a3481d03deb00c3377298df5c0a5aed3f000f2d8bec5753b2b96faf`  
		Last Modified: Thu, 26 Jun 2025 04:33:34 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c44dfa3394146848d926ea117896a1d9a585d974009d658a307a59ca4411bbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.4 KB (945358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cc39b027c64fbe4a5158a785bddb8a3ee32c63cc63582bddc78251cc0a4cc3`

```dockerfile
```

-	Layers:
	-	`sha256:641b904a03efd6fa5e3efec3f8e6c911dccefa6e4a733e6165094d399569ae39`  
		Last Modified: Thu, 26 Jun 2025 05:20:33 GMT  
		Size: 914.4 KB (914396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92056d58af926d57bb5726daf2d449d247a66c377130463559bee61e740fb941`  
		Last Modified: Thu, 26 Jun 2025 05:20:34 GMT  
		Size: 31.0 KB (30962 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12`

```console
$ docker pull influxdb@sha256:b2766b01a99b4f10054e622df3a7f69cbe41c3722efbdb710f62072b7919ff49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:1fb5b939298bb8ffa728c163cdc5678bc6ee68a6dfde9f13a5507ac1d5cb6799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157213959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4355848b856f8acdc24412629625c7248439e5df15cd10a16bc48b884cb986e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 24 Jun 2025 22:21:26 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV GOSU_VER=1.16
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dba06387eee7a6a1867978ffb3eb271fba52c239bee86389de9766c6be503bb`  
		Last Modified: Tue, 01 Jul 2025 02:27:25 GMT  
		Size: 9.8 MB (9793900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251ae7b28987c8c3564d52c6eea8512558a0bc90a552b81cd6b134d5b8d8d7fa`  
		Last Modified: Tue, 01 Jul 2025 02:27:25 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383d803099a2ac22de23042bf0b37804741628b7bf8071a89325ea088a25e316`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c622176d353333b2f9d79d771df07aee725480647e9403d20c9737655fa9b30b`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 1.0 MB (1006372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938f5ab719643314e090aa6ce65d9e50aead8cbfe6bc3a6af42482512c76e0d7`  
		Last Modified: Tue, 01 Jul 2025 02:27:29 GMT  
		Size: 100.2 MB (100242936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1233992fcb7a3053fe1e41b13effe04c6db0ad63472ce7d59e726dbd42f4619`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 11.8 MB (11773682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd863e2f53471dd98f640025131e115bdaffbcdcc2914ca22728fdfe1d50e664`  
		Last Modified: Tue, 01 Jul 2025 02:27:23 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01aa43ef8e9d4a982a027fbb398a3ea11e887e3c7813d7093775abdbdda1554`  
		Last Modified: Tue, 01 Jul 2025 02:27:23 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a289c46ced789334f801323191cef43221bb0a23cac3d77b416ef725ee5cbba4`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:1ee7e90cf7b7806932034fa772c55c1c4affdabcb0be0c12c0e64e20033f3ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51086f996265644b7a88339580660b76b5f7612f4edfb2dd18699c68b56374b1`

```dockerfile
```

-	Layers:
	-	`sha256:fb6090f40047df8bd26e817f0be7c2815179f7afd9e5d7be2debe0fd1b8eb1de`  
		Last Modified: Tue, 01 Jul 2025 05:20:51 GMT  
		Size: 3.0 MB (2979773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfcc750a77001d29d4bdd252583fb42d41c9024aa9f4c38f00aa372a99cf3413`  
		Last Modified: Tue, 01 Jul 2025 05:20:52 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8e42ef527af5083ae810e246067b2a3f6aa2277e56918a93fb06bd46031140c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151541719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6324acffea320bef2041e9c6a62cf579b505411efd0beffdd02e0662d79e1f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 24 Jun 2025 22:21:26 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV GOSU_VER=1.16
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a9750ced17eb9680c39392299667138966b00b1b8ba9964360f165d34aae01`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 9.6 MB (9590213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e2c1dd6de92d4b17bd420e8296ec5ce8e0be197ae85866ce510089f56810f2`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c215e349bdf9c4c6bd41276069ce530b4a9d7773dc7b224fcfe4c3e09b9b6ac7`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f99d0a91ff766c668b657b3c945795c80020cb8d054ee697cf07674f6df903`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 936.1 KB (936103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c2fa4831c1b6a310ff1261e99f9b42d128151317b5f5eac991034a5ecb21d5`  
		Last Modified: Tue, 01 Jul 2025 07:16:41 GMT  
		Size: 96.0 MB (96038367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6def7749394d2ac8cb71787fa688047c89e3e5fef367537bab1a51ddf408bf`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 11.1 MB (11098985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdc132259701de04ab9a4a64bb74425431c853ac20251882987c28a42a1d142`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034ec54bce93029ae930b80ea7e8dc06d7765dd5c473efdc32285b6eb3d6f803`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f046e46a8c615ae075557bb39ffc00094d3bf394f7ea9f46090669132b49b62`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:513a8211cdaaadf97a7adebd2ae5488fd379582a4bcdd149b884b4f9885a0c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e99790d93b535aad6c085ddb5f618f53566efe13ac414605591664f4279e2df`

```dockerfile
```

-	Layers:
	-	`sha256:12fcca2d0f365ddd3e6c3bd5f0c280b02f6897514f3cd9212b3c5ae8e94b0e0a`  
		Last Modified: Tue, 01 Jul 2025 08:20:29 GMT  
		Size: 3.0 MB (2979001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a55c0cda549b8659bcccfae409e8f85910e7dc92523672c92ebc96c2e64d9b9`  
		Last Modified: Tue, 01 Jul 2025 08:20:30 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12-alpine`

```console
$ docker pull influxdb@sha256:ef14203d7014ac9a0df4f087d186901ea7d19993410b35782f6c3c421738eb25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b45f9c1468673ddce3178e3254bfb69dd0d265681a3711f7098cdda9d7a1f200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81524834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81788ed40247fe21d02e4dfdfce4004e333e989cbd5d3a117fa38c4a93bd2bb0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a130cfd37d419a3c532882536eaedef1bafc0b27786d26fa8734031ed282f629`  
		Last Modified: Wed, 25 Jun 2025 23:44:30 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09084b588ed3780c8d765b3773a7c317059756fd8df728c13f22bdf245b1b49f`  
		Last Modified: Wed, 25 Jun 2025 23:44:32 GMT  
		Size: 9.8 MB (9828507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc32c4c9bf881a64da36b412e68bf1d7af5ef2aea99c52f8882707447b6bb59`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8febccab10f6832094ea40bf28d7483092b5c6f36981b07c850077eb6d04bca`  
		Last Modified: Wed, 25 Jun 2025 23:44:30 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bd30a1b2c851f704df2933dcd72d2b25030b43134eeaa6e0359024b9e1fa44`  
		Last Modified: Wed, 25 Jun 2025 23:44:34 GMT  
		Size: 50.1 MB (50115459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307e398e26d544491a6a8082cfa58950d96e7cf7e776834a9de75b66e871d57f`  
		Last Modified: Wed, 25 Jun 2025 23:44:32 GMT  
		Size: 11.8 MB (11773679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe528122573db93efd8e476a3a2411fa80e1baa481f1e2fa639faf2c4dc0af0a`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b06eabc35c9711191786d2e1fc0449aed0966236962b403b5cf99d113e9ff35`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb42a9c506c5101489ca7c4d7f830e77a6768f02f7a79f2e1ebeb4306408183e`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 6.3 KB (6278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e0958522dca232cad2433959de7371b5f471461905ee8e4d318ad5ea73472929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.9 KB (945914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21da3d2c4a5891c4cf6369823aa4d5113a83bf4d2bd5f206bdf0bba30d928fb3`

```dockerfile
```

-	Layers:
	-	`sha256:5aa61282ffe649196be805c68e3d4b428c7c3d3d3949a3647370a202fa81a660`  
		Last Modified: Thu, 26 Jun 2025 02:20:32 GMT  
		Size: 915.1 KB (915145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35d7696f6fb4c45e223cae84a36259ca39435b1c098643f0462f78f4a4b73662`  
		Last Modified: Thu, 26 Jun 2025 02:20:33 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:437f107bd5053d1dc3609ccc141c429a4c91745661cd5f3e8d3da8b53d43295b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78700300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082c94768c31433b98a8e8d7708517413d47bbe300bf26d775a2265161247fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed31da1742ff6f2fea4e2c1de2831020a3cde9f9a53cb6c20f68e2999f2ad29b`  
		Last Modified: Thu, 26 Jun 2025 04:33:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7119cfa8c39cc0ba46ceb95de3382a8b1afe1e640e270bd0878b201719355f7`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 9.8 MB (9793675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a4b10ba50366c9b86c4c5b71a8d4f2b32f50836d950e814246cbb581e78175`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 5.8 MB (5790439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bee941e7a71079f0cfc9ba5897ef41a20121d3ac8579786780e1ff261ee08a1`  
		Last Modified: Thu, 26 Jun 2025 04:33:34 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d33a71eef49e504ffbcfab1fffba83d18d4d0c83a4515dc0719571987ef418e`  
		Last Modified: Thu, 26 Jun 2025 04:33:39 GMT  
		Size: 48.0 MB (48016233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8426a334c0538e7372e25cef2c29432249dfd5a1d54ca201273c78f9f6fbc14b`  
		Last Modified: Thu, 26 Jun 2025 04:33:36 GMT  
		Size: 11.1 MB (11098967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d78e14eccf6f023ef8080b4032a96140dbf33cc42c4675d64363a7c6ce8fd0`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244bbeb63b7925964730c856045559927dbd13b09e092936221e87657608437a`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac072e09a3481d03deb00c3377298df5c0a5aed3f000f2d8bec5753b2b96faf`  
		Last Modified: Thu, 26 Jun 2025 04:33:34 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c44dfa3394146848d926ea117896a1d9a585d974009d658a307a59ca4411bbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.4 KB (945358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cc39b027c64fbe4a5158a785bddb8a3ee32c63cc63582bddc78251cc0a4cc3`

```dockerfile
```

-	Layers:
	-	`sha256:641b904a03efd6fa5e3efec3f8e6c911dccefa6e4a733e6165094d399569ae39`  
		Last Modified: Thu, 26 Jun 2025 05:20:33 GMT  
		Size: 914.4 KB (914396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92056d58af926d57bb5726daf2d449d247a66c377130463559bee61e740fb941`  
		Last Modified: Thu, 26 Jun 2025 05:20:34 GMT  
		Size: 31.0 KB (30962 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:c8a97fa106aef068619ed0f809be49b757060eae65830e230e9e0d2304f94182
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:e9cb99cfc96033da9b3567169ca7aaffdc988eeedfbd0e773167cf7c0d864413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115357882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f51b10172412a4dcdd61733cb0fbc4eeb000a1489eb61b7ce10abc85b340b7`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26e20798f7d55716229eaecc7a930dfb9cb2be3b832c1b5815f578c0bbc58c2`  
		Last Modified: Thu, 03 Jul 2025 18:11:50 GMT  
		Size: 6.7 MB (6664725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9341771867e8a8b7edc9a1ed23942815c29c1ff394dc262e21b228e15b67adf6`  
		Last Modified: Thu, 03 Jul 2025 18:11:50 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a9f97258bff88a66c7d0799e1cca0168159476428196180dcb659145f73d5e`  
		Last Modified: Thu, 03 Jul 2025 18:12:00 GMT  
		Size: 79.0 MB (78970664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdad7988a9b22741b2289f955fef077117f4ad807a3beefc1675f7678a26661`  
		Last Modified: Thu, 03 Jul 2025 18:11:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2602f72de16bb4663944d1242b436d41dae5df4baa325999f8edc8fde9cfc04`  
		Last Modified: Thu, 03 Jul 2025 18:11:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:8c0a91af18f62e031e89b61ff6bc071eb36777896be769f9c91deee87e611c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431a0994b9672df8b2f95e5ec33eb7fdc203380417b687669898b2c2a36cf24e`

```dockerfile
```

-	Layers:
	-	`sha256:b8c2cd2346579d3f5d92615229e24bc81641f3f74fcde66fd036b7d0db75c627`  
		Last Modified: Thu, 03 Jul 2025 20:20:36 GMT  
		Size: 2.3 MB (2311303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250998b6caea34c1ff59f0a8aaddaadea842d3617256fccbf47477924ebc33ec`  
		Last Modified: Thu, 03 Jul 2025 20:20:37 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:25f576cfb27fa503e0b4faad047f2c06288e8c84709c767c598fa00d6c36a01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102895928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404f1926537a3c0ba8ae49f875ff9085f97f713e7e733801929816052f2e5135`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c0686a251b16fc8cbd211dd5bf5418ccc2bd75968ab247e18683ffb32d360e`  
		Last Modified: Wed, 02 Jul 2025 05:43:01 GMT  
		Size: 6.7 MB (6675401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929431d0f1ad953782d674eae05c259f14e0a696e1e97ac83b03b176f22ee189`  
		Last Modified: Wed, 02 Jul 2025 05:43:00 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be577860d3bf6727123bbc988af49989b1ea6badf2520371cc17e31e42d622a8`  
		Last Modified: Thu, 03 Jul 2025 18:22:49 GMT  
		Size: 67.4 MB (67360381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029eb551df41bdea62f1a9c5a6315f93da75ebef3b272dbe84313f1238d5aa71`  
		Last Modified: Thu, 03 Jul 2025 18:22:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282cd605924be4e43bce5a0c961910f7823978985772a79faa510fb1f50291d`  
		Last Modified: Thu, 03 Jul 2025 18:22:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4bf87fdcda35296f02175372f9085cab250d3ebef40c982fc66d4fd8935baba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9460a943d60135b3e7e1a8670fc6df2c4a22966d42a5837da4a60eaea5ecbb12`

```dockerfile
```

-	Layers:
	-	`sha256:4a85b56da49576a265c6a0d1a85eb01f35d9b5840c342eee33e9a6139707d1d8`  
		Last Modified: Thu, 03 Jul 2025 20:20:41 GMT  
		Size: 2.3 MB (2312385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f5d4006592fd4d12771b83c3d5c24b926c4d8b2d7308cad1377be05afbac57d`  
		Last Modified: Thu, 03 Jul 2025 20:20:42 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:eb5fc1d05cf0937c2fe97bb9ab45ca1b5e5a5ce2b1ee3377e88d5dd3a618a96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:51ca1c4c21da5d2f45cb25ceec61559c3919f9521802899d0f2b69d5a3a3cb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124839300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4274af6508e5531d0b5672323bf4180613ffe67b84b3d805f4ae8d4350c2729`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cbb8c7e407a8ed1b6742c78ccf99268ca9a9f4f9461e84334e010d0c3fc6b2`  
		Last Modified: Thu, 03 Jul 2025 18:11:46 GMT  
		Size: 6.7 MB (6664693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bb0d4c62c6f30adba13254138a7c0077325f2b344fec2292e156bf82b154aa`  
		Last Modified: Thu, 03 Jul 2025 18:11:46 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099a272d8885a7c27177e0fa1a5d81bc86b7651a6a6dc811fb2cde96465e7e8`  
		Last Modified: Thu, 03 Jul 2025 18:11:54 GMT  
		Size: 88.5 MB (88452114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fb1fe653059d8f57e6e6535e1b1ad39ac8494ed924ae53f87c13fcb7f93434`  
		Last Modified: Thu, 03 Jul 2025 18:11:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ececb2420e7b1089629603bd36c757aac77f2facdff3ce28a66e65f26f23dc0a`  
		Last Modified: Thu, 03 Jul 2025 18:11:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:da923ab8fb0d75f1062303f7b9fc90f73dc1a7d68fc4e2b7b7694212ca5dc303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d055ef4fc120adbb7f6a864e6fc03fe084719bec53966773d388607ac42f112`

```dockerfile
```

-	Layers:
	-	`sha256:b4bd134cf58714e89a7ab27d9bddec3abb746c70050479cddb0f8222854f4e28`  
		Last Modified: Thu, 03 Jul 2025 20:20:43 GMT  
		Size: 2.3 MB (2311351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b795e89f5b04e68672c789647d166c8674b392c335c79373207cbedfcc240fc3`  
		Last Modified: Thu, 03 Jul 2025 20:20:44 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0f3bf598b4dd54a2fef4810b0dc6a9a19dc9b346741698a490dcf62afca4a4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112051988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97200ea52b35f63f93e14a8266421e6b311ba9fae7c9fa09eea879e837b03f0`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c0686a251b16fc8cbd211dd5bf5418ccc2bd75968ab247e18683ffb32d360e`  
		Last Modified: Wed, 02 Jul 2025 05:43:01 GMT  
		Size: 6.7 MB (6675401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929431d0f1ad953782d674eae05c259f14e0a696e1e97ac83b03b176f22ee189`  
		Last Modified: Wed, 02 Jul 2025 05:43:00 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9aff82d27e2e354c914e8229bdae43752f746fcd3a5a0291347ee5f061861ce`  
		Last Modified: Thu, 03 Jul 2025 18:23:17 GMT  
		Size: 76.5 MB (76516437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235450b5238cc838f09d41e21f3fab325c9dd373696c57c26b34527b5a5e6a3`  
		Last Modified: Thu, 03 Jul 2025 18:23:10 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d438e265e8fcf90be481eff26217ea242fdbb36cc041c6c64c926e7e05a920`  
		Last Modified: Thu, 03 Jul 2025 18:23:10 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:c1cfcd19097d8a713d0addf17608c76e29943679bc9a6914edd4cb2e1c36eebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b187a0f2839da5fe6e87beda84f6078eb8be7bc4f710ea632b45e7919528d3ee`

```dockerfile
```

-	Layers:
	-	`sha256:d50396d28e52e16b20e21903203b11fd26f326edd525664c213a322ea376ec83`  
		Last Modified: Thu, 03 Jul 2025 20:20:48 GMT  
		Size: 2.3 MB (2312433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23062a068ca515ec8b7ce409eaea441db2c9781e141e1cd8ea2d62748bbf3a25`  
		Last Modified: Thu, 03 Jul 2025 20:20:48 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.2-core`

```console
$ docker pull influxdb@sha256:c8a97fa106aef068619ed0f809be49b757060eae65830e230e9e0d2304f94182
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.2-core` - linux; amd64

```console
$ docker pull influxdb@sha256:e9cb99cfc96033da9b3567169ca7aaffdc988eeedfbd0e773167cf7c0d864413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115357882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f51b10172412a4dcdd61733cb0fbc4eeb000a1489eb61b7ce10abc85b340b7`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26e20798f7d55716229eaecc7a930dfb9cb2be3b832c1b5815f578c0bbc58c2`  
		Last Modified: Thu, 03 Jul 2025 18:11:50 GMT  
		Size: 6.7 MB (6664725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9341771867e8a8b7edc9a1ed23942815c29c1ff394dc262e21b228e15b67adf6`  
		Last Modified: Thu, 03 Jul 2025 18:11:50 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a9f97258bff88a66c7d0799e1cca0168159476428196180dcb659145f73d5e`  
		Last Modified: Thu, 03 Jul 2025 18:12:00 GMT  
		Size: 79.0 MB (78970664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdad7988a9b22741b2289f955fef077117f4ad807a3beefc1675f7678a26661`  
		Last Modified: Thu, 03 Jul 2025 18:11:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2602f72de16bb4663944d1242b436d41dae5df4baa325999f8edc8fde9cfc04`  
		Last Modified: Thu, 03 Jul 2025 18:11:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:8c0a91af18f62e031e89b61ff6bc071eb36777896be769f9c91deee87e611c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431a0994b9672df8b2f95e5ec33eb7fdc203380417b687669898b2c2a36cf24e`

```dockerfile
```

-	Layers:
	-	`sha256:b8c2cd2346579d3f5d92615229e24bc81641f3f74fcde66fd036b7d0db75c627`  
		Last Modified: Thu, 03 Jul 2025 20:20:36 GMT  
		Size: 2.3 MB (2311303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250998b6caea34c1ff59f0a8aaddaadea842d3617256fccbf47477924ebc33ec`  
		Last Modified: Thu, 03 Jul 2025 20:20:37 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.2-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:25f576cfb27fa503e0b4faad047f2c06288e8c84709c767c598fa00d6c36a01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102895928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404f1926537a3c0ba8ae49f875ff9085f97f713e7e733801929816052f2e5135`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c0686a251b16fc8cbd211dd5bf5418ccc2bd75968ab247e18683ffb32d360e`  
		Last Modified: Wed, 02 Jul 2025 05:43:01 GMT  
		Size: 6.7 MB (6675401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929431d0f1ad953782d674eae05c259f14e0a696e1e97ac83b03b176f22ee189`  
		Last Modified: Wed, 02 Jul 2025 05:43:00 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be577860d3bf6727123bbc988af49989b1ea6badf2520371cc17e31e42d622a8`  
		Last Modified: Thu, 03 Jul 2025 18:22:49 GMT  
		Size: 67.4 MB (67360381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029eb551df41bdea62f1a9c5a6315f93da75ebef3b272dbe84313f1238d5aa71`  
		Last Modified: Thu, 03 Jul 2025 18:22:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282cd605924be4e43bce5a0c961910f7823978985772a79faa510fb1f50291d`  
		Last Modified: Thu, 03 Jul 2025 18:22:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4bf87fdcda35296f02175372f9085cab250d3ebef40c982fc66d4fd8935baba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9460a943d60135b3e7e1a8670fc6df2c4a22966d42a5837da4a60eaea5ecbb12`

```dockerfile
```

-	Layers:
	-	`sha256:4a85b56da49576a265c6a0d1a85eb01f35d9b5840c342eee33e9a6139707d1d8`  
		Last Modified: Thu, 03 Jul 2025 20:20:41 GMT  
		Size: 2.3 MB (2312385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f5d4006592fd4d12771b83c3d5c24b926c4d8b2d7308cad1377be05afbac57d`  
		Last Modified: Thu, 03 Jul 2025 20:20:42 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.2-enterprise`

```console
$ docker pull influxdb@sha256:eb5fc1d05cf0937c2fe97bb9ab45ca1b5e5a5ce2b1ee3377e88d5dd3a618a96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.2-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:51ca1c4c21da5d2f45cb25ceec61559c3919f9521802899d0f2b69d5a3a3cb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124839300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4274af6508e5531d0b5672323bf4180613ffe67b84b3d805f4ae8d4350c2729`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cbb8c7e407a8ed1b6742c78ccf99268ca9a9f4f9461e84334e010d0c3fc6b2`  
		Last Modified: Thu, 03 Jul 2025 18:11:46 GMT  
		Size: 6.7 MB (6664693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bb0d4c62c6f30adba13254138a7c0077325f2b344fec2292e156bf82b154aa`  
		Last Modified: Thu, 03 Jul 2025 18:11:46 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099a272d8885a7c27177e0fa1a5d81bc86b7651a6a6dc811fb2cde96465e7e8`  
		Last Modified: Thu, 03 Jul 2025 18:11:54 GMT  
		Size: 88.5 MB (88452114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fb1fe653059d8f57e6e6535e1b1ad39ac8494ed924ae53f87c13fcb7f93434`  
		Last Modified: Thu, 03 Jul 2025 18:11:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ececb2420e7b1089629603bd36c757aac77f2facdff3ce28a66e65f26f23dc0a`  
		Last Modified: Thu, 03 Jul 2025 18:11:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:da923ab8fb0d75f1062303f7b9fc90f73dc1a7d68fc4e2b7b7694212ca5dc303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d055ef4fc120adbb7f6a864e6fc03fe084719bec53966773d388607ac42f112`

```dockerfile
```

-	Layers:
	-	`sha256:b4bd134cf58714e89a7ab27d9bddec3abb746c70050479cddb0f8222854f4e28`  
		Last Modified: Thu, 03 Jul 2025 20:20:43 GMT  
		Size: 2.3 MB (2311351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b795e89f5b04e68672c789647d166c8674b392c335c79373207cbedfcc240fc3`  
		Last Modified: Thu, 03 Jul 2025 20:20:44 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.2-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0f3bf598b4dd54a2fef4810b0dc6a9a19dc9b346741698a490dcf62afca4a4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112051988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97200ea52b35f63f93e14a8266421e6b311ba9fae7c9fa09eea879e837b03f0`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c0686a251b16fc8cbd211dd5bf5418ccc2bd75968ab247e18683ffb32d360e`  
		Last Modified: Wed, 02 Jul 2025 05:43:01 GMT  
		Size: 6.7 MB (6675401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929431d0f1ad953782d674eae05c259f14e0a696e1e97ac83b03b176f22ee189`  
		Last Modified: Wed, 02 Jul 2025 05:43:00 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9aff82d27e2e354c914e8229bdae43752f746fcd3a5a0291347ee5f061861ce`  
		Last Modified: Thu, 03 Jul 2025 18:23:17 GMT  
		Size: 76.5 MB (76516437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235450b5238cc838f09d41e21f3fab325c9dd373696c57c26b34527b5a5e6a3`  
		Last Modified: Thu, 03 Jul 2025 18:23:10 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d438e265e8fcf90be481eff26217ea242fdbb36cc041c6c64c926e7e05a920`  
		Last Modified: Thu, 03 Jul 2025 18:23:10 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:c1cfcd19097d8a713d0addf17608c76e29943679bc9a6914edd4cb2e1c36eebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b187a0f2839da5fe6e87beda84f6078eb8be7bc4f710ea632b45e7919528d3ee`

```dockerfile
```

-	Layers:
	-	`sha256:d50396d28e52e16b20e21903203b11fd26f326edd525664c213a322ea376ec83`  
		Last Modified: Thu, 03 Jul 2025 20:20:48 GMT  
		Size: 2.3 MB (2312433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23062a068ca515ec8b7ce409eaea441db2c9781e141e1cd8ea2d62748bbf3a25`  
		Last Modified: Thu, 03 Jul 2025 20:20:48 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.2.1-core`

```console
$ docker pull influxdb@sha256:c8a97fa106aef068619ed0f809be49b757060eae65830e230e9e0d2304f94182
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.2.1-core` - linux; amd64

```console
$ docker pull influxdb@sha256:e9cb99cfc96033da9b3567169ca7aaffdc988eeedfbd0e773167cf7c0d864413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115357882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f51b10172412a4dcdd61733cb0fbc4eeb000a1489eb61b7ce10abc85b340b7`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26e20798f7d55716229eaecc7a930dfb9cb2be3b832c1b5815f578c0bbc58c2`  
		Last Modified: Thu, 03 Jul 2025 18:11:50 GMT  
		Size: 6.7 MB (6664725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9341771867e8a8b7edc9a1ed23942815c29c1ff394dc262e21b228e15b67adf6`  
		Last Modified: Thu, 03 Jul 2025 18:11:50 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a9f97258bff88a66c7d0799e1cca0168159476428196180dcb659145f73d5e`  
		Last Modified: Thu, 03 Jul 2025 18:12:00 GMT  
		Size: 79.0 MB (78970664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdad7988a9b22741b2289f955fef077117f4ad807a3beefc1675f7678a26661`  
		Last Modified: Thu, 03 Jul 2025 18:11:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2602f72de16bb4663944d1242b436d41dae5df4baa325999f8edc8fde9cfc04`  
		Last Modified: Thu, 03 Jul 2025 18:11:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2.1-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:8c0a91af18f62e031e89b61ff6bc071eb36777896be769f9c91deee87e611c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431a0994b9672df8b2f95e5ec33eb7fdc203380417b687669898b2c2a36cf24e`

```dockerfile
```

-	Layers:
	-	`sha256:b8c2cd2346579d3f5d92615229e24bc81641f3f74fcde66fd036b7d0db75c627`  
		Last Modified: Thu, 03 Jul 2025 20:20:36 GMT  
		Size: 2.3 MB (2311303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250998b6caea34c1ff59f0a8aaddaadea842d3617256fccbf47477924ebc33ec`  
		Last Modified: Thu, 03 Jul 2025 20:20:37 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.2.1-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:25f576cfb27fa503e0b4faad047f2c06288e8c84709c767c598fa00d6c36a01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102895928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404f1926537a3c0ba8ae49f875ff9085f97f713e7e733801929816052f2e5135`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c0686a251b16fc8cbd211dd5bf5418ccc2bd75968ab247e18683ffb32d360e`  
		Last Modified: Wed, 02 Jul 2025 05:43:01 GMT  
		Size: 6.7 MB (6675401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929431d0f1ad953782d674eae05c259f14e0a696e1e97ac83b03b176f22ee189`  
		Last Modified: Wed, 02 Jul 2025 05:43:00 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be577860d3bf6727123bbc988af49989b1ea6badf2520371cc17e31e42d622a8`  
		Last Modified: Thu, 03 Jul 2025 18:22:49 GMT  
		Size: 67.4 MB (67360381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029eb551df41bdea62f1a9c5a6315f93da75ebef3b272dbe84313f1238d5aa71`  
		Last Modified: Thu, 03 Jul 2025 18:22:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282cd605924be4e43bce5a0c961910f7823978985772a79faa510fb1f50291d`  
		Last Modified: Thu, 03 Jul 2025 18:22:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2.1-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4bf87fdcda35296f02175372f9085cab250d3ebef40c982fc66d4fd8935baba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9460a943d60135b3e7e1a8670fc6df2c4a22966d42a5837da4a60eaea5ecbb12`

```dockerfile
```

-	Layers:
	-	`sha256:4a85b56da49576a265c6a0d1a85eb01f35d9b5840c342eee33e9a6139707d1d8`  
		Last Modified: Thu, 03 Jul 2025 20:20:41 GMT  
		Size: 2.3 MB (2312385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f5d4006592fd4d12771b83c3d5c24b926c4d8b2d7308cad1377be05afbac57d`  
		Last Modified: Thu, 03 Jul 2025 20:20:42 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.2.1-enterprise`

```console
$ docker pull influxdb@sha256:eb5fc1d05cf0937c2fe97bb9ab45ca1b5e5a5ce2b1ee3377e88d5dd3a618a96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.2.1-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:51ca1c4c21da5d2f45cb25ceec61559c3919f9521802899d0f2b69d5a3a3cb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124839300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4274af6508e5531d0b5672323bf4180613ffe67b84b3d805f4ae8d4350c2729`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cbb8c7e407a8ed1b6742c78ccf99268ca9a9f4f9461e84334e010d0c3fc6b2`  
		Last Modified: Thu, 03 Jul 2025 18:11:46 GMT  
		Size: 6.7 MB (6664693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bb0d4c62c6f30adba13254138a7c0077325f2b344fec2292e156bf82b154aa`  
		Last Modified: Thu, 03 Jul 2025 18:11:46 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099a272d8885a7c27177e0fa1a5d81bc86b7651a6a6dc811fb2cde96465e7e8`  
		Last Modified: Thu, 03 Jul 2025 18:11:54 GMT  
		Size: 88.5 MB (88452114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fb1fe653059d8f57e6e6535e1b1ad39ac8494ed924ae53f87c13fcb7f93434`  
		Last Modified: Thu, 03 Jul 2025 18:11:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ececb2420e7b1089629603bd36c757aac77f2facdff3ce28a66e65f26f23dc0a`  
		Last Modified: Thu, 03 Jul 2025 18:11:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2.1-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:da923ab8fb0d75f1062303f7b9fc90f73dc1a7d68fc4e2b7b7694212ca5dc303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d055ef4fc120adbb7f6a864e6fc03fe084719bec53966773d388607ac42f112`

```dockerfile
```

-	Layers:
	-	`sha256:b4bd134cf58714e89a7ab27d9bddec3abb746c70050479cddb0f8222854f4e28`  
		Last Modified: Thu, 03 Jul 2025 20:20:43 GMT  
		Size: 2.3 MB (2311351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b795e89f5b04e68672c789647d166c8674b392c335c79373207cbedfcc240fc3`  
		Last Modified: Thu, 03 Jul 2025 20:20:44 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.2.1-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0f3bf598b4dd54a2fef4810b0dc6a9a19dc9b346741698a490dcf62afca4a4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112051988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97200ea52b35f63f93e14a8266421e6b311ba9fae7c9fa09eea879e837b03f0`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c0686a251b16fc8cbd211dd5bf5418ccc2bd75968ab247e18683ffb32d360e`  
		Last Modified: Wed, 02 Jul 2025 05:43:01 GMT  
		Size: 6.7 MB (6675401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929431d0f1ad953782d674eae05c259f14e0a696e1e97ac83b03b176f22ee189`  
		Last Modified: Wed, 02 Jul 2025 05:43:00 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9aff82d27e2e354c914e8229bdae43752f746fcd3a5a0291347ee5f061861ce`  
		Last Modified: Thu, 03 Jul 2025 18:23:17 GMT  
		Size: 76.5 MB (76516437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235450b5238cc838f09d41e21f3fab325c9dd373696c57c26b34527b5a5e6a3`  
		Last Modified: Thu, 03 Jul 2025 18:23:10 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d438e265e8fcf90be481eff26217ea242fdbb36cc041c6c64c926e7e05a920`  
		Last Modified: Thu, 03 Jul 2025 18:23:10 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2.1-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:c1cfcd19097d8a713d0addf17608c76e29943679bc9a6914edd4cb2e1c36eebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b187a0f2839da5fe6e87beda84f6078eb8be7bc4f710ea632b45e7919528d3ee`

```dockerfile
```

-	Layers:
	-	`sha256:d50396d28e52e16b20e21903203b11fd26f326edd525664c213a322ea376ec83`  
		Last Modified: Thu, 03 Jul 2025 20:20:48 GMT  
		Size: 2.3 MB (2312433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23062a068ca515ec8b7ce409eaea441db2c9781e141e1cd8ea2d62748bbf3a25`  
		Last Modified: Thu, 03 Jul 2025 20:20:48 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:ef14203d7014ac9a0df4f087d186901ea7d19993410b35782f6c3c421738eb25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b45f9c1468673ddce3178e3254bfb69dd0d265681a3711f7098cdda9d7a1f200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81524834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81788ed40247fe21d02e4dfdfce4004e333e989cbd5d3a117fa38c4a93bd2bb0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a130cfd37d419a3c532882536eaedef1bafc0b27786d26fa8734031ed282f629`  
		Last Modified: Wed, 25 Jun 2025 23:44:30 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09084b588ed3780c8d765b3773a7c317059756fd8df728c13f22bdf245b1b49f`  
		Last Modified: Wed, 25 Jun 2025 23:44:32 GMT  
		Size: 9.8 MB (9828507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc32c4c9bf881a64da36b412e68bf1d7af5ef2aea99c52f8882707447b6bb59`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8febccab10f6832094ea40bf28d7483092b5c6f36981b07c850077eb6d04bca`  
		Last Modified: Wed, 25 Jun 2025 23:44:30 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bd30a1b2c851f704df2933dcd72d2b25030b43134eeaa6e0359024b9e1fa44`  
		Last Modified: Wed, 25 Jun 2025 23:44:34 GMT  
		Size: 50.1 MB (50115459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307e398e26d544491a6a8082cfa58950d96e7cf7e776834a9de75b66e871d57f`  
		Last Modified: Wed, 25 Jun 2025 23:44:32 GMT  
		Size: 11.8 MB (11773679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe528122573db93efd8e476a3a2411fa80e1baa481f1e2fa639faf2c4dc0af0a`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b06eabc35c9711191786d2e1fc0449aed0966236962b403b5cf99d113e9ff35`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb42a9c506c5101489ca7c4d7f830e77a6768f02f7a79f2e1ebeb4306408183e`  
		Last Modified: Wed, 25 Jun 2025 23:44:31 GMT  
		Size: 6.3 KB (6278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e0958522dca232cad2433959de7371b5f471461905ee8e4d318ad5ea73472929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.9 KB (945914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21da3d2c4a5891c4cf6369823aa4d5113a83bf4d2bd5f206bdf0bba30d928fb3`

```dockerfile
```

-	Layers:
	-	`sha256:5aa61282ffe649196be805c68e3d4b428c7c3d3d3949a3647370a202fa81a660`  
		Last Modified: Thu, 26 Jun 2025 02:20:32 GMT  
		Size: 915.1 KB (915145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35d7696f6fb4c45e223cae84a36259ca39435b1c098643f0462f78f4a4b73662`  
		Last Modified: Thu, 26 Jun 2025 02:20:33 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:437f107bd5053d1dc3609ccc141c429a4c91745661cd5f3e8d3da8b53d43295b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78700300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082c94768c31433b98a8e8d7708517413d47bbe300bf26d775a2265161247fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed31da1742ff6f2fea4e2c1de2831020a3cde9f9a53cb6c20f68e2999f2ad29b`  
		Last Modified: Thu, 26 Jun 2025 04:33:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7119cfa8c39cc0ba46ceb95de3382a8b1afe1e640e270bd0878b201719355f7`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 9.8 MB (9793675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a4b10ba50366c9b86c4c5b71a8d4f2b32f50836d950e814246cbb581e78175`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 5.8 MB (5790439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bee941e7a71079f0cfc9ba5897ef41a20121d3ac8579786780e1ff261ee08a1`  
		Last Modified: Thu, 26 Jun 2025 04:33:34 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d33a71eef49e504ffbcfab1fffba83d18d4d0c83a4515dc0719571987ef418e`  
		Last Modified: Thu, 26 Jun 2025 04:33:39 GMT  
		Size: 48.0 MB (48016233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8426a334c0538e7372e25cef2c29432249dfd5a1d54ca201273c78f9f6fbc14b`  
		Last Modified: Thu, 26 Jun 2025 04:33:36 GMT  
		Size: 11.1 MB (11098967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d78e14eccf6f023ef8080b4032a96140dbf33cc42c4675d64363a7c6ce8fd0`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244bbeb63b7925964730c856045559927dbd13b09e092936221e87657608437a`  
		Last Modified: Thu, 26 Jun 2025 04:33:35 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac072e09a3481d03deb00c3377298df5c0a5aed3f000f2d8bec5753b2b96faf`  
		Last Modified: Thu, 26 Jun 2025 04:33:34 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c44dfa3394146848d926ea117896a1d9a585d974009d658a307a59ca4411bbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.4 KB (945358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cc39b027c64fbe4a5158a785bddb8a3ee32c63cc63582bddc78251cc0a4cc3`

```dockerfile
```

-	Layers:
	-	`sha256:641b904a03efd6fa5e3efec3f8e6c911dccefa6e4a733e6165094d399569ae39`  
		Last Modified: Thu, 26 Jun 2025 05:20:33 GMT  
		Size: 914.4 KB (914396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92056d58af926d57bb5726daf2d449d247a66c377130463559bee61e740fb941`  
		Last Modified: Thu, 26 Jun 2025 05:20:34 GMT  
		Size: 31.0 KB (30962 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:core`

```console
$ docker pull influxdb@sha256:c8a97fa106aef068619ed0f809be49b757060eae65830e230e9e0d2304f94182
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:e9cb99cfc96033da9b3567169ca7aaffdc988eeedfbd0e773167cf7c0d864413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115357882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f51b10172412a4dcdd61733cb0fbc4eeb000a1489eb61b7ce10abc85b340b7`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26e20798f7d55716229eaecc7a930dfb9cb2be3b832c1b5815f578c0bbc58c2`  
		Last Modified: Thu, 03 Jul 2025 18:11:50 GMT  
		Size: 6.7 MB (6664725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9341771867e8a8b7edc9a1ed23942815c29c1ff394dc262e21b228e15b67adf6`  
		Last Modified: Thu, 03 Jul 2025 18:11:50 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a9f97258bff88a66c7d0799e1cca0168159476428196180dcb659145f73d5e`  
		Last Modified: Thu, 03 Jul 2025 18:12:00 GMT  
		Size: 79.0 MB (78970664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdad7988a9b22741b2289f955fef077117f4ad807a3beefc1675f7678a26661`  
		Last Modified: Thu, 03 Jul 2025 18:11:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2602f72de16bb4663944d1242b436d41dae5df4baa325999f8edc8fde9cfc04`  
		Last Modified: Thu, 03 Jul 2025 18:11:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:8c0a91af18f62e031e89b61ff6bc071eb36777896be769f9c91deee87e611c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431a0994b9672df8b2f95e5ec33eb7fdc203380417b687669898b2c2a36cf24e`

```dockerfile
```

-	Layers:
	-	`sha256:b8c2cd2346579d3f5d92615229e24bc81641f3f74fcde66fd036b7d0db75c627`  
		Last Modified: Thu, 03 Jul 2025 20:20:36 GMT  
		Size: 2.3 MB (2311303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250998b6caea34c1ff59f0a8aaddaadea842d3617256fccbf47477924ebc33ec`  
		Last Modified: Thu, 03 Jul 2025 20:20:37 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:25f576cfb27fa503e0b4faad047f2c06288e8c84709c767c598fa00d6c36a01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102895928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404f1926537a3c0ba8ae49f875ff9085f97f713e7e733801929816052f2e5135`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c0686a251b16fc8cbd211dd5bf5418ccc2bd75968ab247e18683ffb32d360e`  
		Last Modified: Wed, 02 Jul 2025 05:43:01 GMT  
		Size: 6.7 MB (6675401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929431d0f1ad953782d674eae05c259f14e0a696e1e97ac83b03b176f22ee189`  
		Last Modified: Wed, 02 Jul 2025 05:43:00 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be577860d3bf6727123bbc988af49989b1ea6badf2520371cc17e31e42d622a8`  
		Last Modified: Thu, 03 Jul 2025 18:22:49 GMT  
		Size: 67.4 MB (67360381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029eb551df41bdea62f1a9c5a6315f93da75ebef3b272dbe84313f1238d5aa71`  
		Last Modified: Thu, 03 Jul 2025 18:22:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282cd605924be4e43bce5a0c961910f7823978985772a79faa510fb1f50291d`  
		Last Modified: Thu, 03 Jul 2025 18:22:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4bf87fdcda35296f02175372f9085cab250d3ebef40c982fc66d4fd8935baba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9460a943d60135b3e7e1a8670fc6df2c4a22966d42a5837da4a60eaea5ecbb12`

```dockerfile
```

-	Layers:
	-	`sha256:4a85b56da49576a265c6a0d1a85eb01f35d9b5840c342eee33e9a6139707d1d8`  
		Last Modified: Thu, 03 Jul 2025 20:20:41 GMT  
		Size: 2.3 MB (2312385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f5d4006592fd4d12771b83c3d5c24b926c4d8b2d7308cad1377be05afbac57d`  
		Last Modified: Thu, 03 Jul 2025 20:20:42 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:eb5fc1d05cf0937c2fe97bb9ab45ca1b5e5a5ce2b1ee3377e88d5dd3a618a96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:51ca1c4c21da5d2f45cb25ceec61559c3919f9521802899d0f2b69d5a3a3cb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124839300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4274af6508e5531d0b5672323bf4180613ffe67b84b3d805f4ae8d4350c2729`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cbb8c7e407a8ed1b6742c78ccf99268ca9a9f4f9461e84334e010d0c3fc6b2`  
		Last Modified: Thu, 03 Jul 2025 18:11:46 GMT  
		Size: 6.7 MB (6664693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bb0d4c62c6f30adba13254138a7c0077325f2b344fec2292e156bf82b154aa`  
		Last Modified: Thu, 03 Jul 2025 18:11:46 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099a272d8885a7c27177e0fa1a5d81bc86b7651a6a6dc811fb2cde96465e7e8`  
		Last Modified: Thu, 03 Jul 2025 18:11:54 GMT  
		Size: 88.5 MB (88452114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fb1fe653059d8f57e6e6535e1b1ad39ac8494ed924ae53f87c13fcb7f93434`  
		Last Modified: Thu, 03 Jul 2025 18:11:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ececb2420e7b1089629603bd36c757aac77f2facdff3ce28a66e65f26f23dc0a`  
		Last Modified: Thu, 03 Jul 2025 18:11:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:da923ab8fb0d75f1062303f7b9fc90f73dc1a7d68fc4e2b7b7694212ca5dc303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d055ef4fc120adbb7f6a864e6fc03fe084719bec53966773d388607ac42f112`

```dockerfile
```

-	Layers:
	-	`sha256:b4bd134cf58714e89a7ab27d9bddec3abb746c70050479cddb0f8222854f4e28`  
		Last Modified: Thu, 03 Jul 2025 20:20:43 GMT  
		Size: 2.3 MB (2311351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b795e89f5b04e68672c789647d166c8674b392c335c79373207cbedfcc240fc3`  
		Last Modified: Thu, 03 Jul 2025 20:20:44 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0f3bf598b4dd54a2fef4810b0dc6a9a19dc9b346741698a490dcf62afca4a4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112051988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97200ea52b35f63f93e14a8266421e6b311ba9fae7c9fa09eea879e837b03f0`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c0686a251b16fc8cbd211dd5bf5418ccc2bd75968ab247e18683ffb32d360e`  
		Last Modified: Wed, 02 Jul 2025 05:43:01 GMT  
		Size: 6.7 MB (6675401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929431d0f1ad953782d674eae05c259f14e0a696e1e97ac83b03b176f22ee189`  
		Last Modified: Wed, 02 Jul 2025 05:43:00 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9aff82d27e2e354c914e8229bdae43752f746fcd3a5a0291347ee5f061861ce`  
		Last Modified: Thu, 03 Jul 2025 18:23:17 GMT  
		Size: 76.5 MB (76516437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235450b5238cc838f09d41e21f3fab325c9dd373696c57c26b34527b5a5e6a3`  
		Last Modified: Thu, 03 Jul 2025 18:23:10 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d438e265e8fcf90be481eff26217ea242fdbb36cc041c6c64c926e7e05a920`  
		Last Modified: Thu, 03 Jul 2025 18:23:10 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:c1cfcd19097d8a713d0addf17608c76e29943679bc9a6914edd4cb2e1c36eebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b187a0f2839da5fe6e87beda84f6078eb8be7bc4f710ea632b45e7919528d3ee`

```dockerfile
```

-	Layers:
	-	`sha256:d50396d28e52e16b20e21903203b11fd26f326edd525664c213a322ea376ec83`  
		Last Modified: Thu, 03 Jul 2025 20:20:48 GMT  
		Size: 2.3 MB (2312433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23062a068ca515ec8b7ce409eaea441db2c9781e141e1cd8ea2d62748bbf3a25`  
		Last Modified: Thu, 03 Jul 2025 20:20:48 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:b2766b01a99b4f10054e622df3a7f69cbe41c3722efbdb710f62072b7919ff49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:1fb5b939298bb8ffa728c163cdc5678bc6ee68a6dfde9f13a5507ac1d5cb6799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157213959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4355848b856f8acdc24412629625c7248439e5df15cd10a16bc48b884cb986e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 24 Jun 2025 22:21:26 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV GOSU_VER=1.16
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dba06387eee7a6a1867978ffb3eb271fba52c239bee86389de9766c6be503bb`  
		Last Modified: Tue, 01 Jul 2025 02:27:25 GMT  
		Size: 9.8 MB (9793900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251ae7b28987c8c3564d52c6eea8512558a0bc90a552b81cd6b134d5b8d8d7fa`  
		Last Modified: Tue, 01 Jul 2025 02:27:25 GMT  
		Size: 6.2 MB (6156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383d803099a2ac22de23042bf0b37804741628b7bf8071a89325ea088a25e316`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c622176d353333b2f9d79d771df07aee725480647e9403d20c9737655fa9b30b`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 1.0 MB (1006372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938f5ab719643314e090aa6ce65d9e50aead8cbfe6bc3a6af42482512c76e0d7`  
		Last Modified: Tue, 01 Jul 2025 02:27:29 GMT  
		Size: 100.2 MB (100242936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1233992fcb7a3053fe1e41b13effe04c6db0ad63472ce7d59e726dbd42f4619`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 11.8 MB (11773682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd863e2f53471dd98f640025131e115bdaffbcdcc2914ca22728fdfe1d50e664`  
		Last Modified: Tue, 01 Jul 2025 02:27:23 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01aa43ef8e9d4a982a027fbb398a3ea11e887e3c7813d7093775abdbdda1554`  
		Last Modified: Tue, 01 Jul 2025 02:27:23 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a289c46ced789334f801323191cef43221bb0a23cac3d77b416ef725ee5cbba4`  
		Last Modified: Tue, 01 Jul 2025 02:27:24 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:1ee7e90cf7b7806932034fa772c55c1c4affdabcb0be0c12c0e64e20033f3ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51086f996265644b7a88339580660b76b5f7612f4edfb2dd18699c68b56374b1`

```dockerfile
```

-	Layers:
	-	`sha256:fb6090f40047df8bd26e817f0be7c2815179f7afd9e5d7be2debe0fd1b8eb1de`  
		Last Modified: Tue, 01 Jul 2025 05:20:51 GMT  
		Size: 3.0 MB (2979773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfcc750a77001d29d4bdd252583fb42d41c9024aa9f4c38f00aa372a99cf3413`  
		Last Modified: Tue, 01 Jul 2025 05:20:52 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8e42ef527af5083ae810e246067b2a3f6aa2277e56918a93fb06bd46031140c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151541719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6324acffea320bef2041e9c6a62cf579b505411efd0beffdd02e0662d79e1f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 24 Jun 2025 22:21:26 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV GOSU_VER=1.16
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Jun 2025 22:21:26 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxd"]
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Jun 2025 22:21:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a9750ced17eb9680c39392299667138966b00b1b8ba9964360f165d34aae01`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 9.6 MB (9590213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e2c1dd6de92d4b17bd420e8296ec5ce8e0be197ae85866ce510089f56810f2`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c215e349bdf9c4c6bd41276069ce530b4a9d7773dc7b224fcfe4c3e09b9b6ac7`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f99d0a91ff766c668b657b3c945795c80020cb8d054ee697cf07674f6df903`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 936.1 KB (936103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c2fa4831c1b6a310ff1261e99f9b42d128151317b5f5eac991034a5ecb21d5`  
		Last Modified: Tue, 01 Jul 2025 07:16:41 GMT  
		Size: 96.0 MB (96038367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6def7749394d2ac8cb71787fa688047c89e3e5fef367537bab1a51ddf408bf`  
		Last Modified: Tue, 01 Jul 2025 07:16:37 GMT  
		Size: 11.1 MB (11098985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdc132259701de04ab9a4a64bb74425431c853ac20251882987c28a42a1d142`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034ec54bce93029ae930b80ea7e8dc06d7765dd5c473efdc32285b6eb3d6f803`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f046e46a8c615ae075557bb39ffc00094d3bf394f7ea9f46090669132b49b62`  
		Last Modified: Tue, 01 Jul 2025 07:16:36 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:513a8211cdaaadf97a7adebd2ae5488fd379582a4bcdd149b884b4f9885a0c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e99790d93b535aad6c085ddb5f618f53566efe13ac414605591664f4279e2df`

```dockerfile
```

-	Layers:
	-	`sha256:12fcca2d0f365ddd3e6c3bd5f0c280b02f6897514f3cd9212b3c5ae8e94b0e0a`  
		Last Modified: Tue, 01 Jul 2025 08:20:29 GMT  
		Size: 3.0 MB (2979001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a55c0cda549b8659bcccfae409e8f85910e7dc92523672c92ebc96c2e64d9b9`  
		Last Modified: Tue, 01 Jul 2025 08:20:30 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json
