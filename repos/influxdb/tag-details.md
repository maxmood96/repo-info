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
-	[`influxdb:3.2-core`](#influxdb32-core)
-	[`influxdb:3.2-enterprise`](#influxdb32-enterprise)
-	[`influxdb:3.2.0-core`](#influxdb320-core)
-	[`influxdb:3.2.0-enterprise`](#influxdb320-enterprise)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:core`](#influxdbcore)
-	[`influxdb:enterprise`](#influxdbenterprise)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:60728f32d8b40f5f61ea0e1ed13f4e7af8ca0df259b682b4607c050e3b4025d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:608b27fc814a84c730093be6344754d624adbfef1a487b831805228e302f637d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108963094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b08ed3a74d270be0328dccf725dec90032341b177f9db4da7b7060f9c81a70d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 28 May 2025 23:57:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f5a2b400e77595a25352cbbb004de89be487d5942f173809a7b60f6dbe6a57`  
		Last Modified: Wed, 11 Jun 2025 00:03:23 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35b06aad0f787a141f25ec3280b26742d8e37da8b7de04c05b9a44b3dbd11ee`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 39.4 MB (39439627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a88d9087f434984619cabdb9af6dd34c0d33b7e8942dd7b1a45dec92f74a4e`  
		Last Modified: Wed, 11 Jun 2025 00:03:23 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd5e5faac7f353cc3b1e59276810759cc1b34ff6c38ae8d3f7c15522234750c`  
		Last Modified: Wed, 11 Jun 2025 00:03:24 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395851d2c8ff6180733fce1961e910e805b8e3e78bb0dc9f7b22928fc0fdd895`  
		Last Modified: Wed, 11 Jun 2025 00:03:24 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:8639a100bd113e343ceae96d533922684ac8d7e546edecbd6221429f8b00e0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4799033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9cda7ef12431c00b43bb0c1fc0bab9a1eadf60b296bc74ff754d7d8243e5ab`

```dockerfile
```

-	Layers:
	-	`sha256:4a5b449965df287a90f81ac00a03d9ccbc08106160ee3112da5f90f1ead4d017`  
		Last Modified: Wed, 11 Jun 2025 02:20:20 GMT  
		Size: 4.8 MB (4784326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0076847b6cbe0ccf32e6e6632b648e1214b897af563e989a9bb8adcfd4ca40d1`  
		Last Modified: Wed, 11 Jun 2025 02:20:20 GMT  
		Size: 14.7 KB (14707 bytes)  
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
$ docker pull influxdb@sha256:bd1a3c73943a587e378229490bd1ef42920c1b135f5d227824310873c7a77c88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ff466f4a58e07fc802f6fcc720f505698e5d2df6ec259e3a43ba74a3bb05946d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88162298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3d90d215bf5d32157b54623efffded6eb2d24aaf8d25a07bedcd97499eb880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 28 May 2025 23:57:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ce83243f62d7de2c5083431d877ae6fbb154d6c3df9d429b8e9e9c1c328012`  
		Last Modified: Wed, 11 Jun 2025 00:03:24 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda847adfde156da0140ea2db160a6696e037c38abc745cc86e0ca051f4ad2f4`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 18.6 MB (18640040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f955faa8b4e91b5e59b5d8cbf938d0670d81bf3457027be22e7211548e903d`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5776be1c3ed940fc692169a85ba4cf50302171127032d3520b6274e918c98e61`  
		Last Modified: Wed, 11 Jun 2025 00:04:22 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:77ddc7f2354c095d3fe0dab2f8c577ff08fcaff17050252caa69e419c9e81890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915191da492cd3035da62790aa892f84dfc098316ea6bf036af545e9cd1f722f`

```dockerfile
```

-	Layers:
	-	`sha256:17d3cc737cb357845bc895a4825de10eb001b787bd121dc08f287802af85f761`  
		Last Modified: Wed, 11 Jun 2025 02:20:23 GMT  
		Size: 4.7 MB (4708306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe6d85f1cdb445f4225a5c65082d0026a3ea3416164cbb1934829b29e79a9dd9`  
		Last Modified: Wed, 11 Jun 2025 02:20:24 GMT  
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
$ docker pull influxdb@sha256:60728f32d8b40f5f61ea0e1ed13f4e7af8ca0df259b682b4607c050e3b4025d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:608b27fc814a84c730093be6344754d624adbfef1a487b831805228e302f637d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108963094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b08ed3a74d270be0328dccf725dec90032341b177f9db4da7b7060f9c81a70d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 28 May 2025 23:57:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f5a2b400e77595a25352cbbb004de89be487d5942f173809a7b60f6dbe6a57`  
		Last Modified: Wed, 11 Jun 2025 00:03:23 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35b06aad0f787a141f25ec3280b26742d8e37da8b7de04c05b9a44b3dbd11ee`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 39.4 MB (39439627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a88d9087f434984619cabdb9af6dd34c0d33b7e8942dd7b1a45dec92f74a4e`  
		Last Modified: Wed, 11 Jun 2025 00:03:23 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd5e5faac7f353cc3b1e59276810759cc1b34ff6c38ae8d3f7c15522234750c`  
		Last Modified: Wed, 11 Jun 2025 00:03:24 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395851d2c8ff6180733fce1961e910e805b8e3e78bb0dc9f7b22928fc0fdd895`  
		Last Modified: Wed, 11 Jun 2025 00:03:24 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:8639a100bd113e343ceae96d533922684ac8d7e546edecbd6221429f8b00e0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4799033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9cda7ef12431c00b43bb0c1fc0bab9a1eadf60b296bc74ff754d7d8243e5ab`

```dockerfile
```

-	Layers:
	-	`sha256:4a5b449965df287a90f81ac00a03d9ccbc08106160ee3112da5f90f1ead4d017`  
		Last Modified: Wed, 11 Jun 2025 02:20:20 GMT  
		Size: 4.8 MB (4784326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0076847b6cbe0ccf32e6e6632b648e1214b897af563e989a9bb8adcfd4ca40d1`  
		Last Modified: Wed, 11 Jun 2025 02:20:20 GMT  
		Size: 14.7 KB (14707 bytes)  
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
$ docker pull influxdb@sha256:bd1a3c73943a587e378229490bd1ef42920c1b135f5d227824310873c7a77c88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.10.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ff466f4a58e07fc802f6fcc720f505698e5d2df6ec259e3a43ba74a3bb05946d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88162298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3d90d215bf5d32157b54623efffded6eb2d24aaf8d25a07bedcd97499eb880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=1.10.8-c1.10.8
# Wed, 28 May 2025 23:57:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ce83243f62d7de2c5083431d877ae6fbb154d6c3df9d429b8e9e9c1c328012`  
		Last Modified: Wed, 11 Jun 2025 00:03:24 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda847adfde156da0140ea2db160a6696e037c38abc745cc86e0ca051f4ad2f4`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 18.6 MB (18640040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f955faa8b4e91b5e59b5d8cbf938d0670d81bf3457027be22e7211548e903d`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5776be1c3ed940fc692169a85ba4cf50302171127032d3520b6274e918c98e61`  
		Last Modified: Wed, 11 Jun 2025 00:04:22 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.10.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:77ddc7f2354c095d3fe0dab2f8c577ff08fcaff17050252caa69e419c9e81890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915191da492cd3035da62790aa892f84dfc098316ea6bf036af545e9cd1f722f`

```dockerfile
```

-	Layers:
	-	`sha256:17d3cc737cb357845bc895a4825de10eb001b787bd121dc08f287802af85f761`  
		Last Modified: Wed, 11 Jun 2025 02:20:23 GMT  
		Size: 4.7 MB (4708306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe6d85f1cdb445f4225a5c65082d0026a3ea3416164cbb1934829b29e79a9dd9`  
		Last Modified: Wed, 11 Jun 2025 02:20:24 GMT  
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
$ docker pull influxdb@sha256:aace6b543aacf580c9381692a49906959553bbdd1347b766f12acc65bdf23f21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:b006b75cf52b29a496dd23c6985696115f3728a9fa076009d4eabfe3d2c65568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116164407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79c3b8dd92df9bf24dc9eaa10b4f3060703913853973a218b921f1fb1a79814`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 28 May 2025 23:57:45 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3174229aa88ba904f8c7c6ebe57cb4df46efcc58a9116908aa71ce2bd68acef0`  
		Last Modified: Wed, 11 Jun 2025 00:02:55 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a99c0a1f958d1c015d7d741db213c88fec71c794c8f922d343507f8ad2c155`  
		Last Modified: Wed, 11 Jun 2025 00:02:58 GMT  
		Size: 43.7 MB (43651516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873581df8e55fd0caee6bccfe6bf1c860197a9133f8f4ee581d7b2c7b62f7e32`  
		Last Modified: Wed, 11 Jun 2025 00:02:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0941f1458a4d76fe06e2eada9efa9ae9573786f7f32d6d4ba445b6e87473fea8`  
		Last Modified: Wed, 11 Jun 2025 00:02:56 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56016ebac4f6157aa0d9122c02045e51e83b679a3431023bb5d04cd475b9c985`  
		Last Modified: Wed, 11 Jun 2025 00:02:57 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:70ca1db1b78498374bca6690c910ea50daccd018d15831e4f7010eca87dd9717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2a017a20597e85690db101c5ffa550bf640be60fe6ead07956b9abc75c2d06`

```dockerfile
```

-	Layers:
	-	`sha256:de59fd11a983d7012511ecaa98ae43f4ad948f8c0745cc7e48750f93cdf2218d`  
		Last Modified: Wed, 11 Jun 2025 02:20:31 GMT  
		Size: 5.1 MB (5070491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc21da0f4d0f5e213ef2a9feb2c3b147aae9fb348200b09f974f2c51272420c`  
		Last Modified: Wed, 11 Jun 2025 02:20:32 GMT  
		Size: 15.5 KB (15528 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:48bba2043f162bd8ca610cfba4d2d179c8a012c78caab1ca8933fc71aca9a3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113012646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c79449d2cedcc8e06df49c735c132ba08c167478170276f01cf64467bc02ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 28 May 2025 23:57:45 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1309232b479a9d5f2bdfbde9894b400212a8d25c43f575ef4111b3d431163a9`  
		Last Modified: Wed, 11 Jun 2025 10:51:15 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b739a8fd6dbac7945fc8ac35a557b56ade123667e2a84f1220cb251c8b7bc3`  
		Last Modified: Wed, 11 Jun 2025 10:51:24 GMT  
		Size: 41.1 MB (41119323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe297e74bedf130faa0c8f620fc5a66beac132201b7a1f959baa7dd70d1be13`  
		Last Modified: Wed, 11 Jun 2025 10:51:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1aba98624ebff66717887c9368b4c8bcdcbbcd09eb76693a5ee3f029bc302b8`  
		Last Modified: Wed, 11 Jun 2025 10:51:16 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c429c3f0fc9d3c28ec1667f1989910bd0d13dbe51cd9d86949159bb136c4a9`  
		Last Modified: Wed, 11 Jun 2025 10:51:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:93e73fdfe9a97f01fcbfbde84f94fcdbe907b1923dbb94a49c10d523f5e96bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11126d1e40fe2f1d77b92bfe0c4e14244f3fc2b7fd40953fd73ee236c69c2b35`

```dockerfile
```

-	Layers:
	-	`sha256:b8932e86fff512727dd9e340bba22680614ba288cd2149b98f54cb7e0af23902`  
		Last Modified: Wed, 11 Jun 2025 11:20:24 GMT  
		Size: 5.1 MB (5069956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:872639be7e3fdc811964be670b5abd1a9a39a0c8c4769817bba9038518ae2af3`  
		Last Modified: Wed, 11 Jun 2025 11:20:25 GMT  
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
$ docker pull influxdb@sha256:f74ffd7954e42d394a11e8d13ce1054d41744133320051dc1df66c33c54da182
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f9852d37755b5df2d421d5b899073dc811924a6f9cf3e907e313fce76c7ec49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111692835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9c087fcf288954dce99fa5473936fc7d5804c9dad31167e42de7e77462d8a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Wed, 28 May 2025 23:57:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9fb00e073db4ff686c284eca0193ac9db2d52b46453dcd4a876caa336b12f7`  
		Last Modified: Wed, 11 Jun 2025 01:35:51 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af09512cb173d1e6ed08a38067e692c22ab91afca5b9ece2a503224d362f27e`  
		Last Modified: Wed, 11 Jun 2025 03:23:19 GMT  
		Size: 39.2 MB (39179294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1388aa92a648f7f6ff87a6d82e33650135ad6fe3c264b5707c39116b17641ee8`  
		Last Modified: Wed, 11 Jun 2025 01:35:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b767955b47ef56c4a2eea7284b4e336362ee51a59279e88820be5fe67e63b32`  
		Last Modified: Wed, 11 Jun 2025 01:35:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce7ecc0eaf7058b4f8677219bcd16515e38939f542e32edee2de7711fc83c71`  
		Last Modified: Wed, 11 Jun 2025 01:36:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:99992b71862bf0db3c117460d5a4faccc32a8bd47ff981ef065fce09b707d5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4674376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5762e318ece8dbeea768f97c9eaaa88b1731d84a44873b0eeb8525ea13148364`

```dockerfile
```

-	Layers:
	-	`sha256:c182a464a709277600a61cff9ea478a1617148d0e0558f0ed37cafd48afdd933`  
		Last Modified: Wed, 11 Jun 2025 02:20:36 GMT  
		Size: 4.7 MB (4659668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83ea0aa593afbeb4dea3cbdbe3061222f519f685f7a8e8fd5c318a20c85878f`  
		Last Modified: Wed, 11 Jun 2025 02:20:37 GMT  
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
$ docker pull influxdb@sha256:8b61ab2f6b27ce4816219adfc3b103d7bce32c0bb1d8c9ecdb49b24c09159171
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:00ba6992c69444ccc7da9f13f8bb6cfb1cd4998200fb867e61c53dcaf42f055e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90848862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151925a1164d6f5231645c6cc017c86fe330cf3a6df1e7d090bafeefdbe89d82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Wed, 28 May 2025 23:57:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccf76a31877d302fa442f21a3104c50b5042241fc78942768e2788248e65e15`  
		Last Modified: Wed, 11 Jun 2025 01:35:49 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505180a1c989663d135e78774c23c8369e6a4b7f4e168f5a447896b93f8249a5`  
		Last Modified: Wed, 11 Jun 2025 03:22:50 GMT  
		Size: 18.3 MB (18336545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4e1f85f3c99ea55b85cafa5c073638e1a53ef654ef8ec70083c8e955923713`  
		Last Modified: Wed, 11 Jun 2025 01:35:54 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cc21fa8eb175b4e6db114fe313fce4e1c364f6a84642238502313eabe2efcb`  
		Last Modified: Wed, 11 Jun 2025 01:35:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:25753df2653b889928e0febfed5e4e4134a93287c66bdf5d8e31fac7d70e84dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4597706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84eb7652cf527299db2bab8f392f3062eaeaac1d4c94865621247d83c95954f3`

```dockerfile
```

-	Layers:
	-	`sha256:88bb02144a0053a5c067a5ffa0e932e645aa4a661686ba8e8ac184671f420c28`  
		Last Modified: Wed, 11 Jun 2025 02:20:40 GMT  
		Size: 4.6 MB (4584639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8c3e68ba24af6cbd918d1191835d651260854a1cfb354bf07adf4b21dfb8411`  
		Last Modified: Wed, 11 Jun 2025 02:20:41 GMT  
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
$ docker pull influxdb@sha256:aace6b543aacf580c9381692a49906959553bbdd1347b766f12acc65bdf23f21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:b006b75cf52b29a496dd23c6985696115f3728a9fa076009d4eabfe3d2c65568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116164407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79c3b8dd92df9bf24dc9eaa10b4f3060703913853973a218b921f1fb1a79814`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 28 May 2025 23:57:45 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3174229aa88ba904f8c7c6ebe57cb4df46efcc58a9116908aa71ce2bd68acef0`  
		Last Modified: Wed, 11 Jun 2025 00:02:55 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a99c0a1f958d1c015d7d741db213c88fec71c794c8f922d343507f8ad2c155`  
		Last Modified: Wed, 11 Jun 2025 00:02:58 GMT  
		Size: 43.7 MB (43651516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873581df8e55fd0caee6bccfe6bf1c860197a9133f8f4ee581d7b2c7b62f7e32`  
		Last Modified: Wed, 11 Jun 2025 00:02:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0941f1458a4d76fe06e2eada9efa9ae9573786f7f32d6d4ba445b6e87473fea8`  
		Last Modified: Wed, 11 Jun 2025 00:02:56 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56016ebac4f6157aa0d9122c02045e51e83b679a3431023bb5d04cd475b9c985`  
		Last Modified: Wed, 11 Jun 2025 00:02:57 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:70ca1db1b78498374bca6690c910ea50daccd018d15831e4f7010eca87dd9717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2a017a20597e85690db101c5ffa550bf640be60fe6ead07956b9abc75c2d06`

```dockerfile
```

-	Layers:
	-	`sha256:de59fd11a983d7012511ecaa98ae43f4ad948f8c0745cc7e48750f93cdf2218d`  
		Last Modified: Wed, 11 Jun 2025 02:20:31 GMT  
		Size: 5.1 MB (5070491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc21da0f4d0f5e213ef2a9feb2c3b147aae9fb348200b09f974f2c51272420c`  
		Last Modified: Wed, 11 Jun 2025 02:20:32 GMT  
		Size: 15.5 KB (15528 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:48bba2043f162bd8ca610cfba4d2d179c8a012c78caab1ca8933fc71aca9a3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113012646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c79449d2cedcc8e06df49c735c132ba08c167478170276f01cf64467bc02ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 28 May 2025 23:57:45 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1309232b479a9d5f2bdfbde9894b400212a8d25c43f575ef4111b3d431163a9`  
		Last Modified: Wed, 11 Jun 2025 10:51:15 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b739a8fd6dbac7945fc8ac35a557b56ade123667e2a84f1220cb251c8b7bc3`  
		Last Modified: Wed, 11 Jun 2025 10:51:24 GMT  
		Size: 41.1 MB (41119323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe297e74bedf130faa0c8f620fc5a66beac132201b7a1f959baa7dd70d1be13`  
		Last Modified: Wed, 11 Jun 2025 10:51:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1aba98624ebff66717887c9368b4c8bcdcbbcd09eb76693a5ee3f029bc302b8`  
		Last Modified: Wed, 11 Jun 2025 10:51:16 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c429c3f0fc9d3c28ec1667f1989910bd0d13dbe51cd9d86949159bb136c4a9`  
		Last Modified: Wed, 11 Jun 2025 10:51:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:93e73fdfe9a97f01fcbfbde84f94fcdbe907b1923dbb94a49c10d523f5e96bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11126d1e40fe2f1d77b92bfe0c4e14244f3fc2b7fd40953fd73ee236c69c2b35`

```dockerfile
```

-	Layers:
	-	`sha256:b8932e86fff512727dd9e340bba22680614ba288cd2149b98f54cb7e0af23902`  
		Last Modified: Wed, 11 Jun 2025 11:20:24 GMT  
		Size: 5.1 MB (5069956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:872639be7e3fdc811964be670b5abd1a9a39a0c8c4769817bba9038518ae2af3`  
		Last Modified: Wed, 11 Jun 2025 11:20:25 GMT  
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
$ docker pull influxdb@sha256:f74ffd7954e42d394a11e8d13ce1054d41744133320051dc1df66c33c54da182
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:f9852d37755b5df2d421d5b899073dc811924a6f9cf3e907e313fce76c7ec49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111692835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9c087fcf288954dce99fa5473936fc7d5804c9dad31167e42de7e77462d8a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Wed, 28 May 2025 23:57:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9fb00e073db4ff686c284eca0193ac9db2d52b46453dcd4a876caa336b12f7`  
		Last Modified: Wed, 11 Jun 2025 01:35:51 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af09512cb173d1e6ed08a38067e692c22ab91afca5b9ece2a503224d362f27e`  
		Last Modified: Wed, 11 Jun 2025 03:23:19 GMT  
		Size: 39.2 MB (39179294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1388aa92a648f7f6ff87a6d82e33650135ad6fe3c264b5707c39116b17641ee8`  
		Last Modified: Wed, 11 Jun 2025 01:35:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b767955b47ef56c4a2eea7284b4e336362ee51a59279e88820be5fe67e63b32`  
		Last Modified: Wed, 11 Jun 2025 01:35:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce7ecc0eaf7058b4f8677219bcd16515e38939f542e32edee2de7711fc83c71`  
		Last Modified: Wed, 11 Jun 2025 01:36:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:99992b71862bf0db3c117460d5a4faccc32a8bd47ff981ef065fce09b707d5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4674376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5762e318ece8dbeea768f97c9eaaa88b1731d84a44873b0eeb8525ea13148364`

```dockerfile
```

-	Layers:
	-	`sha256:c182a464a709277600a61cff9ea478a1617148d0e0558f0ed37cafd48afdd933`  
		Last Modified: Wed, 11 Jun 2025 02:20:36 GMT  
		Size: 4.7 MB (4659668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83ea0aa593afbeb4dea3cbdbe3061222f519f685f7a8e8fd5c318a20c85878f`  
		Last Modified: Wed, 11 Jun 2025 02:20:37 GMT  
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
$ docker pull influxdb@sha256:8b61ab2f6b27ce4816219adfc3b103d7bce32c0bb1d8c9ecdb49b24c09159171
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:00ba6992c69444ccc7da9f13f8bb6cfb1cd4998200fb867e61c53dcaf42f055e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90848862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151925a1164d6f5231645c6cc017c86fe330cf3a6df1e7d090bafeefdbe89d82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=1.11.8-c1.11.8
# Wed, 28 May 2025 23:57:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccf76a31877d302fa442f21a3104c50b5042241fc78942768e2788248e65e15`  
		Last Modified: Wed, 11 Jun 2025 01:35:49 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505180a1c989663d135e78774c23c8369e6a4b7f4e168f5a447896b93f8249a5`  
		Last Modified: Wed, 11 Jun 2025 03:22:50 GMT  
		Size: 18.3 MB (18336545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4e1f85f3c99ea55b85cafa5c073638e1a53ef654ef8ec70083c8e955923713`  
		Last Modified: Wed, 11 Jun 2025 01:35:54 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cc21fa8eb175b4e6db114fe313fce4e1c364f6a84642238502313eabe2efcb`  
		Last Modified: Wed, 11 Jun 2025 01:35:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:25753df2653b889928e0febfed5e4e4134a93287c66bdf5d8e31fac7d70e84dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4597706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84eb7652cf527299db2bab8f392f3062eaeaac1d4c94865621247d83c95954f3`

```dockerfile
```

-	Layers:
	-	`sha256:88bb02144a0053a5c067a5ffa0e932e645aa4a661686ba8e8ac184671f420c28`  
		Last Modified: Wed, 11 Jun 2025 02:20:40 GMT  
		Size: 4.6 MB (4584639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8c3e68ba24af6cbd918d1191835d651260854a1cfb354bf07adf4b21dfb8411`  
		Last Modified: Wed, 11 Jun 2025 02:20:41 GMT  
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
$ docker pull influxdb@sha256:d842befa8acabf6058b2e4833e3881391758c3dc6f15f526c8bd8d0b9efa86a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:2bf12cb9c1694340910f4b78738c3dafa9c7c73f42d8358c62e15167a0e507c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157214021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f46b35e028d32dccd333286eedfa8503ec72be31caa641bf41fa10bba04639f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a15f767b95bfe505c34c2c9c4612b132afb64c43f91299bf765a451e44ada9`  
		Last Modified: Thu, 26 Jun 2025 00:42:21 GMT  
		Size: 9.8 MB (9793935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410301d34bc785036a559865ff2153e09b5e5693d855bc8645f82227958ec1e5`  
		Last Modified: Wed, 25 Jun 2025 23:44:36 GMT  
		Size: 6.2 MB (6156983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c75afb199a82bb477f5b9411ca25503e4f19f5e2f8ca6ea99850e754520eb0`  
		Last Modified: Wed, 25 Jun 2025 23:44:34 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ad991a9b4afb9beb319565f9430a57033e73ed35feb0757ade713828b2628d`  
		Last Modified: Wed, 25 Jun 2025 23:44:35 GMT  
		Size: 1.0 MB (1006364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0cec84d26999cd681e4978bec705a9011633d965454b4ed803996684c3c92a`  
		Last Modified: Thu, 26 Jun 2025 00:42:44 GMT  
		Size: 100.2 MB (100242978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78b9902efb2b3ac12445b3c0b46745365b908b098c7a3c86cd4141f4013062e`  
		Last Modified: Wed, 25 Jun 2025 23:44:40 GMT  
		Size: 11.8 MB (11773678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e36a659fa926701de1463a75fca912c9acd84c2f687a33933ffe12e308b7172`  
		Last Modified: Wed, 25 Jun 2025 23:44:34 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4f31eeb21504efef8670614dcdf3268c4a334eaa90c6b7000b891612cb4f5a`  
		Last Modified: Wed, 25 Jun 2025 23:44:36 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edd93dae8da571cb169d57f2ccade9dbf0501a0b099262cf293f375a194ec32`  
		Last Modified: Wed, 25 Jun 2025 23:44:36 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:c32148c1288bd54f064e666562468d83ebf531195d7b6132744c2abb3a8b935b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b95a94956bc5f017f52ecc7dd43ac29aef6eb311ac450a1a1849c9a256ab5f`

```dockerfile
```

-	Layers:
	-	`sha256:16a999f723cece768ea953c3ab45d77681dde665bab724cd454d399705580d6f`  
		Last Modified: Thu, 26 Jun 2025 02:20:27 GMT  
		Size: 3.0 MB (2979773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2214c063ee86101b35912244ae19a3e2b4336790117de8854b8ba0a12ff27cbc`  
		Last Modified: Thu, 26 Jun 2025 02:20:28 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:05a9e597cb6bd926997cb5de1e2da8593ad5d200527a1ec27916ef19854f2b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151541748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2232fdc606edeb9aa338e7acf7c713d251ae52c30936fe31154e2b944e395b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d1adeaee6ad42884f03696f1a8d7957f1407d81bab077ff433ad058deb12b4`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 9.6 MB (9590212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e608cc4c6bfb98dc5899af5cba06a260e46c7db0a4a06d3417f77405f4866f`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 5.8 MB (5790426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca9df937c5329bac6cdc5cea28a5633057eb7161bcdbc217a937eecf19d383`  
		Last Modified: Thu, 26 Jun 2025 04:33:16 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fb10e1d39fc8b7fef29c721f497fec0912fa5aa9200fac9c2921e6fc3a4e32`  
		Last Modified: Thu, 26 Jun 2025 04:33:16 GMT  
		Size: 936.1 KB (936109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af306c5421d00e649d0ec6cbf4ff43b0eb236ebaeeadaccc59482033b9b1cb5`  
		Last Modified: Thu, 26 Jun 2025 04:33:27 GMT  
		Size: 96.0 MB (96038392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7642fd79d9a7197ad9a2ac9f379b2ba07589c66c6c3a6f5f98ea07d78f06e23b`  
		Last Modified: Thu, 26 Jun 2025 04:33:18 GMT  
		Size: 11.1 MB (11098977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126aa653fd120d5dcd2bb8fbbba893b94a74bb79a24298de9e26e70f53a75eb`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25056ab1c476ba142dcfcb4458d77e52d31c63bce5658862f2e2dd77281394da`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3391f59b468948a00967f49c0eca665926ac1e4d65b120797ae8a4a2fe343656`  
		Last Modified: Thu, 26 Jun 2025 04:33:18 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:f7f99f78c3d2bb450955a9c460d9238bb6cff36698e3b3f9ac62e0a7fd60c08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d841afeaf46fc45c1cef9b882cbf199df4cb46c52a590924d26f26098ac65c8`

```dockerfile
```

-	Layers:
	-	`sha256:5d8e8a4cbef84d00153117316e54412170c746a255d0952b382e85dafca13fd8`  
		Last Modified: Thu, 26 Jun 2025 05:20:28 GMT  
		Size: 3.0 MB (2979001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dacc99db9be479885adc48cf53bee3823da392ba1281af7f4f49e6139499ce5`  
		Last Modified: Thu, 26 Jun 2025 05:20:29 GMT  
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
$ docker pull influxdb@sha256:d842befa8acabf6058b2e4833e3881391758c3dc6f15f526c8bd8d0b9efa86a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:2bf12cb9c1694340910f4b78738c3dafa9c7c73f42d8358c62e15167a0e507c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157214021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f46b35e028d32dccd333286eedfa8503ec72be31caa641bf41fa10bba04639f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a15f767b95bfe505c34c2c9c4612b132afb64c43f91299bf765a451e44ada9`  
		Last Modified: Thu, 26 Jun 2025 00:42:21 GMT  
		Size: 9.8 MB (9793935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410301d34bc785036a559865ff2153e09b5e5693d855bc8645f82227958ec1e5`  
		Last Modified: Wed, 25 Jun 2025 23:44:36 GMT  
		Size: 6.2 MB (6156983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c75afb199a82bb477f5b9411ca25503e4f19f5e2f8ca6ea99850e754520eb0`  
		Last Modified: Wed, 25 Jun 2025 23:44:34 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ad991a9b4afb9beb319565f9430a57033e73ed35feb0757ade713828b2628d`  
		Last Modified: Wed, 25 Jun 2025 23:44:35 GMT  
		Size: 1.0 MB (1006364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0cec84d26999cd681e4978bec705a9011633d965454b4ed803996684c3c92a`  
		Last Modified: Thu, 26 Jun 2025 00:42:44 GMT  
		Size: 100.2 MB (100242978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78b9902efb2b3ac12445b3c0b46745365b908b098c7a3c86cd4141f4013062e`  
		Last Modified: Wed, 25 Jun 2025 23:44:40 GMT  
		Size: 11.8 MB (11773678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e36a659fa926701de1463a75fca912c9acd84c2f687a33933ffe12e308b7172`  
		Last Modified: Wed, 25 Jun 2025 23:44:34 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4f31eeb21504efef8670614dcdf3268c4a334eaa90c6b7000b891612cb4f5a`  
		Last Modified: Wed, 25 Jun 2025 23:44:36 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edd93dae8da571cb169d57f2ccade9dbf0501a0b099262cf293f375a194ec32`  
		Last Modified: Wed, 25 Jun 2025 23:44:36 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:c32148c1288bd54f064e666562468d83ebf531195d7b6132744c2abb3a8b935b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b95a94956bc5f017f52ecc7dd43ac29aef6eb311ac450a1a1849c9a256ab5f`

```dockerfile
```

-	Layers:
	-	`sha256:16a999f723cece768ea953c3ab45d77681dde665bab724cd454d399705580d6f`  
		Last Modified: Thu, 26 Jun 2025 02:20:27 GMT  
		Size: 3.0 MB (2979773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2214c063ee86101b35912244ae19a3e2b4336790117de8854b8ba0a12ff27cbc`  
		Last Modified: Thu, 26 Jun 2025 02:20:28 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:05a9e597cb6bd926997cb5de1e2da8593ad5d200527a1ec27916ef19854f2b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151541748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2232fdc606edeb9aa338e7acf7c713d251ae52c30936fe31154e2b944e395b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d1adeaee6ad42884f03696f1a8d7957f1407d81bab077ff433ad058deb12b4`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 9.6 MB (9590212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e608cc4c6bfb98dc5899af5cba06a260e46c7db0a4a06d3417f77405f4866f`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 5.8 MB (5790426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca9df937c5329bac6cdc5cea28a5633057eb7161bcdbc217a937eecf19d383`  
		Last Modified: Thu, 26 Jun 2025 04:33:16 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fb10e1d39fc8b7fef29c721f497fec0912fa5aa9200fac9c2921e6fc3a4e32`  
		Last Modified: Thu, 26 Jun 2025 04:33:16 GMT  
		Size: 936.1 KB (936109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af306c5421d00e649d0ec6cbf4ff43b0eb236ebaeeadaccc59482033b9b1cb5`  
		Last Modified: Thu, 26 Jun 2025 04:33:27 GMT  
		Size: 96.0 MB (96038392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7642fd79d9a7197ad9a2ac9f379b2ba07589c66c6c3a6f5f98ea07d78f06e23b`  
		Last Modified: Thu, 26 Jun 2025 04:33:18 GMT  
		Size: 11.1 MB (11098977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126aa653fd120d5dcd2bb8fbbba893b94a74bb79a24298de9e26e70f53a75eb`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25056ab1c476ba142dcfcb4458d77e52d31c63bce5658862f2e2dd77281394da`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3391f59b468948a00967f49c0eca665926ac1e4d65b120797ae8a4a2fe343656`  
		Last Modified: Thu, 26 Jun 2025 04:33:18 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:f7f99f78c3d2bb450955a9c460d9238bb6cff36698e3b3f9ac62e0a7fd60c08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d841afeaf46fc45c1cef9b882cbf199df4cb46c52a590924d26f26098ac65c8`

```dockerfile
```

-	Layers:
	-	`sha256:5d8e8a4cbef84d00153117316e54412170c746a255d0952b382e85dafca13fd8`  
		Last Modified: Thu, 26 Jun 2025 05:20:28 GMT  
		Size: 3.0 MB (2979001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dacc99db9be479885adc48cf53bee3823da392ba1281af7f4f49e6139499ce5`  
		Last Modified: Thu, 26 Jun 2025 05:20:29 GMT  
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

## `influxdb:2.7.11-alpine`

```console
$ docker pull influxdb@sha256:ef14203d7014ac9a0df4f087d186901ea7d19993410b35782f6c3c421738eb25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.11-alpine` - linux; amd64

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

### `influxdb:2.7.11-alpine` - unknown; unknown

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

### `influxdb:2.7.11-alpine` - linux; arm64 variant v8

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

### `influxdb:2.7.11-alpine` - unknown; unknown

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
$ docker pull influxdb@sha256:d842befa8acabf6058b2e4833e3881391758c3dc6f15f526c8bd8d0b9efa86a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:2bf12cb9c1694340910f4b78738c3dafa9c7c73f42d8358c62e15167a0e507c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157214021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f46b35e028d32dccd333286eedfa8503ec72be31caa641bf41fa10bba04639f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a15f767b95bfe505c34c2c9c4612b132afb64c43f91299bf765a451e44ada9`  
		Last Modified: Thu, 26 Jun 2025 00:42:21 GMT  
		Size: 9.8 MB (9793935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410301d34bc785036a559865ff2153e09b5e5693d855bc8645f82227958ec1e5`  
		Last Modified: Wed, 25 Jun 2025 23:44:36 GMT  
		Size: 6.2 MB (6156983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c75afb199a82bb477f5b9411ca25503e4f19f5e2f8ca6ea99850e754520eb0`  
		Last Modified: Wed, 25 Jun 2025 23:44:34 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ad991a9b4afb9beb319565f9430a57033e73ed35feb0757ade713828b2628d`  
		Last Modified: Wed, 25 Jun 2025 23:44:35 GMT  
		Size: 1.0 MB (1006364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0cec84d26999cd681e4978bec705a9011633d965454b4ed803996684c3c92a`  
		Last Modified: Thu, 26 Jun 2025 00:42:44 GMT  
		Size: 100.2 MB (100242978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78b9902efb2b3ac12445b3c0b46745365b908b098c7a3c86cd4141f4013062e`  
		Last Modified: Wed, 25 Jun 2025 23:44:40 GMT  
		Size: 11.8 MB (11773678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e36a659fa926701de1463a75fca912c9acd84c2f687a33933ffe12e308b7172`  
		Last Modified: Wed, 25 Jun 2025 23:44:34 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4f31eeb21504efef8670614dcdf3268c4a334eaa90c6b7000b891612cb4f5a`  
		Last Modified: Wed, 25 Jun 2025 23:44:36 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edd93dae8da571cb169d57f2ccade9dbf0501a0b099262cf293f375a194ec32`  
		Last Modified: Wed, 25 Jun 2025 23:44:36 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:c32148c1288bd54f064e666562468d83ebf531195d7b6132744c2abb3a8b935b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b95a94956bc5f017f52ecc7dd43ac29aef6eb311ac450a1a1849c9a256ab5f`

```dockerfile
```

-	Layers:
	-	`sha256:16a999f723cece768ea953c3ab45d77681dde665bab724cd454d399705580d6f`  
		Last Modified: Thu, 26 Jun 2025 02:20:27 GMT  
		Size: 3.0 MB (2979773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2214c063ee86101b35912244ae19a3e2b4336790117de8854b8ba0a12ff27cbc`  
		Last Modified: Thu, 26 Jun 2025 02:20:28 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:05a9e597cb6bd926997cb5de1e2da8593ad5d200527a1ec27916ef19854f2b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151541748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2232fdc606edeb9aa338e7acf7c713d251ae52c30936fe31154e2b944e395b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d1adeaee6ad42884f03696f1a8d7957f1407d81bab077ff433ad058deb12b4`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 9.6 MB (9590212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e608cc4c6bfb98dc5899af5cba06a260e46c7db0a4a06d3417f77405f4866f`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 5.8 MB (5790426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca9df937c5329bac6cdc5cea28a5633057eb7161bcdbc217a937eecf19d383`  
		Last Modified: Thu, 26 Jun 2025 04:33:16 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fb10e1d39fc8b7fef29c721f497fec0912fa5aa9200fac9c2921e6fc3a4e32`  
		Last Modified: Thu, 26 Jun 2025 04:33:16 GMT  
		Size: 936.1 KB (936109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af306c5421d00e649d0ec6cbf4ff43b0eb236ebaeeadaccc59482033b9b1cb5`  
		Last Modified: Thu, 26 Jun 2025 04:33:27 GMT  
		Size: 96.0 MB (96038392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7642fd79d9a7197ad9a2ac9f379b2ba07589c66c6c3a6f5f98ea07d78f06e23b`  
		Last Modified: Thu, 26 Jun 2025 04:33:18 GMT  
		Size: 11.1 MB (11098977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126aa653fd120d5dcd2bb8fbbba893b94a74bb79a24298de9e26e70f53a75eb`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25056ab1c476ba142dcfcb4458d77e52d31c63bce5658862f2e2dd77281394da`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3391f59b468948a00967f49c0eca665926ac1e4d65b120797ae8a4a2fe343656`  
		Last Modified: Thu, 26 Jun 2025 04:33:18 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:f7f99f78c3d2bb450955a9c460d9238bb6cff36698e3b3f9ac62e0a7fd60c08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d841afeaf46fc45c1cef9b882cbf199df4cb46c52a590924d26f26098ac65c8`

```dockerfile
```

-	Layers:
	-	`sha256:5d8e8a4cbef84d00153117316e54412170c746a255d0952b382e85dafca13fd8`  
		Last Modified: Thu, 26 Jun 2025 05:20:28 GMT  
		Size: 3.0 MB (2979001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dacc99db9be479885adc48cf53bee3823da392ba1281af7f4f49e6139499ce5`  
		Last Modified: Thu, 26 Jun 2025 05:20:29 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:3241bdea61f11a8cd2c5362d385e6cb2d6ae210316ce7b53163336438eeb1384
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:a131d9f1c4f0ce64eb75b1d819314af21b3fe27dbf59d15fb5419d53291c99df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115496475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ae9aee4fe2d8350a22e78d6ab2f19259c8c1c1b98697517d65d677d9481054`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d839de8123910559c17fd4ba04234a5fb4a9241bce929872e51cd03f11718b`  
		Last Modified: Wed, 25 Jun 2025 23:44:37 GMT  
		Size: 6.7 MB (6664730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91d914566b0df26404488318d48fa579bcedaf412ab6437994463f5e6132a15`  
		Last Modified: Wed, 25 Jun 2025 23:44:38 GMT  
		Size: 3.7 KB (3660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30c7413af1573a636305809441f3689db75df9fca5556fda40ec05aa7968c33`  
		Last Modified: Thu, 26 Jun 2025 02:25:27 GMT  
		Size: 79.1 MB (79112274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26bc7b42ee8cf97a4c546d5ab7cc1e236f4aa7cae018c075b04345219ad81a4`  
		Last Modified: Wed, 25 Jun 2025 23:44:39 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bb46401c29ef322381cb69df539ced8230fa243c8d47008718d3743d760b75`  
		Last Modified: Wed, 25 Jun 2025 23:44:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5c6c3f676eefbc4ddc5f17b3f54c08f8b5665f074e0b64a9d3d2547b4ed60369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11261149df86edc102aa7137db374f9ade4e25df1af455056c57ae4a2bbb9e99`

```dockerfile
```

-	Layers:
	-	`sha256:017d1be51c8ab31609d711f44c9db08cdbf25f36a198bf8150091d68779f0bd5`  
		Last Modified: Thu, 26 Jun 2025 02:20:41 GMT  
		Size: 2.3 MB (2311303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7fdcaa8c961ac2e813e33d5901eb369032c365d4ad33420f1217f37c624f1b0`  
		Last Modified: Thu, 26 Jun 2025 02:20:42 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d16471b253b7d7fef24d9d0b08d1961189ec09bd878c496d680c71ac1d15109e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102950204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e1e3fb26520eda68f4820c083980d47890f54a24756787b144601514a2aa8d`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8865f22a9e785041ccdb0b89712516696e6058fc239ad761649cea02268bb`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 6.7 MB (6675504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fee5000f4705f155ccdb4b21078827c33cfb92f34fba3aac8bbecf2883738d1`  
		Last Modified: Thu, 26 Jun 2025 04:34:30 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7122b41864ae672fba7fd1a94e1edbe0e20bfcbbfe2ca5af7cb318943eec7a`  
		Last Modified: Thu, 26 Jun 2025 04:34:38 GMT  
		Size: 67.4 MB (67418671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c1c2aa26c973141d04d86c4fc0876c693986ff1620d150065f67afc4fb8837`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ef1534ef1ff85dc41eacbc5c9b875db5e758c70a0d3ffef2920fa7b4cb926c`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:9f2207d8e1fe929febe1ebadb0d9ced8fa210d371ac187927ad2fee9dc491f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f934353057a03ce35cc9438993498e5de850700e04c3b7279629806642dac0e`

```dockerfile
```

-	Layers:
	-	`sha256:ec7736f9daaf2b0a7682d856e2c5f2a56c8759751a819b748902891ca09dc3ea`  
		Last Modified: Thu, 26 Jun 2025 05:20:42 GMT  
		Size: 2.3 MB (2312385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46faa1c5d7afb9c93f59113abd21e65373f571c2ef2c81afa20f054b3960ecfc`  
		Last Modified: Thu, 26 Jun 2025 05:20:42 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:3933869b7ad21c38247d9d2d968651340a2f413705c97f1bbf59e4fadbe3fb33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:f747cdbf501d9edd6b117f446021c57fffa4fdb352bad1b4553932984ad62589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124931597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc37247b58a411215f9b0c2c7981a6d13a22716382167f4b4dad7c622ff4ce99`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06072e83ea7225c4a9248c4e2e3f6bc5093d6739501852069e03df78b249bd83`  
		Last Modified: Thu, 26 Jun 2025 02:44:08 GMT  
		Size: 6.7 MB (6664764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fee9bab9d13314c295c89b7dab8b38fb644d24b3d1a53942cbabab6a5b65ce`  
		Last Modified: Wed, 25 Jun 2025 23:44:42 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4689bdea511ca93b17a2c2cbf63ef0aab13099a2386e563d3569c66c41e5301e`  
		Last Modified: Thu, 26 Jun 2025 02:44:43 GMT  
		Size: 88.5 MB (88547365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c4d577f121bd8ecead36a8245423eccecdd6a9e0141f4ad8361b86f7536090`  
		Last Modified: Wed, 25 Jun 2025 23:44:42 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f8755e2a2151a1490bb871c774485542d6c16a0d5dbddc3e1f3fe5a7753965`  
		Last Modified: Wed, 25 Jun 2025 23:44:42 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:297b17f088099fd22751f3cd0b7ea369b352476b30d479e22d7aa7de1ef53c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d66c0a607a245ea6d3ed0cdfa097b394dd64284a30aa738a264dd4819462024`

```dockerfile
```

-	Layers:
	-	`sha256:068b5d803ea973b1db5db52c195e23936dd358b2424f5b0c172e7417ad2ca9e2`  
		Last Modified: Thu, 26 Jun 2025 02:20:45 GMT  
		Size: 2.3 MB (2311351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a33cfa4c08cb9b714961954f6a9decc13d8242a8961b110603f2b5b001bbd3b`  
		Last Modified: Thu, 26 Jun 2025 02:20:46 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4331461b8c04f0d95a221dffd78c61d91efca8d93576e34507c90361cbf15dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112216551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71b6484b37d70e2a8b2ef506c8c8ac3c05c6e970f7a97afbbd919284ac47d54`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8865f22a9e785041ccdb0b89712516696e6058fc239ad761649cea02268bb`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 6.7 MB (6675504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fee5000f4705f155ccdb4b21078827c33cfb92f34fba3aac8bbecf2883738d1`  
		Last Modified: Thu, 26 Jun 2025 04:34:30 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5697b34ed3c8e40eb7ca448b8b6f3a1287641bdeb59c1ae03b015d758b7c503`  
		Last Modified: Thu, 26 Jun 2025 09:14:29 GMT  
		Size: 76.7 MB (76685017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749660ef26019bd746d181b1002e3d4030d6f438f574062e17fc112615a38619`  
		Last Modified: Thu, 26 Jun 2025 04:35:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a058bd28b7792df049771f75172f4ad4cf0eb5b95daa058901bf8cc1f686ab40`  
		Last Modified: Thu, 26 Jun 2025 04:35:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:ec745999e4b527a2c01e457a8cadaec83d85a2ed8b0f97773f05248c60712a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9e6d31b22c5b2c4dc07d2f35c3c40d9dc912207d9d89d784edd9bfeaf1e0d7`

```dockerfile
```

-	Layers:
	-	`sha256:da0bbcf690ffc25271756a7196a72bc366135b6d1b2d7a54a81b4b95f579105c`  
		Last Modified: Thu, 26 Jun 2025 05:20:45 GMT  
		Size: 2.3 MB (2312433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e86880ed582b5ba9500071839f1aa2f28d5e18f2d6db287ff5a6efc27c2267f`  
		Last Modified: Thu, 26 Jun 2025 05:20:46 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.2-core`

```console
$ docker pull influxdb@sha256:3241bdea61f11a8cd2c5362d385e6cb2d6ae210316ce7b53163336438eeb1384
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.2-core` - linux; amd64

```console
$ docker pull influxdb@sha256:a131d9f1c4f0ce64eb75b1d819314af21b3fe27dbf59d15fb5419d53291c99df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115496475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ae9aee4fe2d8350a22e78d6ab2f19259c8c1c1b98697517d65d677d9481054`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d839de8123910559c17fd4ba04234a5fb4a9241bce929872e51cd03f11718b`  
		Last Modified: Wed, 25 Jun 2025 23:44:37 GMT  
		Size: 6.7 MB (6664730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91d914566b0df26404488318d48fa579bcedaf412ab6437994463f5e6132a15`  
		Last Modified: Wed, 25 Jun 2025 23:44:38 GMT  
		Size: 3.7 KB (3660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30c7413af1573a636305809441f3689db75df9fca5556fda40ec05aa7968c33`  
		Last Modified: Thu, 26 Jun 2025 02:25:27 GMT  
		Size: 79.1 MB (79112274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26bc7b42ee8cf97a4c546d5ab7cc1e236f4aa7cae018c075b04345219ad81a4`  
		Last Modified: Wed, 25 Jun 2025 23:44:39 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bb46401c29ef322381cb69df539ced8230fa243c8d47008718d3743d760b75`  
		Last Modified: Wed, 25 Jun 2025 23:44:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5c6c3f676eefbc4ddc5f17b3f54c08f8b5665f074e0b64a9d3d2547b4ed60369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11261149df86edc102aa7137db374f9ade4e25df1af455056c57ae4a2bbb9e99`

```dockerfile
```

-	Layers:
	-	`sha256:017d1be51c8ab31609d711f44c9db08cdbf25f36a198bf8150091d68779f0bd5`  
		Last Modified: Thu, 26 Jun 2025 02:20:41 GMT  
		Size: 2.3 MB (2311303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7fdcaa8c961ac2e813e33d5901eb369032c365d4ad33420f1217f37c624f1b0`  
		Last Modified: Thu, 26 Jun 2025 02:20:42 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.2-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d16471b253b7d7fef24d9d0b08d1961189ec09bd878c496d680c71ac1d15109e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102950204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e1e3fb26520eda68f4820c083980d47890f54a24756787b144601514a2aa8d`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8865f22a9e785041ccdb0b89712516696e6058fc239ad761649cea02268bb`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 6.7 MB (6675504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fee5000f4705f155ccdb4b21078827c33cfb92f34fba3aac8bbecf2883738d1`  
		Last Modified: Thu, 26 Jun 2025 04:34:30 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7122b41864ae672fba7fd1a94e1edbe0e20bfcbbfe2ca5af7cb318943eec7a`  
		Last Modified: Thu, 26 Jun 2025 04:34:38 GMT  
		Size: 67.4 MB (67418671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c1c2aa26c973141d04d86c4fc0876c693986ff1620d150065f67afc4fb8837`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ef1534ef1ff85dc41eacbc5c9b875db5e758c70a0d3ffef2920fa7b4cb926c`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:9f2207d8e1fe929febe1ebadb0d9ced8fa210d371ac187927ad2fee9dc491f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f934353057a03ce35cc9438993498e5de850700e04c3b7279629806642dac0e`

```dockerfile
```

-	Layers:
	-	`sha256:ec7736f9daaf2b0a7682d856e2c5f2a56c8759751a819b748902891ca09dc3ea`  
		Last Modified: Thu, 26 Jun 2025 05:20:42 GMT  
		Size: 2.3 MB (2312385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46faa1c5d7afb9c93f59113abd21e65373f571c2ef2c81afa20f054b3960ecfc`  
		Last Modified: Thu, 26 Jun 2025 05:20:42 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.2-enterprise`

```console
$ docker pull influxdb@sha256:3933869b7ad21c38247d9d2d968651340a2f413705c97f1bbf59e4fadbe3fb33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.2-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:f747cdbf501d9edd6b117f446021c57fffa4fdb352bad1b4553932984ad62589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124931597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc37247b58a411215f9b0c2c7981a6d13a22716382167f4b4dad7c622ff4ce99`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06072e83ea7225c4a9248c4e2e3f6bc5093d6739501852069e03df78b249bd83`  
		Last Modified: Thu, 26 Jun 2025 02:44:08 GMT  
		Size: 6.7 MB (6664764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fee9bab9d13314c295c89b7dab8b38fb644d24b3d1a53942cbabab6a5b65ce`  
		Last Modified: Wed, 25 Jun 2025 23:44:42 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4689bdea511ca93b17a2c2cbf63ef0aab13099a2386e563d3569c66c41e5301e`  
		Last Modified: Thu, 26 Jun 2025 02:44:43 GMT  
		Size: 88.5 MB (88547365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c4d577f121bd8ecead36a8245423eccecdd6a9e0141f4ad8361b86f7536090`  
		Last Modified: Wed, 25 Jun 2025 23:44:42 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f8755e2a2151a1490bb871c774485542d6c16a0d5dbddc3e1f3fe5a7753965`  
		Last Modified: Wed, 25 Jun 2025 23:44:42 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:297b17f088099fd22751f3cd0b7ea369b352476b30d479e22d7aa7de1ef53c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d66c0a607a245ea6d3ed0cdfa097b394dd64284a30aa738a264dd4819462024`

```dockerfile
```

-	Layers:
	-	`sha256:068b5d803ea973b1db5db52c195e23936dd358b2424f5b0c172e7417ad2ca9e2`  
		Last Modified: Thu, 26 Jun 2025 02:20:45 GMT  
		Size: 2.3 MB (2311351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a33cfa4c08cb9b714961954f6a9decc13d8242a8961b110603f2b5b001bbd3b`  
		Last Modified: Thu, 26 Jun 2025 02:20:46 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.2-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4331461b8c04f0d95a221dffd78c61d91efca8d93576e34507c90361cbf15dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112216551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71b6484b37d70e2a8b2ef506c8c8ac3c05c6e970f7a97afbbd919284ac47d54`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8865f22a9e785041ccdb0b89712516696e6058fc239ad761649cea02268bb`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 6.7 MB (6675504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fee5000f4705f155ccdb4b21078827c33cfb92f34fba3aac8bbecf2883738d1`  
		Last Modified: Thu, 26 Jun 2025 04:34:30 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5697b34ed3c8e40eb7ca448b8b6f3a1287641bdeb59c1ae03b015d758b7c503`  
		Last Modified: Thu, 26 Jun 2025 09:14:29 GMT  
		Size: 76.7 MB (76685017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749660ef26019bd746d181b1002e3d4030d6f438f574062e17fc112615a38619`  
		Last Modified: Thu, 26 Jun 2025 04:35:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a058bd28b7792df049771f75172f4ad4cf0eb5b95daa058901bf8cc1f686ab40`  
		Last Modified: Thu, 26 Jun 2025 04:35:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:ec745999e4b527a2c01e457a8cadaec83d85a2ed8b0f97773f05248c60712a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9e6d31b22c5b2c4dc07d2f35c3c40d9dc912207d9d89d784edd9bfeaf1e0d7`

```dockerfile
```

-	Layers:
	-	`sha256:da0bbcf690ffc25271756a7196a72bc366135b6d1b2d7a54a81b4b95f579105c`  
		Last Modified: Thu, 26 Jun 2025 05:20:45 GMT  
		Size: 2.3 MB (2312433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e86880ed582b5ba9500071839f1aa2f28d5e18f2d6db287ff5a6efc27c2267f`  
		Last Modified: Thu, 26 Jun 2025 05:20:46 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.2.0-core`

```console
$ docker pull influxdb@sha256:3241bdea61f11a8cd2c5362d385e6cb2d6ae210316ce7b53163336438eeb1384
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.2.0-core` - linux; amd64

```console
$ docker pull influxdb@sha256:a131d9f1c4f0ce64eb75b1d819314af21b3fe27dbf59d15fb5419d53291c99df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115496475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ae9aee4fe2d8350a22e78d6ab2f19259c8c1c1b98697517d65d677d9481054`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d839de8123910559c17fd4ba04234a5fb4a9241bce929872e51cd03f11718b`  
		Last Modified: Wed, 25 Jun 2025 23:44:37 GMT  
		Size: 6.7 MB (6664730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91d914566b0df26404488318d48fa579bcedaf412ab6437994463f5e6132a15`  
		Last Modified: Wed, 25 Jun 2025 23:44:38 GMT  
		Size: 3.7 KB (3660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30c7413af1573a636305809441f3689db75df9fca5556fda40ec05aa7968c33`  
		Last Modified: Thu, 26 Jun 2025 02:25:27 GMT  
		Size: 79.1 MB (79112274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26bc7b42ee8cf97a4c546d5ab7cc1e236f4aa7cae018c075b04345219ad81a4`  
		Last Modified: Wed, 25 Jun 2025 23:44:39 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bb46401c29ef322381cb69df539ced8230fa243c8d47008718d3743d760b75`  
		Last Modified: Wed, 25 Jun 2025 23:44:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5c6c3f676eefbc4ddc5f17b3f54c08f8b5665f074e0b64a9d3d2547b4ed60369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11261149df86edc102aa7137db374f9ade4e25df1af455056c57ae4a2bbb9e99`

```dockerfile
```

-	Layers:
	-	`sha256:017d1be51c8ab31609d711f44c9db08cdbf25f36a198bf8150091d68779f0bd5`  
		Last Modified: Thu, 26 Jun 2025 02:20:41 GMT  
		Size: 2.3 MB (2311303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7fdcaa8c961ac2e813e33d5901eb369032c365d4ad33420f1217f37c624f1b0`  
		Last Modified: Thu, 26 Jun 2025 02:20:42 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.2.0-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d16471b253b7d7fef24d9d0b08d1961189ec09bd878c496d680c71ac1d15109e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102950204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e1e3fb26520eda68f4820c083980d47890f54a24756787b144601514a2aa8d`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8865f22a9e785041ccdb0b89712516696e6058fc239ad761649cea02268bb`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 6.7 MB (6675504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fee5000f4705f155ccdb4b21078827c33cfb92f34fba3aac8bbecf2883738d1`  
		Last Modified: Thu, 26 Jun 2025 04:34:30 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7122b41864ae672fba7fd1a94e1edbe0e20bfcbbfe2ca5af7cb318943eec7a`  
		Last Modified: Thu, 26 Jun 2025 04:34:38 GMT  
		Size: 67.4 MB (67418671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c1c2aa26c973141d04d86c4fc0876c693986ff1620d150065f67afc4fb8837`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ef1534ef1ff85dc41eacbc5c9b875db5e758c70a0d3ffef2920fa7b4cb926c`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:9f2207d8e1fe929febe1ebadb0d9ced8fa210d371ac187927ad2fee9dc491f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f934353057a03ce35cc9438993498e5de850700e04c3b7279629806642dac0e`

```dockerfile
```

-	Layers:
	-	`sha256:ec7736f9daaf2b0a7682d856e2c5f2a56c8759751a819b748902891ca09dc3ea`  
		Last Modified: Thu, 26 Jun 2025 05:20:42 GMT  
		Size: 2.3 MB (2312385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46faa1c5d7afb9c93f59113abd21e65373f571c2ef2c81afa20f054b3960ecfc`  
		Last Modified: Thu, 26 Jun 2025 05:20:42 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.2.0-enterprise`

```console
$ docker pull influxdb@sha256:3933869b7ad21c38247d9d2d968651340a2f413705c97f1bbf59e4fadbe3fb33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.2.0-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:f747cdbf501d9edd6b117f446021c57fffa4fdb352bad1b4553932984ad62589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124931597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc37247b58a411215f9b0c2c7981a6d13a22716382167f4b4dad7c622ff4ce99`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06072e83ea7225c4a9248c4e2e3f6bc5093d6739501852069e03df78b249bd83`  
		Last Modified: Thu, 26 Jun 2025 02:44:08 GMT  
		Size: 6.7 MB (6664764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fee9bab9d13314c295c89b7dab8b38fb644d24b3d1a53942cbabab6a5b65ce`  
		Last Modified: Wed, 25 Jun 2025 23:44:42 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4689bdea511ca93b17a2c2cbf63ef0aab13099a2386e563d3569c66c41e5301e`  
		Last Modified: Thu, 26 Jun 2025 02:44:43 GMT  
		Size: 88.5 MB (88547365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c4d577f121bd8ecead36a8245423eccecdd6a9e0141f4ad8361b86f7536090`  
		Last Modified: Wed, 25 Jun 2025 23:44:42 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f8755e2a2151a1490bb871c774485542d6c16a0d5dbddc3e1f3fe5a7753965`  
		Last Modified: Wed, 25 Jun 2025 23:44:42 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:297b17f088099fd22751f3cd0b7ea369b352476b30d479e22d7aa7de1ef53c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d66c0a607a245ea6d3ed0cdfa097b394dd64284a30aa738a264dd4819462024`

```dockerfile
```

-	Layers:
	-	`sha256:068b5d803ea973b1db5db52c195e23936dd358b2424f5b0c172e7417ad2ca9e2`  
		Last Modified: Thu, 26 Jun 2025 02:20:45 GMT  
		Size: 2.3 MB (2311351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a33cfa4c08cb9b714961954f6a9decc13d8242a8961b110603f2b5b001bbd3b`  
		Last Modified: Thu, 26 Jun 2025 02:20:46 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.2.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4331461b8c04f0d95a221dffd78c61d91efca8d93576e34507c90361cbf15dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112216551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71b6484b37d70e2a8b2ef506c8c8ac3c05c6e970f7a97afbbd919284ac47d54`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8865f22a9e785041ccdb0b89712516696e6058fc239ad761649cea02268bb`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 6.7 MB (6675504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fee5000f4705f155ccdb4b21078827c33cfb92f34fba3aac8bbecf2883738d1`  
		Last Modified: Thu, 26 Jun 2025 04:34:30 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5697b34ed3c8e40eb7ca448b8b6f3a1287641bdeb59c1ae03b015d758b7c503`  
		Last Modified: Thu, 26 Jun 2025 09:14:29 GMT  
		Size: 76.7 MB (76685017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749660ef26019bd746d181b1002e3d4030d6f438f574062e17fc112615a38619`  
		Last Modified: Thu, 26 Jun 2025 04:35:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a058bd28b7792df049771f75172f4ad4cf0eb5b95daa058901bf8cc1f686ab40`  
		Last Modified: Thu, 26 Jun 2025 04:35:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.2.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:ec745999e4b527a2c01e457a8cadaec83d85a2ed8b0f97773f05248c60712a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9e6d31b22c5b2c4dc07d2f35c3c40d9dc912207d9d89d784edd9bfeaf1e0d7`

```dockerfile
```

-	Layers:
	-	`sha256:da0bbcf690ffc25271756a7196a72bc366135b6d1b2d7a54a81b4b95f579105c`  
		Last Modified: Thu, 26 Jun 2025 05:20:45 GMT  
		Size: 2.3 MB (2312433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e86880ed582b5ba9500071839f1aa2f28d5e18f2d6db287ff5a6efc27c2267f`  
		Last Modified: Thu, 26 Jun 2025 05:20:46 GMT  
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
$ docker pull influxdb@sha256:3241bdea61f11a8cd2c5362d385e6cb2d6ae210316ce7b53163336438eeb1384
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:a131d9f1c4f0ce64eb75b1d819314af21b3fe27dbf59d15fb5419d53291c99df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115496475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ae9aee4fe2d8350a22e78d6ab2f19259c8c1c1b98697517d65d677d9481054`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d839de8123910559c17fd4ba04234a5fb4a9241bce929872e51cd03f11718b`  
		Last Modified: Wed, 25 Jun 2025 23:44:37 GMT  
		Size: 6.7 MB (6664730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91d914566b0df26404488318d48fa579bcedaf412ab6437994463f5e6132a15`  
		Last Modified: Wed, 25 Jun 2025 23:44:38 GMT  
		Size: 3.7 KB (3660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30c7413af1573a636305809441f3689db75df9fca5556fda40ec05aa7968c33`  
		Last Modified: Thu, 26 Jun 2025 02:25:27 GMT  
		Size: 79.1 MB (79112274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26bc7b42ee8cf97a4c546d5ab7cc1e236f4aa7cae018c075b04345219ad81a4`  
		Last Modified: Wed, 25 Jun 2025 23:44:39 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bb46401c29ef322381cb69df539ced8230fa243c8d47008718d3743d760b75`  
		Last Modified: Wed, 25 Jun 2025 23:44:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5c6c3f676eefbc4ddc5f17b3f54c08f8b5665f074e0b64a9d3d2547b4ed60369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11261149df86edc102aa7137db374f9ade4e25df1af455056c57ae4a2bbb9e99`

```dockerfile
```

-	Layers:
	-	`sha256:017d1be51c8ab31609d711f44c9db08cdbf25f36a198bf8150091d68779f0bd5`  
		Last Modified: Thu, 26 Jun 2025 02:20:41 GMT  
		Size: 2.3 MB (2311303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7fdcaa8c961ac2e813e33d5901eb369032c365d4ad33420f1217f37c624f1b0`  
		Last Modified: Thu, 26 Jun 2025 02:20:42 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d16471b253b7d7fef24d9d0b08d1961189ec09bd878c496d680c71ac1d15109e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102950204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e1e3fb26520eda68f4820c083980d47890f54a24756787b144601514a2aa8d`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8865f22a9e785041ccdb0b89712516696e6058fc239ad761649cea02268bb`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 6.7 MB (6675504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fee5000f4705f155ccdb4b21078827c33cfb92f34fba3aac8bbecf2883738d1`  
		Last Modified: Thu, 26 Jun 2025 04:34:30 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7122b41864ae672fba7fd1a94e1edbe0e20bfcbbfe2ca5af7cb318943eec7a`  
		Last Modified: Thu, 26 Jun 2025 04:34:38 GMT  
		Size: 67.4 MB (67418671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c1c2aa26c973141d04d86c4fc0876c693986ff1620d150065f67afc4fb8837`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ef1534ef1ff85dc41eacbc5c9b875db5e758c70a0d3ffef2920fa7b4cb926c`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:9f2207d8e1fe929febe1ebadb0d9ced8fa210d371ac187927ad2fee9dc491f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f934353057a03ce35cc9438993498e5de850700e04c3b7279629806642dac0e`

```dockerfile
```

-	Layers:
	-	`sha256:ec7736f9daaf2b0a7682d856e2c5f2a56c8759751a819b748902891ca09dc3ea`  
		Last Modified: Thu, 26 Jun 2025 05:20:42 GMT  
		Size: 2.3 MB (2312385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46faa1c5d7afb9c93f59113abd21e65373f571c2ef2c81afa20f054b3960ecfc`  
		Last Modified: Thu, 26 Jun 2025 05:20:42 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:3933869b7ad21c38247d9d2d968651340a2f413705c97f1bbf59e4fadbe3fb33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:f747cdbf501d9edd6b117f446021c57fffa4fdb352bad1b4553932984ad62589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124931597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc37247b58a411215f9b0c2c7981a6d13a22716382167f4b4dad7c622ff4ce99`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06072e83ea7225c4a9248c4e2e3f6bc5093d6739501852069e03df78b249bd83`  
		Last Modified: Thu, 26 Jun 2025 02:44:08 GMT  
		Size: 6.7 MB (6664764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fee9bab9d13314c295c89b7dab8b38fb644d24b3d1a53942cbabab6a5b65ce`  
		Last Modified: Wed, 25 Jun 2025 23:44:42 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4689bdea511ca93b17a2c2cbf63ef0aab13099a2386e563d3569c66c41e5301e`  
		Last Modified: Thu, 26 Jun 2025 02:44:43 GMT  
		Size: 88.5 MB (88547365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c4d577f121bd8ecead36a8245423eccecdd6a9e0141f4ad8361b86f7536090`  
		Last Modified: Wed, 25 Jun 2025 23:44:42 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f8755e2a2151a1490bb871c774485542d6c16a0d5dbddc3e1f3fe5a7753965`  
		Last Modified: Wed, 25 Jun 2025 23:44:42 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:297b17f088099fd22751f3cd0b7ea369b352476b30d479e22d7aa7de1ef53c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d66c0a607a245ea6d3ed0cdfa097b394dd64284a30aa738a264dd4819462024`

```dockerfile
```

-	Layers:
	-	`sha256:068b5d803ea973b1db5db52c195e23936dd358b2424f5b0c172e7417ad2ca9e2`  
		Last Modified: Thu, 26 Jun 2025 02:20:45 GMT  
		Size: 2.3 MB (2311351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a33cfa4c08cb9b714961954f6a9decc13d8242a8961b110603f2b5b001bbd3b`  
		Last Modified: Thu, 26 Jun 2025 02:20:46 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4331461b8c04f0d95a221dffd78c61d91efca8d93576e34507c90361cbf15dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112216551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71b6484b37d70e2a8b2ef506c8c8ac3c05c6e970f7a97afbbd919284ac47d54`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8865f22a9e785041ccdb0b89712516696e6058fc239ad761649cea02268bb`  
		Last Modified: Thu, 26 Jun 2025 04:34:31 GMT  
		Size: 6.7 MB (6675504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fee5000f4705f155ccdb4b21078827c33cfb92f34fba3aac8bbecf2883738d1`  
		Last Modified: Thu, 26 Jun 2025 04:34:30 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5697b34ed3c8e40eb7ca448b8b6f3a1287641bdeb59c1ae03b015d758b7c503`  
		Last Modified: Thu, 26 Jun 2025 09:14:29 GMT  
		Size: 76.7 MB (76685017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749660ef26019bd746d181b1002e3d4030d6f438f574062e17fc112615a38619`  
		Last Modified: Thu, 26 Jun 2025 04:35:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a058bd28b7792df049771f75172f4ad4cf0eb5b95daa058901bf8cc1f686ab40`  
		Last Modified: Thu, 26 Jun 2025 04:35:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:ec745999e4b527a2c01e457a8cadaec83d85a2ed8b0f97773f05248c60712a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9e6d31b22c5b2c4dc07d2f35c3c40d9dc912207d9d89d784edd9bfeaf1e0d7`

```dockerfile
```

-	Layers:
	-	`sha256:da0bbcf690ffc25271756a7196a72bc366135b6d1b2d7a54a81b4b95f579105c`  
		Last Modified: Thu, 26 Jun 2025 05:20:45 GMT  
		Size: 2.3 MB (2312433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e86880ed582b5ba9500071839f1aa2f28d5e18f2d6db287ff5a6efc27c2267f`  
		Last Modified: Thu, 26 Jun 2025 05:20:46 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:d842befa8acabf6058b2e4833e3881391758c3dc6f15f526c8bd8d0b9efa86a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:2bf12cb9c1694340910f4b78738c3dafa9c7c73f42d8358c62e15167a0e507c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157214021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f46b35e028d32dccd333286eedfa8503ec72be31caa641bf41fa10bba04639f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a15f767b95bfe505c34c2c9c4612b132afb64c43f91299bf765a451e44ada9`  
		Last Modified: Thu, 26 Jun 2025 00:42:21 GMT  
		Size: 9.8 MB (9793935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410301d34bc785036a559865ff2153e09b5e5693d855bc8645f82227958ec1e5`  
		Last Modified: Wed, 25 Jun 2025 23:44:36 GMT  
		Size: 6.2 MB (6156983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c75afb199a82bb477f5b9411ca25503e4f19f5e2f8ca6ea99850e754520eb0`  
		Last Modified: Wed, 25 Jun 2025 23:44:34 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ad991a9b4afb9beb319565f9430a57033e73ed35feb0757ade713828b2628d`  
		Last Modified: Wed, 25 Jun 2025 23:44:35 GMT  
		Size: 1.0 MB (1006364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0cec84d26999cd681e4978bec705a9011633d965454b4ed803996684c3c92a`  
		Last Modified: Thu, 26 Jun 2025 00:42:44 GMT  
		Size: 100.2 MB (100242978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78b9902efb2b3ac12445b3c0b46745365b908b098c7a3c86cd4141f4013062e`  
		Last Modified: Wed, 25 Jun 2025 23:44:40 GMT  
		Size: 11.8 MB (11773678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e36a659fa926701de1463a75fca912c9acd84c2f687a33933ffe12e308b7172`  
		Last Modified: Wed, 25 Jun 2025 23:44:34 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4f31eeb21504efef8670614dcdf3268c4a334eaa90c6b7000b891612cb4f5a`  
		Last Modified: Wed, 25 Jun 2025 23:44:36 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edd93dae8da571cb169d57f2ccade9dbf0501a0b099262cf293f375a194ec32`  
		Last Modified: Wed, 25 Jun 2025 23:44:36 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:c32148c1288bd54f064e666562468d83ebf531195d7b6132744c2abb3a8b935b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b95a94956bc5f017f52ecc7dd43ac29aef6eb311ac450a1a1849c9a256ab5f`

```dockerfile
```

-	Layers:
	-	`sha256:16a999f723cece768ea953c3ab45d77681dde665bab724cd454d399705580d6f`  
		Last Modified: Thu, 26 Jun 2025 02:20:27 GMT  
		Size: 3.0 MB (2979773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2214c063ee86101b35912244ae19a3e2b4336790117de8854b8ba0a12ff27cbc`  
		Last Modified: Thu, 26 Jun 2025 02:20:28 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:05a9e597cb6bd926997cb5de1e2da8593ad5d200527a1ec27916ef19854f2b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151541748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2232fdc606edeb9aa338e7acf7c713d251ae52c30936fe31154e2b944e395b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d1adeaee6ad42884f03696f1a8d7957f1407d81bab077ff433ad058deb12b4`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 9.6 MB (9590212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e608cc4c6bfb98dc5899af5cba06a260e46c7db0a4a06d3417f77405f4866f`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 5.8 MB (5790426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca9df937c5329bac6cdc5cea28a5633057eb7161bcdbc217a937eecf19d383`  
		Last Modified: Thu, 26 Jun 2025 04:33:16 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fb10e1d39fc8b7fef29c721f497fec0912fa5aa9200fac9c2921e6fc3a4e32`  
		Last Modified: Thu, 26 Jun 2025 04:33:16 GMT  
		Size: 936.1 KB (936109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af306c5421d00e649d0ec6cbf4ff43b0eb236ebaeeadaccc59482033b9b1cb5`  
		Last Modified: Thu, 26 Jun 2025 04:33:27 GMT  
		Size: 96.0 MB (96038392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7642fd79d9a7197ad9a2ac9f379b2ba07589c66c6c3a6f5f98ea07d78f06e23b`  
		Last Modified: Thu, 26 Jun 2025 04:33:18 GMT  
		Size: 11.1 MB (11098977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126aa653fd120d5dcd2bb8fbbba893b94a74bb79a24298de9e26e70f53a75eb`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25056ab1c476ba142dcfcb4458d77e52d31c63bce5658862f2e2dd77281394da`  
		Last Modified: Thu, 26 Jun 2025 04:33:17 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3391f59b468948a00967f49c0eca665926ac1e4d65b120797ae8a4a2fe343656`  
		Last Modified: Thu, 26 Jun 2025 04:33:18 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:f7f99f78c3d2bb450955a9c460d9238bb6cff36698e3b3f9ac62e0a7fd60c08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d841afeaf46fc45c1cef9b882cbf199df4cb46c52a590924d26f26098ac65c8`

```dockerfile
```

-	Layers:
	-	`sha256:5d8e8a4cbef84d00153117316e54412170c746a255d0952b382e85dafca13fd8`  
		Last Modified: Thu, 26 Jun 2025 05:20:28 GMT  
		Size: 3.0 MB (2979001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dacc99db9be479885adc48cf53bee3823da392ba1281af7f4f49e6139499ce5`  
		Last Modified: Thu, 26 Jun 2025 05:20:29 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json
