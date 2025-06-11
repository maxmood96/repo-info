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
$ docker pull influxdb@sha256:633f90c555c590c0ad9b73040deac0d47e85570bd5c6e83d855c8e77e3723662
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
$ docker pull influxdb@sha256:633f90c555c590c0ad9b73040deac0d47e85570bd5c6e83d855c8e77e3723662
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
$ docker pull influxdb@sha256:fac6ceeca56efc0d97f4a3b22f1c474eb04b6bef570de0264180490e5d3631f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:09742cb64d69a379823ce21c03bd73c1818738cbd69e03b98c107a6918912648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168647686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c599907d80e3d19592504a41f766714f68d762e9dade6ccaa148896b8cb9b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV GOSU_VER=1.16
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 May 2025 23:57:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 May 2025 23:57:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781d4bc0b622264c3b95a002a659e1fd52d7c866443ab2bb61086ef36bfa628a`  
		Last Modified: Wed, 11 Jun 2025 00:27:15 GMT  
		Size: 9.8 MB (9790978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c13825d3e5797e42d23cd10193a1975c7a342fb65a1a140bbf9e3a1942de55b`  
		Last Modified: Wed, 11 Jun 2025 00:27:14 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccbd15a33d1df4cb152d05cfe92fb4d9612886aeb6b87c8aeaac1e23c981ef4`  
		Last Modified: Wed, 11 Jun 2025 00:09:37 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb6b7e49268f149c50757d6496bc7a72d312bce887b0ae6a5d92270bb4acff4`  
		Last Modified: Wed, 11 Jun 2025 00:09:41 GMT  
		Size: 1.0 MB (1006369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e3eae90cf98ee2ed4269e1d08bf34423f33e5a48019464eae48ae1da4ca721`  
		Last Modified: Wed, 11 Jun 2025 00:27:29 GMT  
		Size: 100.2 MB (100242937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cbf8839cb30c0c6cee94987f6edc4e38a0f4c261ffc4ea98bbe0d5dc20a3db`  
		Last Modified: Wed, 11 Jun 2025 00:27:23 GMT  
		Size: 23.5 MB (23546398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bef2790a8c2912e900047217f4411a8aa44a8f6f0967ee97674bee7c0b727e`  
		Last Modified: Wed, 11 Jun 2025 00:09:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa292f7f47619d3e17da9c791e2afba84d8386b527f9a4aed795c5ea36f754e`  
		Last Modified: Wed, 11 Jun 2025 00:09:50 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1101a98020eb8ba562010bb3d105e6a599482e247790af299298a01b2bcb24ac`  
		Last Modified: Wed, 11 Jun 2025 00:09:54 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:90399b48251b3a383055062e0e6b988d41716ce14316fed5a25b6c7dffde36f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3021422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa49386252bbf3a01b40220df62ff98f7f201dc73d4422eae7d9c12ca515d19f`

```dockerfile
```

-	Layers:
	-	`sha256:982fed0043621e4127b99462ff4dea32ea851f6dc964c1cdec297c5bccfba768`  
		Last Modified: Wed, 11 Jun 2025 02:20:49 GMT  
		Size: 3.0 MB (2987604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d9a20fc4b1df79fb9f905cf01c080fc3b585f3475e65eac544c837ba6dc754`  
		Last Modified: Wed, 11 Jun 2025 02:20:50 GMT  
		Size: 33.8 KB (33818 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2734c55f3973993cb937802f40110bc334abc6f61689e80f5437f1e180358766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162312532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066584d55a104c2d3c8bebee98e4b5e3d8c53a63b40d6d886f423189d89748ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV GOSU_VER=1.16
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 May 2025 23:57:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 May 2025 23:57:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1338d636b55bf40227a68fad20cc20a12b4eb561002dfed9d4a9d832a2ad5dec`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 9.6 MB (9588706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c99ce16ececd1df586c43abb732624912826a6957ea184635dc5e43ab58487`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 5.5 MB (5463800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b84852bd30ce95f8cb21262ca216b153313cd6864182247e4c245f2ad84fdd0`  
		Last Modified: Wed, 11 Jun 2025 03:20:23 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9287fea1160b0b93b2b9084f1efcceaddceb7173234a853d4bc32838b5ba6fef`  
		Last Modified: Wed, 11 Jun 2025 03:20:23 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0768d103a32c3b5610ac3f5eed723a96fd6fcd4e0ef998c9391291be4ed0c842`  
		Last Modified: Wed, 11 Jun 2025 03:20:28 GMT  
		Size: 96.0 MB (96038367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d17cb46a20bffef6742e8ff3b49e282e35e66f121a22bc298cdcaa74c9acc2`  
		Last Modified: Wed, 11 Jun 2025 03:20:25 GMT  
		Size: 22.2 MB (22197922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b69185d54127df49f7de5fd0c20d388733e52c69694770b0b1b65affea97c1`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1bc8e6f9218823f7cbd648f9012b83e7b023ac41970432d1298678e4a9ca90`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3dd21e7bc004f70d62a904bfdcac9f4b5eb3cba5c0c8600aaaf507711273c9`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:91ce738b51653495fe4ea3e215477344c9f7efd31e7df004e58bf2fe02dc3f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3020832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce4247d9f150d6afd9e06498ae3e60378bdc507972371f299c8faa79b1f79d`

```dockerfile
```

-	Layers:
	-	`sha256:ba6b4436547e246d349b32dce556c942f4cdf65b0585fdcdb5c978cdd27dc3d0`  
		Last Modified: Wed, 11 Jun 2025 05:20:30 GMT  
		Size: 3.0 MB (2986832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db56fcde0fe907669db0b7a161c0dccecb0354a37af3c4bb9c7d4bdb8cf4c85`  
		Last Modified: Wed, 11 Jun 2025 05:20:30 GMT  
		Size: 34.0 KB (34000 bytes)  
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
$ docker pull influxdb@sha256:fac6ceeca56efc0d97f4a3b22f1c474eb04b6bef570de0264180490e5d3631f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:09742cb64d69a379823ce21c03bd73c1818738cbd69e03b98c107a6918912648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168647686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c599907d80e3d19592504a41f766714f68d762e9dade6ccaa148896b8cb9b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV GOSU_VER=1.16
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 May 2025 23:57:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 May 2025 23:57:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781d4bc0b622264c3b95a002a659e1fd52d7c866443ab2bb61086ef36bfa628a`  
		Last Modified: Wed, 11 Jun 2025 00:27:15 GMT  
		Size: 9.8 MB (9790978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c13825d3e5797e42d23cd10193a1975c7a342fb65a1a140bbf9e3a1942de55b`  
		Last Modified: Wed, 11 Jun 2025 00:27:14 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccbd15a33d1df4cb152d05cfe92fb4d9612886aeb6b87c8aeaac1e23c981ef4`  
		Last Modified: Wed, 11 Jun 2025 00:09:37 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb6b7e49268f149c50757d6496bc7a72d312bce887b0ae6a5d92270bb4acff4`  
		Last Modified: Wed, 11 Jun 2025 00:09:41 GMT  
		Size: 1.0 MB (1006369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e3eae90cf98ee2ed4269e1d08bf34423f33e5a48019464eae48ae1da4ca721`  
		Last Modified: Wed, 11 Jun 2025 00:27:29 GMT  
		Size: 100.2 MB (100242937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cbf8839cb30c0c6cee94987f6edc4e38a0f4c261ffc4ea98bbe0d5dc20a3db`  
		Last Modified: Wed, 11 Jun 2025 00:27:23 GMT  
		Size: 23.5 MB (23546398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bef2790a8c2912e900047217f4411a8aa44a8f6f0967ee97674bee7c0b727e`  
		Last Modified: Wed, 11 Jun 2025 00:09:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa292f7f47619d3e17da9c791e2afba84d8386b527f9a4aed795c5ea36f754e`  
		Last Modified: Wed, 11 Jun 2025 00:09:50 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1101a98020eb8ba562010bb3d105e6a599482e247790af299298a01b2bcb24ac`  
		Last Modified: Wed, 11 Jun 2025 00:09:54 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:90399b48251b3a383055062e0e6b988d41716ce14316fed5a25b6c7dffde36f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3021422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa49386252bbf3a01b40220df62ff98f7f201dc73d4422eae7d9c12ca515d19f`

```dockerfile
```

-	Layers:
	-	`sha256:982fed0043621e4127b99462ff4dea32ea851f6dc964c1cdec297c5bccfba768`  
		Last Modified: Wed, 11 Jun 2025 02:20:49 GMT  
		Size: 3.0 MB (2987604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d9a20fc4b1df79fb9f905cf01c080fc3b585f3475e65eac544c837ba6dc754`  
		Last Modified: Wed, 11 Jun 2025 02:20:50 GMT  
		Size: 33.8 KB (33818 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2734c55f3973993cb937802f40110bc334abc6f61689e80f5437f1e180358766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162312532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066584d55a104c2d3c8bebee98e4b5e3d8c53a63b40d6d886f423189d89748ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV GOSU_VER=1.16
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 May 2025 23:57:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 May 2025 23:57:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1338d636b55bf40227a68fad20cc20a12b4eb561002dfed9d4a9d832a2ad5dec`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 9.6 MB (9588706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c99ce16ececd1df586c43abb732624912826a6957ea184635dc5e43ab58487`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 5.5 MB (5463800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b84852bd30ce95f8cb21262ca216b153313cd6864182247e4c245f2ad84fdd0`  
		Last Modified: Wed, 11 Jun 2025 03:20:23 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9287fea1160b0b93b2b9084f1efcceaddceb7173234a853d4bc32838b5ba6fef`  
		Last Modified: Wed, 11 Jun 2025 03:20:23 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0768d103a32c3b5610ac3f5eed723a96fd6fcd4e0ef998c9391291be4ed0c842`  
		Last Modified: Wed, 11 Jun 2025 03:20:28 GMT  
		Size: 96.0 MB (96038367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d17cb46a20bffef6742e8ff3b49e282e35e66f121a22bc298cdcaa74c9acc2`  
		Last Modified: Wed, 11 Jun 2025 03:20:25 GMT  
		Size: 22.2 MB (22197922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b69185d54127df49f7de5fd0c20d388733e52c69694770b0b1b65affea97c1`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1bc8e6f9218823f7cbd648f9012b83e7b023ac41970432d1298678e4a9ca90`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3dd21e7bc004f70d62a904bfdcac9f4b5eb3cba5c0c8600aaaf507711273c9`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:91ce738b51653495fe4ea3e215477344c9f7efd31e7df004e58bf2fe02dc3f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3020832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce4247d9f150d6afd9e06498ae3e60378bdc507972371f299c8faa79b1f79d`

```dockerfile
```

-	Layers:
	-	`sha256:ba6b4436547e246d349b32dce556c942f4cdf65b0585fdcdb5c978cdd27dc3d0`  
		Last Modified: Wed, 11 Jun 2025 05:20:30 GMT  
		Size: 3.0 MB (2986832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db56fcde0fe907669db0b7a161c0dccecb0354a37af3c4bb9c7d4bdb8cf4c85`  
		Last Modified: Wed, 11 Jun 2025 05:20:30 GMT  
		Size: 34.0 KB (34000 bytes)  
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
$ docker pull influxdb@sha256:fac6ceeca56efc0d97f4a3b22f1c474eb04b6bef570de0264180490e5d3631f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:09742cb64d69a379823ce21c03bd73c1818738cbd69e03b98c107a6918912648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168647686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c599907d80e3d19592504a41f766714f68d762e9dade6ccaa148896b8cb9b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV GOSU_VER=1.16
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 May 2025 23:57:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 May 2025 23:57:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781d4bc0b622264c3b95a002a659e1fd52d7c866443ab2bb61086ef36bfa628a`  
		Last Modified: Wed, 11 Jun 2025 00:27:15 GMT  
		Size: 9.8 MB (9790978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c13825d3e5797e42d23cd10193a1975c7a342fb65a1a140bbf9e3a1942de55b`  
		Last Modified: Wed, 11 Jun 2025 00:27:14 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccbd15a33d1df4cb152d05cfe92fb4d9612886aeb6b87c8aeaac1e23c981ef4`  
		Last Modified: Wed, 11 Jun 2025 00:09:37 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb6b7e49268f149c50757d6496bc7a72d312bce887b0ae6a5d92270bb4acff4`  
		Last Modified: Wed, 11 Jun 2025 00:09:41 GMT  
		Size: 1.0 MB (1006369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e3eae90cf98ee2ed4269e1d08bf34423f33e5a48019464eae48ae1da4ca721`  
		Last Modified: Wed, 11 Jun 2025 00:27:29 GMT  
		Size: 100.2 MB (100242937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cbf8839cb30c0c6cee94987f6edc4e38a0f4c261ffc4ea98bbe0d5dc20a3db`  
		Last Modified: Wed, 11 Jun 2025 00:27:23 GMT  
		Size: 23.5 MB (23546398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bef2790a8c2912e900047217f4411a8aa44a8f6f0967ee97674bee7c0b727e`  
		Last Modified: Wed, 11 Jun 2025 00:09:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa292f7f47619d3e17da9c791e2afba84d8386b527f9a4aed795c5ea36f754e`  
		Last Modified: Wed, 11 Jun 2025 00:09:50 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1101a98020eb8ba562010bb3d105e6a599482e247790af299298a01b2bcb24ac`  
		Last Modified: Wed, 11 Jun 2025 00:09:54 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:90399b48251b3a383055062e0e6b988d41716ce14316fed5a25b6c7dffde36f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3021422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa49386252bbf3a01b40220df62ff98f7f201dc73d4422eae7d9c12ca515d19f`

```dockerfile
```

-	Layers:
	-	`sha256:982fed0043621e4127b99462ff4dea32ea851f6dc964c1cdec297c5bccfba768`  
		Last Modified: Wed, 11 Jun 2025 02:20:49 GMT  
		Size: 3.0 MB (2987604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d9a20fc4b1df79fb9f905cf01c080fc3b585f3475e65eac544c837ba6dc754`  
		Last Modified: Wed, 11 Jun 2025 02:20:50 GMT  
		Size: 33.8 KB (33818 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2734c55f3973993cb937802f40110bc334abc6f61689e80f5437f1e180358766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162312532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066584d55a104c2d3c8bebee98e4b5e3d8c53a63b40d6d886f423189d89748ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV GOSU_VER=1.16
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 May 2025 23:57:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 May 2025 23:57:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1338d636b55bf40227a68fad20cc20a12b4eb561002dfed9d4a9d832a2ad5dec`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 9.6 MB (9588706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c99ce16ececd1df586c43abb732624912826a6957ea184635dc5e43ab58487`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 5.5 MB (5463800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b84852bd30ce95f8cb21262ca216b153313cd6864182247e4c245f2ad84fdd0`  
		Last Modified: Wed, 11 Jun 2025 03:20:23 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9287fea1160b0b93b2b9084f1efcceaddceb7173234a853d4bc32838b5ba6fef`  
		Last Modified: Wed, 11 Jun 2025 03:20:23 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0768d103a32c3b5610ac3f5eed723a96fd6fcd4e0ef998c9391291be4ed0c842`  
		Last Modified: Wed, 11 Jun 2025 03:20:28 GMT  
		Size: 96.0 MB (96038367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d17cb46a20bffef6742e8ff3b49e282e35e66f121a22bc298cdcaa74c9acc2`  
		Last Modified: Wed, 11 Jun 2025 03:20:25 GMT  
		Size: 22.2 MB (22197922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b69185d54127df49f7de5fd0c20d388733e52c69694770b0b1b65affea97c1`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1bc8e6f9218823f7cbd648f9012b83e7b023ac41970432d1298678e4a9ca90`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3dd21e7bc004f70d62a904bfdcac9f4b5eb3cba5c0c8600aaaf507711273c9`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:91ce738b51653495fe4ea3e215477344c9f7efd31e7df004e58bf2fe02dc3f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3020832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce4247d9f150d6afd9e06498ae3e60378bdc507972371f299c8faa79b1f79d`

```dockerfile
```

-	Layers:
	-	`sha256:ba6b4436547e246d349b32dce556c942f4cdf65b0585fdcdb5c978cdd27dc3d0`  
		Last Modified: Wed, 11 Jun 2025 05:20:30 GMT  
		Size: 3.0 MB (2986832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db56fcde0fe907669db0b7a161c0dccecb0354a37af3c4bb9c7d4bdb8cf4c85`  
		Last Modified: Wed, 11 Jun 2025 05:20:30 GMT  
		Size: 34.0 KB (34000 bytes)  
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
		Last Modified: Sun, 08 Jun 2025 12:29:41 GMT  
		Size: 2.2 MB (2203260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f205c8b6ef888b50c090dc278e429864438a6d7b54fd3a3a6fbe7282bc257604`  
		Last Modified: Sun, 08 Jun 2025 12:29:43 GMT  
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
		Last Modified: Sun, 08 Jun 2025 12:29:41 GMT  
		Size: 2.2 MB (2203260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f205c8b6ef888b50c090dc278e429864438a6d7b54fd3a3a6fbe7282bc257604`  
		Last Modified: Sun, 08 Jun 2025 12:29:43 GMT  
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
		Last Modified: Sun, 08 Jun 2025 12:29:41 GMT  
		Size: 2.2 MB (2203260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f205c8b6ef888b50c090dc278e429864438a6d7b54fd3a3a6fbe7282bc257604`  
		Last Modified: Sun, 08 Jun 2025 12:29:43 GMT  
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
		Last Modified: Sun, 08 Jun 2025 12:29:41 GMT  
		Size: 2.2 MB (2203260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f205c8b6ef888b50c090dc278e429864438a6d7b54fd3a3a6fbe7282bc257604`  
		Last Modified: Sun, 08 Jun 2025 12:29:43 GMT  
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
$ docker pull influxdb@sha256:fac6ceeca56efc0d97f4a3b22f1c474eb04b6bef570de0264180490e5d3631f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:09742cb64d69a379823ce21c03bd73c1818738cbd69e03b98c107a6918912648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168647686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c599907d80e3d19592504a41f766714f68d762e9dade6ccaa148896b8cb9b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV GOSU_VER=1.16
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 May 2025 23:57:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 May 2025 23:57:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781d4bc0b622264c3b95a002a659e1fd52d7c866443ab2bb61086ef36bfa628a`  
		Last Modified: Wed, 11 Jun 2025 00:27:15 GMT  
		Size: 9.8 MB (9790978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c13825d3e5797e42d23cd10193a1975c7a342fb65a1a140bbf9e3a1942de55b`  
		Last Modified: Wed, 11 Jun 2025 00:27:14 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccbd15a33d1df4cb152d05cfe92fb4d9612886aeb6b87c8aeaac1e23c981ef4`  
		Last Modified: Wed, 11 Jun 2025 00:09:37 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb6b7e49268f149c50757d6496bc7a72d312bce887b0ae6a5d92270bb4acff4`  
		Last Modified: Wed, 11 Jun 2025 00:09:41 GMT  
		Size: 1.0 MB (1006369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e3eae90cf98ee2ed4269e1d08bf34423f33e5a48019464eae48ae1da4ca721`  
		Last Modified: Wed, 11 Jun 2025 00:27:29 GMT  
		Size: 100.2 MB (100242937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cbf8839cb30c0c6cee94987f6edc4e38a0f4c261ffc4ea98bbe0d5dc20a3db`  
		Last Modified: Wed, 11 Jun 2025 00:27:23 GMT  
		Size: 23.5 MB (23546398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bef2790a8c2912e900047217f4411a8aa44a8f6f0967ee97674bee7c0b727e`  
		Last Modified: Wed, 11 Jun 2025 00:09:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa292f7f47619d3e17da9c791e2afba84d8386b527f9a4aed795c5ea36f754e`  
		Last Modified: Wed, 11 Jun 2025 00:09:50 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1101a98020eb8ba562010bb3d105e6a599482e247790af299298a01b2bcb24ac`  
		Last Modified: Wed, 11 Jun 2025 00:09:54 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:90399b48251b3a383055062e0e6b988d41716ce14316fed5a25b6c7dffde36f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3021422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa49386252bbf3a01b40220df62ff98f7f201dc73d4422eae7d9c12ca515d19f`

```dockerfile
```

-	Layers:
	-	`sha256:982fed0043621e4127b99462ff4dea32ea851f6dc964c1cdec297c5bccfba768`  
		Last Modified: Wed, 11 Jun 2025 02:20:49 GMT  
		Size: 3.0 MB (2987604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d9a20fc4b1df79fb9f905cf01c080fc3b585f3475e65eac544c837ba6dc754`  
		Last Modified: Wed, 11 Jun 2025 02:20:50 GMT  
		Size: 33.8 KB (33818 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2734c55f3973993cb937802f40110bc334abc6f61689e80f5437f1e180358766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162312532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066584d55a104c2d3c8bebee98e4b5e3d8c53a63b40d6d886f423189d89748ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV GOSU_VER=1.16
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 May 2025 23:57:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxd"]
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 May 2025 23:57:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1338d636b55bf40227a68fad20cc20a12b4eb561002dfed9d4a9d832a2ad5dec`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 9.6 MB (9588706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c99ce16ececd1df586c43abb732624912826a6957ea184635dc5e43ab58487`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 5.5 MB (5463800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b84852bd30ce95f8cb21262ca216b153313cd6864182247e4c245f2ad84fdd0`  
		Last Modified: Wed, 11 Jun 2025 03:20:23 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9287fea1160b0b93b2b9084f1efcceaddceb7173234a853d4bc32838b5ba6fef`  
		Last Modified: Wed, 11 Jun 2025 03:20:23 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0768d103a32c3b5610ac3f5eed723a96fd6fcd4e0ef998c9391291be4ed0c842`  
		Last Modified: Wed, 11 Jun 2025 03:20:28 GMT  
		Size: 96.0 MB (96038367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d17cb46a20bffef6742e8ff3b49e282e35e66f121a22bc298cdcaa74c9acc2`  
		Last Modified: Wed, 11 Jun 2025 03:20:25 GMT  
		Size: 22.2 MB (22197922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b69185d54127df49f7de5fd0c20d388733e52c69694770b0b1b65affea97c1`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1bc8e6f9218823f7cbd648f9012b83e7b023ac41970432d1298678e4a9ca90`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3dd21e7bc004f70d62a904bfdcac9f4b5eb3cba5c0c8600aaaf507711273c9`  
		Last Modified: Wed, 11 Jun 2025 03:20:24 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:91ce738b51653495fe4ea3e215477344c9f7efd31e7df004e58bf2fe02dc3f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3020832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ce4247d9f150d6afd9e06498ae3e60378bdc507972371f299c8faa79b1f79d`

```dockerfile
```

-	Layers:
	-	`sha256:ba6b4436547e246d349b32dce556c942f4cdf65b0585fdcdb5c978cdd27dc3d0`  
		Last Modified: Wed, 11 Jun 2025 05:20:30 GMT  
		Size: 3.0 MB (2986832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db56fcde0fe907669db0b7a161c0dccecb0354a37af3c4bb9c7d4bdb8cf4c85`  
		Last Modified: Wed, 11 Jun 2025 05:20:30 GMT  
		Size: 34.0 KB (34000 bytes)  
		MIME: application/vnd.in-toto+json
