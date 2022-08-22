<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.10-data`](#influxdb110-data)
-	[`influxdb:1.10-data-alpine`](#influxdb110-data-alpine)
-	[`influxdb:1.10-meta`](#influxdb110-meta)
-	[`influxdb:1.10-meta-alpine`](#influxdb110-meta-alpine)
-	[`influxdb:1.10.0-data`](#influxdb1100-data)
-	[`influxdb:1.10.0-data-alpine`](#influxdb1100-data-alpine)
-	[`influxdb:1.10.0-meta`](#influxdb1100-meta)
-	[`influxdb:1.10.0-meta-alpine`](#influxdb1100-meta-alpine)
-	[`influxdb:1.8`](#influxdb18)
-	[`influxdb:1.8-alpine`](#influxdb18-alpine)
-	[`influxdb:1.8-data`](#influxdb18-data)
-	[`influxdb:1.8-data-alpine`](#influxdb18-data-alpine)
-	[`influxdb:1.8-meta`](#influxdb18-meta)
-	[`influxdb:1.8-meta-alpine`](#influxdb18-meta-alpine)
-	[`influxdb:1.8.10`](#influxdb1810)
-	[`influxdb:1.8.10-alpine`](#influxdb1810-alpine)
-	[`influxdb:1.8.10-data`](#influxdb1810-data)
-	[`influxdb:1.8.10-data-alpine`](#influxdb1810-data-alpine)
-	[`influxdb:1.8.10-meta`](#influxdb1810-meta)
-	[`influxdb:1.8.10-meta-alpine`](#influxdb1810-meta-alpine)
-	[`influxdb:1.9-data`](#influxdb19-data)
-	[`influxdb:1.9-data-alpine`](#influxdb19-data-alpine)
-	[`influxdb:1.9-meta`](#influxdb19-meta)
-	[`influxdb:1.9-meta-alpine`](#influxdb19-meta-alpine)
-	[`influxdb:1.9.8-data`](#influxdb198-data)
-	[`influxdb:1.9.8-data-alpine`](#influxdb198-data-alpine)
-	[`influxdb:1.9.8-meta`](#influxdb198-meta)
-	[`influxdb:1.9.8-meta-alpine`](#influxdb198-meta-alpine)
-	[`influxdb:2.2`](#influxdb22)
-	[`influxdb:2.2-alpine`](#influxdb22-alpine)
-	[`influxdb:2.2.0`](#influxdb220)
-	[`influxdb:2.2.0-alpine`](#influxdb220-alpine)
-	[`influxdb:2.3`](#influxdb23)
-	[`influxdb:2.3-alpine`](#influxdb23-alpine)
-	[`influxdb:2.3.0`](#influxdb230)
-	[`influxdb:2.3.0-alpine`](#influxdb230-alpine)
-	[`influxdb:2.4`](#influxdb24)
-	[`influxdb:2.4-alpine`](#influxdb24-alpine)
-	[`influxdb:2.4.0`](#influxdb240)
-	[`influxdb:2.4.0-alpine`](#influxdb240-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:data`](#influxdbdata)
-	[`influxdb:data-alpine`](#influxdbdata-alpine)
-	[`influxdb:latest`](#influxdblatest)
-	[`influxdb:meta`](#influxdbmeta)
-	[`influxdb:meta-alpine`](#influxdbmeta-alpine)

## `influxdb:1.10-data`

```console
$ docker pull influxdb@sha256:ce96d974eb209d8a21bbaab42cbd59efe27071c82e9a6a5cb1559f18791844fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:35961f37cfee7b6f4963868336896a3548d0b8791fb8dc2bbf881b1e38718274
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101730015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9715e4500943a10eab02d8e5914a93996a9c8507e122d15fbcfa2a63fe3fb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 05 Aug 2022 18:20:08 GMT
ENV INFLUXDB_VERSION=1.10.0-c1.10.0
# Fri, 05 Aug 2022 18:20:13 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Fri, 05 Aug 2022 18:20:13 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 05 Aug 2022 18:20:13 GMT
EXPOSE 8086
# Fri, 05 Aug 2022 18:20:13 GMT
VOLUME [/var/lib/influxdb]
# Fri, 05 Aug 2022 18:20:13 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 05 Aug 2022 18:20:13 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 05 Aug 2022 18:20:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Aug 2022 18:20:14 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4f40394b4c2f79a6796a75963da01829ce6d559b5750800adb91a01caed707`  
		Last Modified: Fri, 05 Aug 2022 18:21:50 GMT  
		Size: 30.7 MB (30693270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00107037718338c80a26bc084540639c304c43c8dd1f9df2274e5bff6cb4c13c`  
		Last Modified: Fri, 05 Aug 2022 18:21:45 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f780e28df8553081cb76f0c6fce47883add3582377bafd10775d9feee5c2563`  
		Last Modified: Fri, 05 Aug 2022 18:21:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7601c3d4faa0f2411cbf45d794aec78a5aa967c51a8471f2d29d822da52f9c9c`  
		Last Modified: Fri, 05 Aug 2022 18:21:45 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10-data-alpine`

```console
$ docker pull influxdb@sha256:6977f3da3e776a40c89a52509c3842f8c335e6b959753a196a27e5596360162a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c014fea40d855272ef5462d65f8452e437707afd49242b535b6f3d2a70e62f42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34971355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167daf06a9d35631732952903037c4ae4e3d80f7187875f77aff03566ba0a693`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:36:01 GMT
ENV INFLUXDB_VERSION=1.10.0-c1.10.0
# Mon, 22 Aug 2022 20:23:07 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 22 Aug 2022 20:23:07 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Mon, 22 Aug 2022 20:23:08 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:23:08 GMT
VOLUME [/var/lib/influxdb]
# Mon, 22 Aug 2022 20:23:08 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:23:08 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Mon, 22 Aug 2022 20:23:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:23:08 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870b7924ffe35ca300051767bb768f8bc6ddc4d293f8a88c63fa222e03f7edef`  
		Last Modified: Mon, 22 Aug 2022 20:26:14 GMT  
		Size: 30.7 MB (30652665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89314d5e18db6c3b0a1c4e96fa137994e003fa452840bac621c7304b9323604`  
		Last Modified: Mon, 22 Aug 2022 20:26:08 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a52d2822fb7ee0cfa05a69dd1f1e58529daef36dad4c0712ee163c78bb92cb`  
		Last Modified: Mon, 22 Aug 2022 20:26:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1111fe89fc4160e717f87171ff0f8c02c2f8b7231a87eaaa0d055ad1d5a22ee3`  
		Last Modified: Mon, 22 Aug 2022 20:26:08 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10-meta`

```console
$ docker pull influxdb@sha256:9b15d1d3cb2198dccadae00d0553761764f8d5981e37540f1f64625dd1054d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:694d312bdfff12be32abef4900bcc77e25b9b5a9c3cf22e5dc62751702e524d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82942712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa25d81afa33a26ac4a7ee206c45ec8c99a47df4e43bcd88492cf4743d98384e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 05 Aug 2022 18:20:08 GMT
ENV INFLUXDB_VERSION=1.10.0-c1.10.0
# Fri, 05 Aug 2022 18:20:29 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Fri, 05 Aug 2022 18:20:29 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 05 Aug 2022 18:20:29 GMT
EXPOSE 8091
# Fri, 05 Aug 2022 18:20:29 GMT
VOLUME [/var/lib/influxdb]
# Fri, 05 Aug 2022 18:20:29 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 05 Aug 2022 18:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Aug 2022 18:20:29 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3963e83235bb5b7a72cf48d7534b24d43697ea3224a13f748957da5ca6307ebb`  
		Last Modified: Fri, 05 Aug 2022 18:22:16 GMT  
		Size: 11.9 MB (11907170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c97fbca0fdf76d1e5293bb56f6770bb3ae47b61c215cc1a9b62941896644c8`  
		Last Modified: Fri, 05 Aug 2022 18:22:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e1ad96592e96a4107896b8dee3348554b585a687162c074ba48ebb9bb70614`  
		Last Modified: Fri, 05 Aug 2022 18:22:14 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10-meta-alpine`

```console
$ docker pull influxdb@sha256:c54692961476dd3d2326b1a6b285b0e637ccd5ed47534b6cb8f20dd85329fa75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:762c401300e37eec0348a3bd0e3f7d89f8a12cc34fcc769a17598e86d603f667
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16189420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f623a23f8e5c8e1c55049cffe9fbf44fbeb161324cf7347b086273d10970a339`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:36:01 GMT
ENV INFLUXDB_VERSION=1.10.0-c1.10.0
# Mon, 22 Aug 2022 20:23:17 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 22 Aug 2022 20:23:17 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Mon, 22 Aug 2022 20:23:17 GMT
EXPOSE 8091
# Mon, 22 Aug 2022 20:23:17 GMT
VOLUME [/var/lib/influxdb]
# Mon, 22 Aug 2022 20:23:17 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:23:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:23:17 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b59dc2348ddc94dec9b35989d33ca3346cc976efbc292ebdc7aeb91a2832838`  
		Last Modified: Mon, 22 Aug 2022 20:26:28 GMT  
		Size: 11.9 MB (11871936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8c138a4f41ec61b666fb05e1740da9b3c12f92fcbefb82729995fcd48ff46f`  
		Last Modified: Mon, 22 Aug 2022 20:26:26 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b341a61be9df085a7999cfd98883637b31792ab6377e330f7239f0a8d7fd3b7a`  
		Last Modified: Mon, 22 Aug 2022 20:26:25 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.0-data`

```console
$ docker pull influxdb@sha256:ce96d974eb209d8a21bbaab42cbd59efe27071c82e9a6a5cb1559f18791844fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.0-data` - linux; amd64

```console
$ docker pull influxdb@sha256:35961f37cfee7b6f4963868336896a3548d0b8791fb8dc2bbf881b1e38718274
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101730015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9715e4500943a10eab02d8e5914a93996a9c8507e122d15fbcfa2a63fe3fb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 05 Aug 2022 18:20:08 GMT
ENV INFLUXDB_VERSION=1.10.0-c1.10.0
# Fri, 05 Aug 2022 18:20:13 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Fri, 05 Aug 2022 18:20:13 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 05 Aug 2022 18:20:13 GMT
EXPOSE 8086
# Fri, 05 Aug 2022 18:20:13 GMT
VOLUME [/var/lib/influxdb]
# Fri, 05 Aug 2022 18:20:13 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 05 Aug 2022 18:20:13 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 05 Aug 2022 18:20:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Aug 2022 18:20:14 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4f40394b4c2f79a6796a75963da01829ce6d559b5750800adb91a01caed707`  
		Last Modified: Fri, 05 Aug 2022 18:21:50 GMT  
		Size: 30.7 MB (30693270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00107037718338c80a26bc084540639c304c43c8dd1f9df2274e5bff6cb4c13c`  
		Last Modified: Fri, 05 Aug 2022 18:21:45 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f780e28df8553081cb76f0c6fce47883add3582377bafd10775d9feee5c2563`  
		Last Modified: Fri, 05 Aug 2022 18:21:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7601c3d4faa0f2411cbf45d794aec78a5aa967c51a8471f2d29d822da52f9c9c`  
		Last Modified: Fri, 05 Aug 2022 18:21:45 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.0-data-alpine`

```console
$ docker pull influxdb@sha256:6977f3da3e776a40c89a52509c3842f8c335e6b959753a196a27e5596360162a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.0-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c014fea40d855272ef5462d65f8452e437707afd49242b535b6f3d2a70e62f42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34971355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167daf06a9d35631732952903037c4ae4e3d80f7187875f77aff03566ba0a693`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:36:01 GMT
ENV INFLUXDB_VERSION=1.10.0-c1.10.0
# Mon, 22 Aug 2022 20:23:07 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 22 Aug 2022 20:23:07 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Mon, 22 Aug 2022 20:23:08 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:23:08 GMT
VOLUME [/var/lib/influxdb]
# Mon, 22 Aug 2022 20:23:08 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:23:08 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Mon, 22 Aug 2022 20:23:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:23:08 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870b7924ffe35ca300051767bb768f8bc6ddc4d293f8a88c63fa222e03f7edef`  
		Last Modified: Mon, 22 Aug 2022 20:26:14 GMT  
		Size: 30.7 MB (30652665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89314d5e18db6c3b0a1c4e96fa137994e003fa452840bac621c7304b9323604`  
		Last Modified: Mon, 22 Aug 2022 20:26:08 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a52d2822fb7ee0cfa05a69dd1f1e58529daef36dad4c0712ee163c78bb92cb`  
		Last Modified: Mon, 22 Aug 2022 20:26:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1111fe89fc4160e717f87171ff0f8c02c2f8b7231a87eaaa0d055ad1d5a22ee3`  
		Last Modified: Mon, 22 Aug 2022 20:26:08 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.0-meta`

```console
$ docker pull influxdb@sha256:9b15d1d3cb2198dccadae00d0553761764f8d5981e37540f1f64625dd1054d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.0-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:694d312bdfff12be32abef4900bcc77e25b9b5a9c3cf22e5dc62751702e524d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82942712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa25d81afa33a26ac4a7ee206c45ec8c99a47df4e43bcd88492cf4743d98384e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 05 Aug 2022 18:20:08 GMT
ENV INFLUXDB_VERSION=1.10.0-c1.10.0
# Fri, 05 Aug 2022 18:20:29 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Fri, 05 Aug 2022 18:20:29 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 05 Aug 2022 18:20:29 GMT
EXPOSE 8091
# Fri, 05 Aug 2022 18:20:29 GMT
VOLUME [/var/lib/influxdb]
# Fri, 05 Aug 2022 18:20:29 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 05 Aug 2022 18:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Aug 2022 18:20:29 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3963e83235bb5b7a72cf48d7534b24d43697ea3224a13f748957da5ca6307ebb`  
		Last Modified: Fri, 05 Aug 2022 18:22:16 GMT  
		Size: 11.9 MB (11907170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c97fbca0fdf76d1e5293bb56f6770bb3ae47b61c215cc1a9b62941896644c8`  
		Last Modified: Fri, 05 Aug 2022 18:22:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e1ad96592e96a4107896b8dee3348554b585a687162c074ba48ebb9bb70614`  
		Last Modified: Fri, 05 Aug 2022 18:22:14 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.10.0-meta-alpine`

```console
$ docker pull influxdb@sha256:c54692961476dd3d2326b1a6b285b0e637ccd5ed47534b6cb8f20dd85329fa75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.10.0-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:762c401300e37eec0348a3bd0e3f7d89f8a12cc34fcc769a17598e86d603f667
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16189420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f623a23f8e5c8e1c55049cffe9fbf44fbeb161324cf7347b086273d10970a339`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:36:01 GMT
ENV INFLUXDB_VERSION=1.10.0-c1.10.0
# Mon, 22 Aug 2022 20:23:17 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 22 Aug 2022 20:23:17 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Mon, 22 Aug 2022 20:23:17 GMT
EXPOSE 8091
# Mon, 22 Aug 2022 20:23:17 GMT
VOLUME [/var/lib/influxdb]
# Mon, 22 Aug 2022 20:23:17 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:23:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:23:17 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b59dc2348ddc94dec9b35989d33ca3346cc976efbc292ebdc7aeb91a2832838`  
		Last Modified: Mon, 22 Aug 2022 20:26:28 GMT  
		Size: 11.9 MB (11871936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8c138a4f41ec61b666fb05e1740da9b3c12f92fcbefb82729995fcd48ff46f`  
		Last Modified: Mon, 22 Aug 2022 20:26:26 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b341a61be9df085a7999cfd98883637b31792ab6377e330f7239f0a8d7fd3b7a`  
		Last Modified: Mon, 22 Aug 2022 20:26:25 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:ab2afa118fec0dc14f2c40fb1b6b76fbaec61bbb0d81a3049146ffaa29e4a6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:246fcbd4ca250ca8aa4c20c8b3e6970040dff4e92c8af3e285a49288332a2267
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125922409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3a88ba75253956a3b6758e043e62fddc9c0cca27f4b5c54498af346084550f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 03 Aug 2022 02:03:54 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 03 Aug 2022 02:03:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 03 Aug 2022 02:03:59 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 03 Aug 2022 02:03:59 GMT
EXPOSE 8086
# Wed, 03 Aug 2022 02:03:59 GMT
VOLUME [/var/lib/influxdb]
# Wed, 03 Aug 2022 02:03:59 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:03:59 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 03 Aug 2022 02:03:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:03:59 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e157e7adeb534595c09a96412e4c05a01ed423ac15ad36980d953c09f0645f`  
		Last Modified: Wed, 03 Aug 2022 02:06:24 GMT  
		Size: 54.9 MB (54885722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d279ba0a4507e3f2b46cc3f32a4b17ddcc1edc204177a901c9e023173ec2bed`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4eb369c0591aadfb4eabed26639f30674416f20a14d6c81311e840bd2c93532`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cd05d995284b2500e0d3af4a7cd3b3146b2f70a13e5839585435ab9835cbbd`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:6931ddb70f718024b35ca30edc8e483bbe5ea62f8c921a13f14ebb8c222fbc95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116961846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b4c644ac63622ac18c47e813b88ed8c0f9eed25dca84cd44c97609ce15f634`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:36 GMT
ADD file:4e2780cf1c53cc1c475d2ebae48d4bf03029fa68ba9fbc991be76ac9e3944977 in / 
# Tue, 02 Aug 2022 00:58:37 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:47:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 04 Aug 2022 08:07:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 04 Aug 2022 08:07:04 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 04 Aug 2022 08:07:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 04 Aug 2022 08:07:11 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 04 Aug 2022 08:07:11 GMT
EXPOSE 8086
# Thu, 04 Aug 2022 08:07:12 GMT
VOLUME [/var/lib/influxdb]
# Thu, 04 Aug 2022 08:07:12 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 04 Aug 2022 08:07:12 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 04 Aug 2022 08:07:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Aug 2022 08:07:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:05aa23077de69478dfc20e56aa2d54a2b13bbef07c4d2578524585d098af4e72`  
		Last Modified: Tue, 02 Aug 2022 01:06:07 GMT  
		Size: 50.2 MB (50195271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a4ec510d3ede75fd285276ee8b3d9dd3c1d2bce8f21ae0f2de4898c015b9e`  
		Last Modified: Tue, 02 Aug 2022 02:09:14 GMT  
		Size: 4.9 MB (4930860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef792f88dc77db1940eec048a6d0b4d691c7650b28cd058aed9314fea5f708b6`  
		Last Modified: Tue, 02 Aug 2022 02:09:14 GMT  
		Size: 10.2 MB (10217964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ddf6dbab250f8a67d3cdfe93ac12d7780cf6fad00af63c2b8b94d2103c797f`  
		Last Modified: Thu, 04 Aug 2022 08:07:24 GMT  
		Size: 2.9 KB (2901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf3895c07eacf37c1209c36c9fc743701dcebd4499106a1a505bb46e01bfea9`  
		Last Modified: Thu, 04 Aug 2022 08:07:31 GMT  
		Size: 51.6 MB (51613134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a297d08ce60909a5c77a471d0653301db4098699d8781cd42ff33eac3a807e4`  
		Last Modified: Thu, 04 Aug 2022 08:07:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60805d9d430ecd463efb551c54edbebc514f646ec022fac5a6e99e3f7a9aa686`  
		Last Modified: Thu, 04 Aug 2022 08:07:24 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7193dbe67b7bd26b52b2888052b1fd13fe99fcaec3eeebc35cdc485f358d8ac`  
		Last Modified: Thu, 04 Aug 2022 08:07:24 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f111b2c8baeb5e708ffd77ce93d362259ce15ab18bd9501b2392dfe508de55e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120723848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516748423f9411aa2c5bdb8e5165baa83b72cf1e5c38e223d204f5aed08da215`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:24 GMT
ADD file:5972a7ce0f1d89d63e5ed48011838c998fa506cd34f8e5f0b0070039cd74c5b9 in / 
# Tue, 02 Aug 2022 00:40:25 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:24:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 22:43:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 02 Aug 2022 22:43:06 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 02 Aug 2022 22:43:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 02 Aug 2022 22:43:15 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 02 Aug 2022 22:43:15 GMT
EXPOSE 8086
# Tue, 02 Aug 2022 22:43:16 GMT
VOLUME [/var/lib/influxdb]
# Tue, 02 Aug 2022 22:43:18 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 02 Aug 2022 22:43:19 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 02 Aug 2022 22:43:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Aug 2022 22:43:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:114ba63dd73a866ac1bb59fe594dfd218f44ac9b4fa4b2c68499da5584fcfa9d`  
		Last Modified: Tue, 02 Aug 2022 00:45:33 GMT  
		Size: 53.7 MB (53683005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0b8a8acead4d7bf71c232054b2a0a8e08eb3e1e2cf46f9f3dba68723e88c85`  
		Last Modified: Tue, 02 Aug 2022 01:44:32 GMT  
		Size: 5.1 MB (5148901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ea641ee67989acdb6af3d8b9b984ecd751a2a83c3b7ce071542b31c9ac1304`  
		Last Modified: Tue, 02 Aug 2022 01:44:33 GMT  
		Size: 10.7 MB (10657494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ec686a96c32bacc8ec1f4f9cbac10fb5825eace12202b3aecb9514915d2906`  
		Last Modified: Tue, 02 Aug 2022 22:45:58 GMT  
		Size: 2.9 KB (2860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda7888afb2785b5be1cf6849612cd64be15cbf6bd78def5dd15202029a1809e`  
		Last Modified: Tue, 02 Aug 2022 22:46:06 GMT  
		Size: 51.2 MB (51229873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c5d5a7b25536a5e738a81ff9cda760a9e419477a92db3b0e766dbca913cbd8`  
		Last Modified: Tue, 02 Aug 2022 22:45:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735dfa4635a7dceae5852deb0b682bf613ab4d8fc6d6b71462a08b3d47213be8`  
		Last Modified: Tue, 02 Aug 2022 22:45:59 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e804c21a0afdb96cac59c99785b092a1a5d4ff38042016dd4c0f4919f2ba44d7`  
		Last Modified: Tue, 02 Aug 2022 22:45:59 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:0fd1969335adb2dd533c6c162720144c8b0648b7b51d274f0614b4b6e2b277fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8efe52dc0c6bdf7beb50f6d6930127e70e35152a5815894b2226749c135f5f15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58966047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4e803c566d11ac4423c3ef70f633de2d0b5dff2db4c62f7d55396470011bfc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:35:04 GMT
ENV INFLUXDB_VERSION=1.8.10
# Mon, 22 Aug 2022 20:22:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 22 Aug 2022 20:22:30 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Mon, 22 Aug 2022 20:22:31 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:22:31 GMT
VOLUME [/var/lib/influxdb]
# Mon, 22 Aug 2022 20:22:31 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:22:31 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Mon, 22 Aug 2022 20:22:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:22:31 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f4276ac0611dbd0c24d15256d089c8f800d0de493d6f33365ad58522cfe70c`  
		Last Modified: Mon, 22 Aug 2022 20:25:22 GMT  
		Size: 54.6 MB (54647419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8a8bea3229b318ec1c61bcb11b414093cd653a2d2ff3d48e8224a282fb734c`  
		Last Modified: Mon, 22 Aug 2022 20:25:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e02f49aba4792edc976f8b9ab76f91d5980489c96f6129681bc1ebc3955a039`  
		Last Modified: Mon, 22 Aug 2022 20:25:15 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173d34f1771efd20aac74d07fbce7833bbb73a475a9e258128256676eb8b9f8f`  
		Last Modified: Mon, 22 Aug 2022 20:25:15 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data`

```console
$ docker pull influxdb@sha256:96d2ba932c6f83edbd5a81a35f1fcbc29a453aac31360ffb7ece49f3a0fb6b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:428f0a943f4d1bb2821b1129b3f18cf70a863d0ee76bfb58b6b5b3b165a18ac2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127741811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdab6d751f8f38c2628ec4deb6338d9c17dfe13138e74ecb2f737e230802a5f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 03 Aug 2022 02:04:04 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 03 Aug 2022 02:04:09 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 03 Aug 2022 02:04:09 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 03 Aug 2022 02:04:09 GMT
EXPOSE 8086
# Wed, 03 Aug 2022 02:04:09 GMT
VOLUME [/var/lib/influxdb]
# Wed, 03 Aug 2022 02:04:10 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:04:10 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 03 Aug 2022 02:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:04:10 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c5bfaf0100c41f5215b47473f5f76d5aec8fbb92e515eff6e4037e1992288c`  
		Last Modified: Wed, 03 Aug 2022 02:06:43 GMT  
		Size: 56.7 MB (56705063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fecda5610f26727ec646dd115dbdeb639b2bfca3e6a099e10db99d96749cc9`  
		Last Modified: Wed, 03 Aug 2022 02:06:36 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c581908d052c6b5a0a693b80b21529731e1c859dfbf858e9c826d50d5f529b2`  
		Last Modified: Wed, 03 Aug 2022 02:06:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4195b4a1bce05cd25771565d8307ec366a139995c6cc09b606d8187dd997ec`  
		Last Modified: Wed, 03 Aug 2022 02:06:36 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data-alpine`

```console
$ docker pull influxdb@sha256:3ae2d7877a2ca613d44fc532fdfd48feff4e80bea5346e0d10416d0ca6fb31a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c97c879631f76b6bc00095e53a9a5c30f15b9333611581458ba91ca0884f3469
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60822331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf7673e1fbd0a4bc7479f3211f3049aed4d80055fef6375acbcd1814832ea71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:35:16 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Tue, 09 Aug 2022 20:35:25 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 20:35:26 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 09 Aug 2022 20:35:26 GMT
EXPOSE 8086
# Tue, 09 Aug 2022 20:35:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Aug 2022 20:35:26 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 09 Aug 2022 20:35:26 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 09 Aug 2022 20:35:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 20:35:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660d3aa692c8b0d29b4e7e0ffac0a02c11599f26cc0bd002756e9e6b76108cd8`  
		Last Modified: Tue, 09 Aug 2022 20:38:42 GMT  
		Size: 56.5 MB (56503646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa39318d497281db1f9a02388ac2fd99a5e9ad63f66e041c00b44cbcf1759f23`  
		Last Modified: Tue, 09 Aug 2022 20:38:34 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32b49f32e3c793a399105f5b26a556202ced39b82314e099cb5a9a56ae3acb0`  
		Last Modified: Tue, 09 Aug 2022 20:38:34 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d76fd0d307652bc45d42778a79476cd91b78e515dd1b95714e35721de95fae`  
		Last Modified: Tue, 09 Aug 2022 20:38:34 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta`

```console
$ docker pull influxdb@sha256:5e345117ba9f8143da42364749f5fba2289c9a916ca5ef0688f3b1efa6b97d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3b7b709c16fcc6f1418f42ae901cdff9553eb2556a3ed39c1b94e0a53847d202
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94448300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269924d4772c2a43ff87d66fe3b3c36a9e5b728d1edc1b63b809cb07b2a268dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 03 Aug 2022 02:04:04 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 03 Aug 2022 02:04:17 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 03 Aug 2022 02:04:17 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 03 Aug 2022 02:04:17 GMT
EXPOSE 8091
# Wed, 03 Aug 2022 02:04:18 GMT
VOLUME [/var/lib/influxdb]
# Wed, 03 Aug 2022 02:04:18 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:04:18 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200d1c964c659220d3808f865050cb12346d90f4ef8b119143f59fc6f5380bf`  
		Last Modified: Wed, 03 Aug 2022 02:07:00 GMT  
		Size: 23.4 MB (23412758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9431f49f5357a73efefcea8ce35acb4a54df1b73b66c5ae29001e1294b836ef7`  
		Last Modified: Wed, 03 Aug 2022 02:06:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155e3e30f68132af9a5c0902bc1c7e817b709acf97e82f34c92b563f500339fd`  
		Last Modified: Wed, 03 Aug 2022 02:06:57 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta-alpine`

```console
$ docker pull influxdb@sha256:1bc53a804fca50ef4f8ff62269b97fc2f999f3f1b4b2c286b9a1d1e6252f1841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b2295d4b7e378ebe952bd3db3eee150fc33b5c432bc6bd6ed03b233d07764186
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27610491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daffb717093e5bdc9c615118ce300a424b46c357b7e071101f2a78ceb3ccc024`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:35:16 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Tue, 09 Aug 2022 20:35:36 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 20:35:36 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 09 Aug 2022 20:35:37 GMT
EXPOSE 8091
# Tue, 09 Aug 2022 20:35:37 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Aug 2022 20:35:37 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 09 Aug 2022 20:35:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 20:35:37 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85effd48049aab32e47b63df4632902515f5c87326ec4d45f173490d9040e308`  
		Last Modified: Tue, 09 Aug 2022 20:38:58 GMT  
		Size: 23.3 MB (23293005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83a163fb6c3d2277185ea1bd9a4aee51518e3d8b101a46364ffeb99db61367f`  
		Last Modified: Tue, 09 Aug 2022 20:38:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef0f697d368b5ad70ca2b594e9b44589e36b36e30957e81d64e7f960a99db90`  
		Last Modified: Tue, 09 Aug 2022 20:38:55 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10`

```console
$ docker pull influxdb@sha256:ab2afa118fec0dc14f2c40fb1b6b76fbaec61bbb0d81a3049146ffaa29e4a6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.10` - linux; amd64

```console
$ docker pull influxdb@sha256:246fcbd4ca250ca8aa4c20c8b3e6970040dff4e92c8af3e285a49288332a2267
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125922409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3a88ba75253956a3b6758e043e62fddc9c0cca27f4b5c54498af346084550f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 03 Aug 2022 02:03:54 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 03 Aug 2022 02:03:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 03 Aug 2022 02:03:59 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 03 Aug 2022 02:03:59 GMT
EXPOSE 8086
# Wed, 03 Aug 2022 02:03:59 GMT
VOLUME [/var/lib/influxdb]
# Wed, 03 Aug 2022 02:03:59 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:03:59 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 03 Aug 2022 02:03:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:03:59 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e157e7adeb534595c09a96412e4c05a01ed423ac15ad36980d953c09f0645f`  
		Last Modified: Wed, 03 Aug 2022 02:06:24 GMT  
		Size: 54.9 MB (54885722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d279ba0a4507e3f2b46cc3f32a4b17ddcc1edc204177a901c9e023173ec2bed`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4eb369c0591aadfb4eabed26639f30674416f20a14d6c81311e840bd2c93532`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cd05d995284b2500e0d3af4a7cd3b3146b2f70a13e5839585435ab9835cbbd`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:6931ddb70f718024b35ca30edc8e483bbe5ea62f8c921a13f14ebb8c222fbc95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116961846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b4c644ac63622ac18c47e813b88ed8c0f9eed25dca84cd44c97609ce15f634`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 00:58:36 GMT
ADD file:4e2780cf1c53cc1c475d2ebae48d4bf03029fa68ba9fbc991be76ac9e3944977 in / 
# Tue, 02 Aug 2022 00:58:37 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:47:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 04 Aug 2022 08:07:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 04 Aug 2022 08:07:04 GMT
ENV INFLUXDB_VERSION=1.8.10
# Thu, 04 Aug 2022 08:07:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Thu, 04 Aug 2022 08:07:11 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 04 Aug 2022 08:07:11 GMT
EXPOSE 8086
# Thu, 04 Aug 2022 08:07:12 GMT
VOLUME [/var/lib/influxdb]
# Thu, 04 Aug 2022 08:07:12 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 04 Aug 2022 08:07:12 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 04 Aug 2022 08:07:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Aug 2022 08:07:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:05aa23077de69478dfc20e56aa2d54a2b13bbef07c4d2578524585d098af4e72`  
		Last Modified: Tue, 02 Aug 2022 01:06:07 GMT  
		Size: 50.2 MB (50195271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a4ec510d3ede75fd285276ee8b3d9dd3c1d2bce8f21ae0f2de4898c015b9e`  
		Last Modified: Tue, 02 Aug 2022 02:09:14 GMT  
		Size: 4.9 MB (4930860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef792f88dc77db1940eec048a6d0b4d691c7650b28cd058aed9314fea5f708b6`  
		Last Modified: Tue, 02 Aug 2022 02:09:14 GMT  
		Size: 10.2 MB (10217964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ddf6dbab250f8a67d3cdfe93ac12d7780cf6fad00af63c2b8b94d2103c797f`  
		Last Modified: Thu, 04 Aug 2022 08:07:24 GMT  
		Size: 2.9 KB (2901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf3895c07eacf37c1209c36c9fc743701dcebd4499106a1a505bb46e01bfea9`  
		Last Modified: Thu, 04 Aug 2022 08:07:31 GMT  
		Size: 51.6 MB (51613134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a297d08ce60909a5c77a471d0653301db4098699d8781cd42ff33eac3a807e4`  
		Last Modified: Thu, 04 Aug 2022 08:07:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60805d9d430ecd463efb551c54edbebc514f646ec022fac5a6e99e3f7a9aa686`  
		Last Modified: Thu, 04 Aug 2022 08:07:24 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7193dbe67b7bd26b52b2888052b1fd13fe99fcaec3eeebc35cdc485f358d8ac`  
		Last Modified: Thu, 04 Aug 2022 08:07:24 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f111b2c8baeb5e708ffd77ce93d362259ce15ab18bd9501b2392dfe508de55e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120723848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516748423f9411aa2c5bdb8e5165baa83b72cf1e5c38e223d204f5aed08da215`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:24 GMT
ADD file:5972a7ce0f1d89d63e5ed48011838c998fa506cd34f8e5f0b0070039cd74c5b9 in / 
# Tue, 02 Aug 2022 00:40:25 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:24:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 22:43:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 02 Aug 2022 22:43:06 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 02 Aug 2022 22:43:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 02 Aug 2022 22:43:15 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 02 Aug 2022 22:43:15 GMT
EXPOSE 8086
# Tue, 02 Aug 2022 22:43:16 GMT
VOLUME [/var/lib/influxdb]
# Tue, 02 Aug 2022 22:43:18 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 02 Aug 2022 22:43:19 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 02 Aug 2022 22:43:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Aug 2022 22:43:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:114ba63dd73a866ac1bb59fe594dfd218f44ac9b4fa4b2c68499da5584fcfa9d`  
		Last Modified: Tue, 02 Aug 2022 00:45:33 GMT  
		Size: 53.7 MB (53683005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0b8a8acead4d7bf71c232054b2a0a8e08eb3e1e2cf46f9f3dba68723e88c85`  
		Last Modified: Tue, 02 Aug 2022 01:44:32 GMT  
		Size: 5.1 MB (5148901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ea641ee67989acdb6af3d8b9b984ecd751a2a83c3b7ce071542b31c9ac1304`  
		Last Modified: Tue, 02 Aug 2022 01:44:33 GMT  
		Size: 10.7 MB (10657494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ec686a96c32bacc8ec1f4f9cbac10fb5825eace12202b3aecb9514915d2906`  
		Last Modified: Tue, 02 Aug 2022 22:45:58 GMT  
		Size: 2.9 KB (2860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda7888afb2785b5be1cf6849612cd64be15cbf6bd78def5dd15202029a1809e`  
		Last Modified: Tue, 02 Aug 2022 22:46:06 GMT  
		Size: 51.2 MB (51229873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c5d5a7b25536a5e738a81ff9cda760a9e419477a92db3b0e766dbca913cbd8`  
		Last Modified: Tue, 02 Aug 2022 22:45:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735dfa4635a7dceae5852deb0b682bf613ab4d8fc6d6b71462a08b3d47213be8`  
		Last Modified: Tue, 02 Aug 2022 22:45:59 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e804c21a0afdb96cac59c99785b092a1a5d4ff38042016dd4c0f4919f2ba44d7`  
		Last Modified: Tue, 02 Aug 2022 22:45:59 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-alpine`

```console
$ docker pull influxdb@sha256:0fd1969335adb2dd533c6c162720144c8b0648b7b51d274f0614b4b6e2b277fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8efe52dc0c6bdf7beb50f6d6930127e70e35152a5815894b2226749c135f5f15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58966047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4e803c566d11ac4423c3ef70f633de2d0b5dff2db4c62f7d55396470011bfc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:35:04 GMT
ENV INFLUXDB_VERSION=1.8.10
# Mon, 22 Aug 2022 20:22:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     chmod +x /usr/src/influxdb-*/influx              /usr/src/influxdb-*/influx_inspect              /usr/src/influxdb-*/influx_stress              /usr/src/influxdb-*/influxd &&    mv /usr/src/influxdb-*/influx        /usr/src/influxdb-*/influx_inspect        /usr/src/influxdb-*/influx_stress         /usr/src/influxdb-*/influxd        /usr/bin/ &&    gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 22 Aug 2022 20:22:30 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Mon, 22 Aug 2022 20:22:31 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:22:31 GMT
VOLUME [/var/lib/influxdb]
# Mon, 22 Aug 2022 20:22:31 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:22:31 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Mon, 22 Aug 2022 20:22:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:22:31 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f4276ac0611dbd0c24d15256d089c8f800d0de493d6f33365ad58522cfe70c`  
		Last Modified: Mon, 22 Aug 2022 20:25:22 GMT  
		Size: 54.6 MB (54647419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8a8bea3229b318ec1c61bcb11b414093cd653a2d2ff3d48e8224a282fb734c`  
		Last Modified: Mon, 22 Aug 2022 20:25:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e02f49aba4792edc976f8b9ab76f91d5980489c96f6129681bc1ebc3955a039`  
		Last Modified: Mon, 22 Aug 2022 20:25:15 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173d34f1771efd20aac74d07fbce7833bbb73a475a9e258128256676eb8b9f8f`  
		Last Modified: Mon, 22 Aug 2022 20:25:15 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-data`

```console
$ docker pull influxdb@sha256:96d2ba932c6f83edbd5a81a35f1fcbc29a453aac31360ffb7ece49f3a0fb6b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:428f0a943f4d1bb2821b1129b3f18cf70a863d0ee76bfb58b6b5b3b165a18ac2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127741811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdab6d751f8f38c2628ec4deb6338d9c17dfe13138e74ecb2f737e230802a5f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 03 Aug 2022 02:04:04 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 03 Aug 2022 02:04:09 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 03 Aug 2022 02:04:09 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 03 Aug 2022 02:04:09 GMT
EXPOSE 8086
# Wed, 03 Aug 2022 02:04:09 GMT
VOLUME [/var/lib/influxdb]
# Wed, 03 Aug 2022 02:04:10 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:04:10 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 03 Aug 2022 02:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:04:10 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c5bfaf0100c41f5215b47473f5f76d5aec8fbb92e515eff6e4037e1992288c`  
		Last Modified: Wed, 03 Aug 2022 02:06:43 GMT  
		Size: 56.7 MB (56705063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fecda5610f26727ec646dd115dbdeb639b2bfca3e6a099e10db99d96749cc9`  
		Last Modified: Wed, 03 Aug 2022 02:06:36 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c581908d052c6b5a0a693b80b21529731e1c859dfbf858e9c826d50d5f529b2`  
		Last Modified: Wed, 03 Aug 2022 02:06:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4195b4a1bce05cd25771565d8307ec366a139995c6cc09b606d8187dd997ec`  
		Last Modified: Wed, 03 Aug 2022 02:06:36 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-data-alpine`

```console
$ docker pull influxdb@sha256:3ae2d7877a2ca613d44fc532fdfd48feff4e80bea5346e0d10416d0ca6fb31a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c97c879631f76b6bc00095e53a9a5c30f15b9333611581458ba91ca0884f3469
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60822331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf7673e1fbd0a4bc7479f3211f3049aed4d80055fef6375acbcd1814832ea71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:35:16 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Tue, 09 Aug 2022 20:35:25 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 20:35:26 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 09 Aug 2022 20:35:26 GMT
EXPOSE 8086
# Tue, 09 Aug 2022 20:35:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Aug 2022 20:35:26 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 09 Aug 2022 20:35:26 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 09 Aug 2022 20:35:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 20:35:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660d3aa692c8b0d29b4e7e0ffac0a02c11599f26cc0bd002756e9e6b76108cd8`  
		Last Modified: Tue, 09 Aug 2022 20:38:42 GMT  
		Size: 56.5 MB (56503646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa39318d497281db1f9a02388ac2fd99a5e9ad63f66e041c00b44cbcf1759f23`  
		Last Modified: Tue, 09 Aug 2022 20:38:34 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32b49f32e3c793a399105f5b26a556202ced39b82314e099cb5a9a56ae3acb0`  
		Last Modified: Tue, 09 Aug 2022 20:38:34 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d76fd0d307652bc45d42778a79476cd91b78e515dd1b95714e35721de95fae`  
		Last Modified: Tue, 09 Aug 2022 20:38:34 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-meta`

```console
$ docker pull influxdb@sha256:5e345117ba9f8143da42364749f5fba2289c9a916ca5ef0688f3b1efa6b97d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3b7b709c16fcc6f1418f42ae901cdff9553eb2556a3ed39c1b94e0a53847d202
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94448300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269924d4772c2a43ff87d66fe3b3c36a9e5b728d1edc1b63b809cb07b2a268dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 03 Aug 2022 02:04:04 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 03 Aug 2022 02:04:17 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 03 Aug 2022 02:04:17 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 03 Aug 2022 02:04:17 GMT
EXPOSE 8091
# Wed, 03 Aug 2022 02:04:18 GMT
VOLUME [/var/lib/influxdb]
# Wed, 03 Aug 2022 02:04:18 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:04:18 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200d1c964c659220d3808f865050cb12346d90f4ef8b119143f59fc6f5380bf`  
		Last Modified: Wed, 03 Aug 2022 02:07:00 GMT  
		Size: 23.4 MB (23412758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9431f49f5357a73efefcea8ce35acb4a54df1b73b66c5ae29001e1294b836ef7`  
		Last Modified: Wed, 03 Aug 2022 02:06:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155e3e30f68132af9a5c0902bc1c7e817b709acf97e82f34c92b563f500339fd`  
		Last Modified: Wed, 03 Aug 2022 02:06:57 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-meta-alpine`

```console
$ docker pull influxdb@sha256:1bc53a804fca50ef4f8ff62269b97fc2f999f3f1b4b2c286b9a1d1e6252f1841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b2295d4b7e378ebe952bd3db3eee150fc33b5c432bc6bd6ed03b233d07764186
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27610491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daffb717093e5bdc9c615118ce300a424b46c357b7e071101f2a78ceb3ccc024`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:35:16 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Tue, 09 Aug 2022 20:35:36 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 20:35:36 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 09 Aug 2022 20:35:37 GMT
EXPOSE 8091
# Tue, 09 Aug 2022 20:35:37 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Aug 2022 20:35:37 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 09 Aug 2022 20:35:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 20:35:37 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85effd48049aab32e47b63df4632902515f5c87326ec4d45f173490d9040e308`  
		Last Modified: Tue, 09 Aug 2022 20:38:58 GMT  
		Size: 23.3 MB (23293005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83a163fb6c3d2277185ea1bd9a4aee51518e3d8b101a46364ffeb99db61367f`  
		Last Modified: Tue, 09 Aug 2022 20:38:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef0f697d368b5ad70ca2b594e9b44589e36b36e30957e81d64e7f960a99db90`  
		Last Modified: Tue, 09 Aug 2022 20:38:55 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-data`

```console
$ docker pull influxdb@sha256:ef8f81f9ccad06b06c2c19f1a64a35697515f82eac63a468a141c7916fcbd29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:d8f1050c829a6ddf729f12af8b82036dc037937421e78fe454b02bc81a5af4d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100657634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2fe49e3b6b7a23557991bf2c7ba5b6c9006e253cc9f7fd629e13ee38f24a31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 03 Aug 2022 02:04:22 GMT
ENV INFLUXDB_VERSION=1.9.8-c1.9.8
# Wed, 03 Aug 2022 02:04:27 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 03 Aug 2022 02:04:27 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 03 Aug 2022 02:04:27 GMT
EXPOSE 8086
# Wed, 03 Aug 2022 02:04:27 GMT
VOLUME [/var/lib/influxdb]
# Wed, 03 Aug 2022 02:04:27 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:04:27 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 03 Aug 2022 02:04:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:04:28 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bb3f335d411b6f23b1e617cf71735477cef0b53675b16ebc8b37441814cfc2`  
		Last Modified: Wed, 03 Aug 2022 02:07:19 GMT  
		Size: 29.6 MB (29620887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e591eee599d30a462b4b4457a2a6812cf4ddee787f348defd0baf4e8cc16dd9`  
		Last Modified: Wed, 03 Aug 2022 02:07:14 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fbcd7aec7b04825d0120b1384a181d53738a8d83658da4ff30c15dc5ee3f69`  
		Last Modified: Wed, 03 Aug 2022 02:07:14 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316e61e8423b43e98da1c0562c80af4481c4d65fc9df4a22bde4fdfc464a2946`  
		Last Modified: Wed, 03 Aug 2022 02:07:14 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-data-alpine`

```console
$ docker pull influxdb@sha256:0106cefa9a6b114900e7c183794e5894ae2a02b1e6fce457de4b670fbd75a688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:92fdbf355a282f1a087f2fe48d7876229b80dcdb3d31def0f97c22e2239b57a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33898851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab84d1c934bfe0d1e0d338ca09b7d90f224a11a1e6aced98071f36e881d40b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:35:41 GMT
ENV INFLUXDB_VERSION=1.9.8-c1.9.8
# Mon, 22 Aug 2022 20:22:49 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 22 Aug 2022 20:22:49 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Mon, 22 Aug 2022 20:22:49 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:22:49 GMT
VOLUME [/var/lib/influxdb]
# Mon, 22 Aug 2022 20:22:49 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:22:49 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Mon, 22 Aug 2022 20:22:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:22:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8ddc3f33134cc54782d543c0b059e635024dd78ab5175dcb185d2f0f4dbe7f`  
		Last Modified: Mon, 22 Aug 2022 20:25:45 GMT  
		Size: 29.6 MB (29580164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b68ba023a2533ebe1c957fc9b43a554accb0dde55dd062cba713e6b02f72e6f`  
		Last Modified: Mon, 22 Aug 2022 20:25:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a67c029eb1a9922b906fe423d9eb61c64062b17a5b68a35e55bac5681423314`  
		Last Modified: Mon, 22 Aug 2022 20:25:39 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e100624101290786f35a7b96c80ac8d8cb81a27a94533acaa9240f5dcb64a6`  
		Last Modified: Mon, 22 Aug 2022 20:25:39 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-meta`

```console
$ docker pull influxdb@sha256:142cc7d0d6e135f3f5a20d9bcda4db6fa53a9ba11df481f8f1d1068937f028d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3f2434d543c1abc751b1888146a1c8317f7d4981e715acbecaed75ee9af0a882
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82435638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5e459f10ff623030f2eb361f65bdca32c615152f276986251a364244b5ebfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 03 Aug 2022 02:04:22 GMT
ENV INFLUXDB_VERSION=1.9.8-c1.9.8
# Wed, 03 Aug 2022 02:04:35 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 03 Aug 2022 02:04:35 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 03 Aug 2022 02:04:35 GMT
EXPOSE 8091
# Wed, 03 Aug 2022 02:04:35 GMT
VOLUME [/var/lib/influxdb]
# Wed, 03 Aug 2022 02:04:36 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:04:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:04:36 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07294638d88b3dd359f56db96212f3ddff71e477cacbec4a4bf14bb02e69bd1c`  
		Last Modified: Wed, 03 Aug 2022 02:07:32 GMT  
		Size: 11.4 MB (11400097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82232585714f8678b1c76577aaa0f48a61ce92ce670423abea4bdf8f3c76e684`  
		Last Modified: Wed, 03 Aug 2022 02:07:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4843b6630483e29334a7f6e157ec2a80ada2db3af6fb6436d6f60226a02e6b`  
		Last Modified: Wed, 03 Aug 2022 02:07:30 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-meta-alpine`

```console
$ docker pull influxdb@sha256:3e123d5674e24bd00711c2aa83f7019a96d67e761c1e0a5580bad607a7ad9937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4e0585005f924dec5368ebe5697587f03cbfaeb88ba9930e87194056ed2c86e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15678995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c35cfd6abf8cbc8a6ff65c3ebb79a9a35d1658c144488cfbc74a72885914226`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:35:41 GMT
ENV INFLUXDB_VERSION=1.9.8-c1.9.8
# Mon, 22 Aug 2022 20:22:58 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 22 Aug 2022 20:22:58 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Mon, 22 Aug 2022 20:22:58 GMT
EXPOSE 8091
# Mon, 22 Aug 2022 20:22:58 GMT
VOLUME [/var/lib/influxdb]
# Mon, 22 Aug 2022 20:22:58 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:22:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:22:58 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bff7a5223c2733209f581df6a8db4fa7afd144cc145dd0fc97b4014db5ae1b`  
		Last Modified: Mon, 22 Aug 2022 20:25:57 GMT  
		Size: 11.4 MB (11361510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6423d66b652ee55e436e1d70efc4a52725152a46d0d420d9c7578f85069b366`  
		Last Modified: Mon, 22 Aug 2022 20:25:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c98f4c554bcb202e709da46a929f7bf80ea82dc944e13ca31552e5dc2cad5f9`  
		Last Modified: Mon, 22 Aug 2022 20:25:55 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.8-data`

```console
$ docker pull influxdb@sha256:ef8f81f9ccad06b06c2c19f1a64a35697515f82eac63a468a141c7916fcbd29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:d8f1050c829a6ddf729f12af8b82036dc037937421e78fe454b02bc81a5af4d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100657634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2fe49e3b6b7a23557991bf2c7ba5b6c9006e253cc9f7fd629e13ee38f24a31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 03 Aug 2022 02:04:22 GMT
ENV INFLUXDB_VERSION=1.9.8-c1.9.8
# Wed, 03 Aug 2022 02:04:27 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 03 Aug 2022 02:04:27 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 03 Aug 2022 02:04:27 GMT
EXPOSE 8086
# Wed, 03 Aug 2022 02:04:27 GMT
VOLUME [/var/lib/influxdb]
# Wed, 03 Aug 2022 02:04:27 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:04:27 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 03 Aug 2022 02:04:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:04:28 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bb3f335d411b6f23b1e617cf71735477cef0b53675b16ebc8b37441814cfc2`  
		Last Modified: Wed, 03 Aug 2022 02:07:19 GMT  
		Size: 29.6 MB (29620887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e591eee599d30a462b4b4457a2a6812cf4ddee787f348defd0baf4e8cc16dd9`  
		Last Modified: Wed, 03 Aug 2022 02:07:14 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fbcd7aec7b04825d0120b1384a181d53738a8d83658da4ff30c15dc5ee3f69`  
		Last Modified: Wed, 03 Aug 2022 02:07:14 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316e61e8423b43e98da1c0562c80af4481c4d65fc9df4a22bde4fdfc464a2946`  
		Last Modified: Wed, 03 Aug 2022 02:07:14 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.8-data-alpine`

```console
$ docker pull influxdb@sha256:0106cefa9a6b114900e7c183794e5894ae2a02b1e6fce457de4b670fbd75a688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:92fdbf355a282f1a087f2fe48d7876229b80dcdb3d31def0f97c22e2239b57a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33898851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab84d1c934bfe0d1e0d338ca09b7d90f224a11a1e6aced98071f36e881d40b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:35:41 GMT
ENV INFLUXDB_VERSION=1.9.8-c1.9.8
# Mon, 22 Aug 2022 20:22:49 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 22 Aug 2022 20:22:49 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Mon, 22 Aug 2022 20:22:49 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:22:49 GMT
VOLUME [/var/lib/influxdb]
# Mon, 22 Aug 2022 20:22:49 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:22:49 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Mon, 22 Aug 2022 20:22:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:22:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8ddc3f33134cc54782d543c0b059e635024dd78ab5175dcb185d2f0f4dbe7f`  
		Last Modified: Mon, 22 Aug 2022 20:25:45 GMT  
		Size: 29.6 MB (29580164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b68ba023a2533ebe1c957fc9b43a554accb0dde55dd062cba713e6b02f72e6f`  
		Last Modified: Mon, 22 Aug 2022 20:25:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a67c029eb1a9922b906fe423d9eb61c64062b17a5b68a35e55bac5681423314`  
		Last Modified: Mon, 22 Aug 2022 20:25:39 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e100624101290786f35a7b96c80ac8d8cb81a27a94533acaa9240f5dcb64a6`  
		Last Modified: Mon, 22 Aug 2022 20:25:39 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.8-meta`

```console
$ docker pull influxdb@sha256:142cc7d0d6e135f3f5a20d9bcda4db6fa53a9ba11df481f8f1d1068937f028d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3f2434d543c1abc751b1888146a1c8317f7d4981e715acbecaed75ee9af0a882
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82435638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5e459f10ff623030f2eb361f65bdca32c615152f276986251a364244b5ebfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 03 Aug 2022 02:04:22 GMT
ENV INFLUXDB_VERSION=1.9.8-c1.9.8
# Wed, 03 Aug 2022 02:04:35 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 03 Aug 2022 02:04:35 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 03 Aug 2022 02:04:35 GMT
EXPOSE 8091
# Wed, 03 Aug 2022 02:04:35 GMT
VOLUME [/var/lib/influxdb]
# Wed, 03 Aug 2022 02:04:36 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:04:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:04:36 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07294638d88b3dd359f56db96212f3ddff71e477cacbec4a4bf14bb02e69bd1c`  
		Last Modified: Wed, 03 Aug 2022 02:07:32 GMT  
		Size: 11.4 MB (11400097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82232585714f8678b1c76577aaa0f48a61ce92ce670423abea4bdf8f3c76e684`  
		Last Modified: Wed, 03 Aug 2022 02:07:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4843b6630483e29334a7f6e157ec2a80ada2db3af6fb6436d6f60226a02e6b`  
		Last Modified: Wed, 03 Aug 2022 02:07:30 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.8-meta-alpine`

```console
$ docker pull influxdb@sha256:3e123d5674e24bd00711c2aa83f7019a96d67e761c1e0a5580bad607a7ad9937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4e0585005f924dec5368ebe5697587f03cbfaeb88ba9930e87194056ed2c86e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15678995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c35cfd6abf8cbc8a6ff65c3ebb79a9a35d1658c144488cfbc74a72885914226`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:35:41 GMT
ENV INFLUXDB_VERSION=1.9.8-c1.9.8
# Mon, 22 Aug 2022 20:22:58 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/etc/influxdb/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 22 Aug 2022 20:22:58 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Mon, 22 Aug 2022 20:22:58 GMT
EXPOSE 8091
# Mon, 22 Aug 2022 20:22:58 GMT
VOLUME [/var/lib/influxdb]
# Mon, 22 Aug 2022 20:22:58 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:22:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:22:58 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bff7a5223c2733209f581df6a8db4fa7afd144cc145dd0fc97b4014db5ae1b`  
		Last Modified: Mon, 22 Aug 2022 20:25:57 GMT  
		Size: 11.4 MB (11361510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6423d66b652ee55e436e1d70efc4a52725152a46d0d420d9c7578f85069b366`  
		Last Modified: Mon, 22 Aug 2022 20:25:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c98f4c554bcb202e709da46a929f7bf80ea82dc944e13ca31552e5dc2cad5f9`  
		Last Modified: Mon, 22 Aug 2022 20:25:55 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.2`

```console
$ docker pull influxdb@sha256:cde3bfee9d8a6fc70f254644fea5350886d4d324446a69fd92c68883841c01a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.2` - linux; amd64

```console
$ docker pull influxdb@sha256:0f3ec3fb975e6001ddb9df90b7fefaeb7c85946b2032acca5da2618299bb9070
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181851558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bed58cd138d3b1a9c3a52e2d6d0a65495079523a191afaee9fcfd10ffa4b18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:48:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:04:40 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 03 Aug 2022 02:04:41 GMT
ENV GOSU_VER=1.12
# Wed, 03 Aug 2022 02:04:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Wed, 03 Aug 2022 02:05:01 GMT
ENV INFLUXDB_VERSION=2.2.0
# Wed, 03 Aug 2022 02:05:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 03 Aug 2022 02:05:10 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Wed, 03 Aug 2022 02:05:13 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 03 Aug 2022 02:05:14 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 03 Aug 2022 02:05:14 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 03 Aug 2022 02:05:14 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 03 Aug 2022 02:05:14 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:05:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:05:14 GMT
CMD ["influxd"]
# Wed, 03 Aug 2022 02:05:14 GMT
EXPOSE 8086
# Wed, 03 Aug 2022 02:05:14 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 03 Aug 2022 02:05:14 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 03 Aug 2022 02:05:15 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 03 Aug 2022 02:05:15 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe4e1c58b4af82939a918665dd1e7b5b636dd73c710b4bccb530edbb15470d2`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 7.9 MB (7856856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc915d298757b72963f0d061cc16ca4925e9f4481446b87a5297b4043ffc8033`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 10.0 MB (9998020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3d7f16384587e5b2713024237a979acb818cf5d1170a10733847d12297c86`  
		Last Modified: Wed, 03 Aug 2022 02:07:45 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dfe6b886df040caa48deed54f54000d2c9be265b2bdcf115eb9354b0bbe600`  
		Last Modified: Wed, 03 Aug 2022 02:07:45 GMT  
		Size: 961.0 KB (960957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14910ad68092c9b3a3316b7f01ec1516d760cedb984e3329bd3d7d263dd2197b`  
		Last Modified: Wed, 03 Aug 2022 02:08:10 GMT  
		Size: 107.2 MB (107220538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59593e414b32ab8bfec613de662028ff85e9be19a3334443f12332dc1aa9287c`  
		Last Modified: Wed, 03 Aug 2022 02:08:03 GMT  
		Size: 5.4 MB (5366855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6ffbb5c8347a91faf3fdb6af8540250792919747dbefbf646ab09fee0a5b3`  
		Last Modified: Wed, 03 Aug 2022 02:08:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9010bffaba6f1dcb51685bf1f7a79fca90770ada851f440ad5cf8cd77365f37`  
		Last Modified: Wed, 03 Aug 2022 02:08:02 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48af3f43641a772c3f02d9c40950b691c65583cb78c7d5dae1c7b737b1ae2fb8`  
		Last Modified: Wed, 03 Aug 2022 02:08:02 GMT  
		Size: 5.0 KB (5013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bdd0db2e4b469aa6ef9422f7596ae3007f8900acc5a564549d1e5e64b04befcd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182451687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c271c503eb0c4e4048b2f5e7c779e1d7b0f02e7e581c7b26c1a1ac294a91a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:25:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:25:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 22:43:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 02 Aug 2022 22:43:28 GMT
ENV GOSU_VER=1.12
# Tue, 02 Aug 2022 22:43:37 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Tue, 02 Aug 2022 22:44:15 GMT
ENV INFLUXDB_VERSION=2.2.0
# Tue, 02 Aug 2022 22:44:23 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Tue, 02 Aug 2022 22:44:23 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Tue, 02 Aug 2022 22:44:27 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Tue, 02 Aug 2022 22:44:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 02 Aug 2022 22:44:28 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 02 Aug 2022 22:44:30 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 02 Aug 2022 22:44:31 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Tue, 02 Aug 2022 22:44:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Aug 2022 22:44:32 GMT
CMD ["influxd"]
# Tue, 02 Aug 2022 22:44:33 GMT
EXPOSE 8086
# Tue, 02 Aug 2022 22:44:34 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 02 Aug 2022 22:44:35 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 02 Aug 2022 22:44:36 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 02 Aug 2022 22:44:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31ca5ccee8fca6610f14b5ed35ac33bb5f545532b6583e1461037a083c3d87b`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 7.7 MB (7719992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32de8e1f96ccb825d3be85704be7218044a19ff05ea1eea0222e8c942fbf6f8f`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 9.8 MB (9768645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8378fb3d56c5694f548622c9b57fa2f03ff1624a807548f4c01bce25fad6b571`  
		Last Modified: Tue, 02 Aug 2022 22:46:19 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092b709a97b7a0b81523c600a3f87245a3899a5ca52a86beb9e494dcce37903d`  
		Last Modified: Tue, 02 Aug 2022 22:46:19 GMT  
		Size: 896.3 KB (896336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe933c7e6fe8994bc778dd52e70bba692956327ab5b3094277ddd45bf51b1d2`  
		Last Modified: Tue, 02 Aug 2022 22:46:49 GMT  
		Size: 109.9 MB (109877911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7fab647a57eb0be0e3029ad6d845d04a088a2775328c5df8418137583603b5d`  
		Last Modified: Tue, 02 Aug 2022 22:46:40 GMT  
		Size: 5.0 MB (4952630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b856b28682aa545b302f7471515375e01917422a735c457dcabb0941d71986a0`  
		Last Modified: Tue, 02 Aug 2022 22:46:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a658cd002d3f07f8f0759cd393937b04b7d6c7df0a4cc178a2953de28522f11`  
		Last Modified: Tue, 02 Aug 2022 22:46:39 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d4254eb52aaf044de51eb156155a946bbd0c0d892a829261b70d3ba1c4e062`  
		Last Modified: Tue, 02 Aug 2022 22:46:39 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.2-alpine`

```console
$ docker pull influxdb@sha256:c27059a04e6e1069e1ebb67af2e3a4b5602914bfc8e40ecb31cd3e33f8eaedd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f3b54d91cae591fc3fde20299bd0b262f6f6d9a1f73b98d623b501e82c49d5fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125271216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd6d8fafd08d6d65f94dfb0df4bfcca35d130c9efed70857db547dbc5ddba45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:23:24 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:23:25 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:23:25 GMT
ENV INFLUXDB_VERSION=2.2.0
# Mon, 22 Aug 2022 20:23:34 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:23:34 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Mon, 22 Aug 2022 20:23:37 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:23:38 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:23:38 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:23:39 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:23:39 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:23:39 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:23:39 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:23:39 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:23:39 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6402af9050b861838e26160dfa36debcd6dd6475ea0fd83bca7456ce75a5b625`  
		Last Modified: Mon, 22 Aug 2022 20:26:43 GMT  
		Size: 9.8 MB (9849332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e48e1ebaf1c86c438b7e1a5c14b907d4df63562a822fbdc21e2463a6d2dbf`  
		Last Modified: Mon, 22 Aug 2022 20:26:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b040377b8b5acd01e7e84bde888f68e50dcafdd8c66c0c20111dad9be87739`  
		Last Modified: Mon, 22 Aug 2022 20:26:47 GMT  
		Size: 107.2 MB (107220556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6a2ded64055386f1d1b6bdfca4aeb66949fd4f02041b275a2dd0818066d886`  
		Last Modified: Mon, 22 Aug 2022 20:26:40 GMT  
		Size: 5.4 MB (5366860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea454e365c2b0850d4f706a365eb346f6d31146c4e14fbb105b438c55609d41a`  
		Last Modified: Mon, 22 Aug 2022 20:26:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822d25c5189fd957f1538caa0417b36769603ba8386dd1defb1aa1cb7f7135dd`  
		Last Modified: Mon, 22 Aug 2022 20:26:39 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3138291a465d8aba6501a3d6c5232c89488ed9d695635e8a51b36efee048592b`  
		Last Modified: Mon, 22 Aug 2022 20:26:39 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4eed02a9e39b8fb5764aa936f4195b104499e4080c664f65b5c1787a45f2d3f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127246073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e39be6512bb1e82497fc301bd9a1d2bc2e7aa5a62b5f9b72c2d77207c30123`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:37:19 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:40:08 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:40:09 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:40:10 GMT
ENV INFLUXDB_VERSION=2.2.0
# Mon, 22 Aug 2022 20:40:22 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:40:22 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Mon, 22 Aug 2022 20:40:26 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:40:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:40:28 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:40:30 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:40:31 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:40:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:40:32 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:40:33 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:40:34 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:40:35 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:40:36 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:40:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d115c2e84067616c51d32a9aa355071965e141dcaab8f8a8b3d26939dab269`  
		Last Modified: Tue, 09 Aug 2022 20:39:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c4a50852ded4220bf7f48c74a648463f1cbaa41d1e64945009b0ab04ab97c`  
		Last Modified: Mon, 22 Aug 2022 20:43:04 GMT  
		Size: 9.7 MB (9686496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8279c4c64bc9372a4413cb0c0b4a8fcec42038f48bceba1672521f1cf362a277`  
		Last Modified: Mon, 22 Aug 2022 20:43:02 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b964a455be031b752191befbb7c05593801a613630849641d716ffe5d0a8321a`  
		Last Modified: Mon, 22 Aug 2022 20:43:09 GMT  
		Size: 109.9 MB (109877941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924dd5ff08376fa262e04b05736e922c21146a0f5a0772d5a38d09a08d5ae7c7`  
		Last Modified: Mon, 22 Aug 2022 20:43:01 GMT  
		Size: 5.0 MB (4952626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a48aef9a4bc27690c5497fd09a07db7e9359c08dffa75cad68ba6b21d420be3`  
		Last Modified: Mon, 22 Aug 2022 20:43:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cb047d81471641cbaab9d699c9852b8d43e535a62b0b7028d3bcfd71702535`  
		Last Modified: Mon, 22 Aug 2022 20:43:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a18886a2debb965c7637aeb4d9c063b3391b8838d864ce52bc273c7df361a2e`  
		Last Modified: Mon, 22 Aug 2022 20:43:01 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.2.0`

```console
$ docker pull influxdb@sha256:cde3bfee9d8a6fc70f254644fea5350886d4d324446a69fd92c68883841c01a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.2.0` - linux; amd64

```console
$ docker pull influxdb@sha256:0f3ec3fb975e6001ddb9df90b7fefaeb7c85946b2032acca5da2618299bb9070
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181851558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bed58cd138d3b1a9c3a52e2d6d0a65495079523a191afaee9fcfd10ffa4b18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:48:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:04:40 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 03 Aug 2022 02:04:41 GMT
ENV GOSU_VER=1.12
# Wed, 03 Aug 2022 02:04:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Wed, 03 Aug 2022 02:05:01 GMT
ENV INFLUXDB_VERSION=2.2.0
# Wed, 03 Aug 2022 02:05:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 03 Aug 2022 02:05:10 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Wed, 03 Aug 2022 02:05:13 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 03 Aug 2022 02:05:14 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 03 Aug 2022 02:05:14 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 03 Aug 2022 02:05:14 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 03 Aug 2022 02:05:14 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:05:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:05:14 GMT
CMD ["influxd"]
# Wed, 03 Aug 2022 02:05:14 GMT
EXPOSE 8086
# Wed, 03 Aug 2022 02:05:14 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 03 Aug 2022 02:05:14 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 03 Aug 2022 02:05:15 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 03 Aug 2022 02:05:15 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe4e1c58b4af82939a918665dd1e7b5b636dd73c710b4bccb530edbb15470d2`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 7.9 MB (7856856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc915d298757b72963f0d061cc16ca4925e9f4481446b87a5297b4043ffc8033`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 10.0 MB (9998020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3d7f16384587e5b2713024237a979acb818cf5d1170a10733847d12297c86`  
		Last Modified: Wed, 03 Aug 2022 02:07:45 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dfe6b886df040caa48deed54f54000d2c9be265b2bdcf115eb9354b0bbe600`  
		Last Modified: Wed, 03 Aug 2022 02:07:45 GMT  
		Size: 961.0 KB (960957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14910ad68092c9b3a3316b7f01ec1516d760cedb984e3329bd3d7d263dd2197b`  
		Last Modified: Wed, 03 Aug 2022 02:08:10 GMT  
		Size: 107.2 MB (107220538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59593e414b32ab8bfec613de662028ff85e9be19a3334443f12332dc1aa9287c`  
		Last Modified: Wed, 03 Aug 2022 02:08:03 GMT  
		Size: 5.4 MB (5366855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6ffbb5c8347a91faf3fdb6af8540250792919747dbefbf646ab09fee0a5b3`  
		Last Modified: Wed, 03 Aug 2022 02:08:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9010bffaba6f1dcb51685bf1f7a79fca90770ada851f440ad5cf8cd77365f37`  
		Last Modified: Wed, 03 Aug 2022 02:08:02 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48af3f43641a772c3f02d9c40950b691c65583cb78c7d5dae1c7b737b1ae2fb8`  
		Last Modified: Wed, 03 Aug 2022 02:08:02 GMT  
		Size: 5.0 KB (5013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.2.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bdd0db2e4b469aa6ef9422f7596ae3007f8900acc5a564549d1e5e64b04befcd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182451687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c271c503eb0c4e4048b2f5e7c779e1d7b0f02e7e581c7b26c1a1ac294a91a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:25:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:25:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 22:43:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 02 Aug 2022 22:43:28 GMT
ENV GOSU_VER=1.12
# Tue, 02 Aug 2022 22:43:37 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Tue, 02 Aug 2022 22:44:15 GMT
ENV INFLUXDB_VERSION=2.2.0
# Tue, 02 Aug 2022 22:44:23 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Tue, 02 Aug 2022 22:44:23 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Tue, 02 Aug 2022 22:44:27 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Tue, 02 Aug 2022 22:44:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 02 Aug 2022 22:44:28 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 02 Aug 2022 22:44:30 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 02 Aug 2022 22:44:31 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Tue, 02 Aug 2022 22:44:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Aug 2022 22:44:32 GMT
CMD ["influxd"]
# Tue, 02 Aug 2022 22:44:33 GMT
EXPOSE 8086
# Tue, 02 Aug 2022 22:44:34 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 02 Aug 2022 22:44:35 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 02 Aug 2022 22:44:36 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 02 Aug 2022 22:44:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31ca5ccee8fca6610f14b5ed35ac33bb5f545532b6583e1461037a083c3d87b`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 7.7 MB (7719992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32de8e1f96ccb825d3be85704be7218044a19ff05ea1eea0222e8c942fbf6f8f`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 9.8 MB (9768645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8378fb3d56c5694f548622c9b57fa2f03ff1624a807548f4c01bce25fad6b571`  
		Last Modified: Tue, 02 Aug 2022 22:46:19 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092b709a97b7a0b81523c600a3f87245a3899a5ca52a86beb9e494dcce37903d`  
		Last Modified: Tue, 02 Aug 2022 22:46:19 GMT  
		Size: 896.3 KB (896336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe933c7e6fe8994bc778dd52e70bba692956327ab5b3094277ddd45bf51b1d2`  
		Last Modified: Tue, 02 Aug 2022 22:46:49 GMT  
		Size: 109.9 MB (109877911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7fab647a57eb0be0e3029ad6d845d04a088a2775328c5df8418137583603b5d`  
		Last Modified: Tue, 02 Aug 2022 22:46:40 GMT  
		Size: 5.0 MB (4952630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b856b28682aa545b302f7471515375e01917422a735c457dcabb0941d71986a0`  
		Last Modified: Tue, 02 Aug 2022 22:46:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a658cd002d3f07f8f0759cd393937b04b7d6c7df0a4cc178a2953de28522f11`  
		Last Modified: Tue, 02 Aug 2022 22:46:39 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d4254eb52aaf044de51eb156155a946bbd0c0d892a829261b70d3ba1c4e062`  
		Last Modified: Tue, 02 Aug 2022 22:46:39 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.2.0-alpine`

```console
$ docker pull influxdb@sha256:c27059a04e6e1069e1ebb67af2e3a4b5602914bfc8e40ecb31cd3e33f8eaedd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.2.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f3b54d91cae591fc3fde20299bd0b262f6f6d9a1f73b98d623b501e82c49d5fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125271216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd6d8fafd08d6d65f94dfb0df4bfcca35d130c9efed70857db547dbc5ddba45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:23:24 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:23:25 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:23:25 GMT
ENV INFLUXDB_VERSION=2.2.0
# Mon, 22 Aug 2022 20:23:34 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:23:34 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Mon, 22 Aug 2022 20:23:37 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:23:38 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:23:38 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:23:39 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:23:39 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:23:39 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:23:39 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:23:39 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:23:39 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6402af9050b861838e26160dfa36debcd6dd6475ea0fd83bca7456ce75a5b625`  
		Last Modified: Mon, 22 Aug 2022 20:26:43 GMT  
		Size: 9.8 MB (9849332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e48e1ebaf1c86c438b7e1a5c14b907d4df63562a822fbdc21e2463a6d2dbf`  
		Last Modified: Mon, 22 Aug 2022 20:26:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b040377b8b5acd01e7e84bde888f68e50dcafdd8c66c0c20111dad9be87739`  
		Last Modified: Mon, 22 Aug 2022 20:26:47 GMT  
		Size: 107.2 MB (107220556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6a2ded64055386f1d1b6bdfca4aeb66949fd4f02041b275a2dd0818066d886`  
		Last Modified: Mon, 22 Aug 2022 20:26:40 GMT  
		Size: 5.4 MB (5366860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea454e365c2b0850d4f706a365eb346f6d31146c4e14fbb105b438c55609d41a`  
		Last Modified: Mon, 22 Aug 2022 20:26:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822d25c5189fd957f1538caa0417b36769603ba8386dd1defb1aa1cb7f7135dd`  
		Last Modified: Mon, 22 Aug 2022 20:26:39 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3138291a465d8aba6501a3d6c5232c89488ed9d695635e8a51b36efee048592b`  
		Last Modified: Mon, 22 Aug 2022 20:26:39 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.2.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4eed02a9e39b8fb5764aa936f4195b104499e4080c664f65b5c1787a45f2d3f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127246073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e39be6512bb1e82497fc301bd9a1d2bc2e7aa5a62b5f9b72c2d77207c30123`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:37:19 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:40:08 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:40:09 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:40:10 GMT
ENV INFLUXDB_VERSION=2.2.0
# Mon, 22 Aug 2022 20:40:22 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:40:22 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Mon, 22 Aug 2022 20:40:26 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:40:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:40:28 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:40:30 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:40:31 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:40:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:40:32 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:40:33 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:40:34 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:40:35 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:40:36 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:40:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d115c2e84067616c51d32a9aa355071965e141dcaab8f8a8b3d26939dab269`  
		Last Modified: Tue, 09 Aug 2022 20:39:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c4a50852ded4220bf7f48c74a648463f1cbaa41d1e64945009b0ab04ab97c`  
		Last Modified: Mon, 22 Aug 2022 20:43:04 GMT  
		Size: 9.7 MB (9686496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8279c4c64bc9372a4413cb0c0b4a8fcec42038f48bceba1672521f1cf362a277`  
		Last Modified: Mon, 22 Aug 2022 20:43:02 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b964a455be031b752191befbb7c05593801a613630849641d716ffe5d0a8321a`  
		Last Modified: Mon, 22 Aug 2022 20:43:09 GMT  
		Size: 109.9 MB (109877941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924dd5ff08376fa262e04b05736e922c21146a0f5a0772d5a38d09a08d5ae7c7`  
		Last Modified: Mon, 22 Aug 2022 20:43:01 GMT  
		Size: 5.0 MB (4952626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a48aef9a4bc27690c5497fd09a07db7e9359c08dffa75cad68ba6b21d420be3`  
		Last Modified: Mon, 22 Aug 2022 20:43:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cb047d81471641cbaab9d699c9852b8d43e535a62b0b7028d3bcfd71702535`  
		Last Modified: Mon, 22 Aug 2022 20:43:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a18886a2debb965c7637aeb4d9c063b3391b8838d864ce52bc273c7df361a2e`  
		Last Modified: Mon, 22 Aug 2022 20:43:01 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.3`

```console
$ docker pull influxdb@sha256:f90f1bda60f6db2d8ef1c61eac55d86d542451fb4c2e6e190f64fda9f85a468b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.3` - linux; amd64

```console
$ docker pull influxdb@sha256:be9343aaee11a28413511991ae44b11d64cdfa8ca2d7b1a383662d1af56daa2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255109706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0458c4356aa6b7d5249a13df29cb8ecc4d8b8468d3e6f7689c2a1433d36a132e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:48:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:04:40 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 03 Aug 2022 02:04:41 GMT
ENV GOSU_VER=1.12
# Wed, 03 Aug 2022 02:04:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Wed, 03 Aug 2022 02:05:20 GMT
ENV INFLUXDB_VERSION=2.3.0
# Wed, 03 Aug 2022 02:05:27 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 03 Aug 2022 02:05:27 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Wed, 03 Aug 2022 02:05:30 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 03 Aug 2022 02:05:31 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 03 Aug 2022 02:05:31 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 03 Aug 2022 02:05:31 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 03 Aug 2022 02:05:31 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:05:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:05:31 GMT
CMD ["influxd"]
# Wed, 03 Aug 2022 02:05:32 GMT
EXPOSE 8086
# Wed, 03 Aug 2022 02:05:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 03 Aug 2022 02:05:32 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 03 Aug 2022 02:05:32 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 03 Aug 2022 02:05:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe4e1c58b4af82939a918665dd1e7b5b636dd73c710b4bccb530edbb15470d2`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 7.9 MB (7856856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc915d298757b72963f0d061cc16ca4925e9f4481446b87a5297b4043ffc8033`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 10.0 MB (9998020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3d7f16384587e5b2713024237a979acb818cf5d1170a10733847d12297c86`  
		Last Modified: Wed, 03 Aug 2022 02:07:45 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dfe6b886df040caa48deed54f54000d2c9be265b2bdcf115eb9354b0bbe600`  
		Last Modified: Wed, 03 Aug 2022 02:07:45 GMT  
		Size: 961.0 KB (960957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e41d3761dd486fe1a434d05f15f8c6688d0fb90f99c879a1deb247bb8d67fe`  
		Last Modified: Wed, 03 Aug 2022 02:08:39 GMT  
		Size: 180.5 MB (180478682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2df79bbb0553afa811b5da9fd4a437f0a4bc3ba61fe29b2a69d98e23255f1c`  
		Last Modified: Wed, 03 Aug 2022 02:08:27 GMT  
		Size: 5.4 MB (5366855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0896686d78a120fea820c5a4b0d3347a3f6a9eb62b79f68e79e0ba7f315dad52`  
		Last Modified: Wed, 03 Aug 2022 02:08:27 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a722dc73e43e76046ffe757161aef52e6ac4a69b78fd9e5e87622b79110b3ad`  
		Last Modified: Wed, 03 Aug 2022 02:08:27 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0065159929d050506385ecea7d1671a145484af85bf999d31cbc4b2ae5ce160`  
		Last Modified: Wed, 03 Aug 2022 02:08:26 GMT  
		Size: 5.0 KB (5016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.3` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8a76932ada97fa381fa608b9436c924b2cd361b37a0955274a4cf8a341018dd2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253366217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934a6120cd876dc8fec6bd799ad918b7908533a258ddf61570bd22b684724da6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:25:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:25:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 22:43:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 02 Aug 2022 22:43:28 GMT
ENV GOSU_VER=1.12
# Tue, 02 Aug 2022 22:43:37 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Tue, 02 Aug 2022 22:44:50 GMT
ENV INFLUXDB_VERSION=2.3.0
# Tue, 02 Aug 2022 22:45:00 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Tue, 02 Aug 2022 22:45:01 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Tue, 02 Aug 2022 22:45:04 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Tue, 02 Aug 2022 22:45:05 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 02 Aug 2022 22:45:06 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 02 Aug 2022 22:45:08 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 02 Aug 2022 22:45:09 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Tue, 02 Aug 2022 22:45:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Aug 2022 22:45:10 GMT
CMD ["influxd"]
# Tue, 02 Aug 2022 22:45:11 GMT
EXPOSE 8086
# Tue, 02 Aug 2022 22:45:12 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 02 Aug 2022 22:45:13 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 02 Aug 2022 22:45:14 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 02 Aug 2022 22:45:15 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31ca5ccee8fca6610f14b5ed35ac33bb5f545532b6583e1461037a083c3d87b`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 7.7 MB (7719992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32de8e1f96ccb825d3be85704be7218044a19ff05ea1eea0222e8c942fbf6f8f`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 9.8 MB (9768645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8378fb3d56c5694f548622c9b57fa2f03ff1624a807548f4c01bce25fad6b571`  
		Last Modified: Tue, 02 Aug 2022 22:46:19 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092b709a97b7a0b81523c600a3f87245a3899a5ca52a86beb9e494dcce37903d`  
		Last Modified: Tue, 02 Aug 2022 22:46:19 GMT  
		Size: 896.3 KB (896336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4870cc0010a33207e631c9b15c816b6902cd0156d56ef8fa177c05fcd8965dca`  
		Last Modified: Tue, 02 Aug 2022 22:47:17 GMT  
		Size: 180.8 MB (180792442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5039f2de6ef31ea22211447d7d8d65f04cf1c0988963e52abff9795e407dfcfb`  
		Last Modified: Tue, 02 Aug 2022 22:47:03 GMT  
		Size: 5.0 MB (4952630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbc11d359af7d17fe9e54a3b384e00a496909e02b3c891496976d87599f9b80`  
		Last Modified: Tue, 02 Aug 2022 22:47:02 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36635655046d7471cb368b40d3fd0dd40a5debbe4b8e469984bd43478d628dae`  
		Last Modified: Tue, 02 Aug 2022 22:47:02 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6028b5b1e0d46991ba5429b26871d1f354de5aab63377d6bff04ffb311763b7`  
		Last Modified: Tue, 02 Aug 2022 22:47:02 GMT  
		Size: 5.0 KB (5013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.3-alpine`

```console
$ docker pull influxdb@sha256:362f614ea31cda29f820a125dc4fae94f48a0156da7f890d0b7a6dd68a9b445a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.3-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a8922160b8a4372f0d84f9720caee252b6de8378b48552a95de491ec278e4635
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198529290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cbf5e22f21fea51de882df79efc238b545fc8efd3b0269a81177feee236d2c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:23:24 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:23:25 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:23:44 GMT
ENV INFLUXDB_VERSION=2.3.0
# Mon, 22 Aug 2022 20:23:51 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:23:52 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Mon, 22 Aug 2022 20:23:55 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:23:55 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:23:55 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:23:55 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:23:55 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:23:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:23:56 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:23:56 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:23:56 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:23:56 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:23:56 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:23:56 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6402af9050b861838e26160dfa36debcd6dd6475ea0fd83bca7456ce75a5b625`  
		Last Modified: Mon, 22 Aug 2022 20:26:43 GMT  
		Size: 9.8 MB (9849332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e48e1ebaf1c86c438b7e1a5c14b907d4df63562a822fbdc21e2463a6d2dbf`  
		Last Modified: Mon, 22 Aug 2022 20:26:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd476b1b47490f505b607364334029547f95e8e7752153cbb81fd4be226ae13`  
		Last Modified: Mon, 22 Aug 2022 20:27:11 GMT  
		Size: 180.5 MB (180478621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c8ced105f1c13f3021b13254a6ccf60c5c1c5e628886cc4fe7c19c7ff64dcb`  
		Last Modified: Mon, 22 Aug 2022 20:26:59 GMT  
		Size: 5.4 MB (5366868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b657ad2643cfb6fd141e137fd9e1fe9e3a14ae3745a6da4a01fe4d124cd86213`  
		Last Modified: Mon, 22 Aug 2022 20:26:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a26a3547057bcc934954828c7f0472f61c2963a2d5ee848f49e1f69bb3327d1`  
		Last Modified: Mon, 22 Aug 2022 20:26:58 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6884cfd8ab752cbdb3c91ec4b5915d377d56f0190e286a3583c45c1e1ac45ebb`  
		Last Modified: Mon, 22 Aug 2022 20:26:58 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.3-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b56a8d30891b4ed59c1fe4cac2f0042d745eb95f63f1a1861dbcfbc1c6478c6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198160542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9095ecc8220964331c04a01acbba9e0cd1ae422ced482e7831710f477fde3b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:37:19 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:40:08 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:40:09 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:40:47 GMT
ENV INFLUXDB_VERSION=2.3.0
# Mon, 22 Aug 2022 20:41:03 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:41:03 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Mon, 22 Aug 2022 20:41:06 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:41:07 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:41:08 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:41:10 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:41:11 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:41:12 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:41:13 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:41:14 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:41:15 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:41:16 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:41:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d115c2e84067616c51d32a9aa355071965e141dcaab8f8a8b3d26939dab269`  
		Last Modified: Tue, 09 Aug 2022 20:39:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c4a50852ded4220bf7f48c74a648463f1cbaa41d1e64945009b0ab04ab97c`  
		Last Modified: Mon, 22 Aug 2022 20:43:04 GMT  
		Size: 9.7 MB (9686496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8279c4c64bc9372a4413cb0c0b4a8fcec42038f48bceba1672521f1cf362a277`  
		Last Modified: Mon, 22 Aug 2022 20:43:02 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9820298a9496926caa09329751eb724022580ae84ce1cafbfd1a0e47fa227fe8`  
		Last Modified: Mon, 22 Aug 2022 20:43:36 GMT  
		Size: 180.8 MB (180792403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e853e2fea33bedcafb331531f1243a608f2508afc7b718cc8a012c17d8bd4e5`  
		Last Modified: Mon, 22 Aug 2022 20:43:22 GMT  
		Size: 5.0 MB (4952634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5246659574b4dd9d3e77319f2327f068755e891823e55bdc91b44a1a8f1003`  
		Last Modified: Mon, 22 Aug 2022 20:43:22 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454ac9077d73973eee1e5ba9dcccc5ea90ef46dd851af12ddc04efedbf9a262b`  
		Last Modified: Mon, 22 Aug 2022 20:43:22 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4557fa8b2f50e5b1c3aca79df601f9a6a6db7fad0cf3d95d2a63e72f0c89795b`  
		Last Modified: Mon, 22 Aug 2022 20:43:22 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.3.0`

```console
$ docker pull influxdb@sha256:f90f1bda60f6db2d8ef1c61eac55d86d542451fb4c2e6e190f64fda9f85a468b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.3.0` - linux; amd64

```console
$ docker pull influxdb@sha256:be9343aaee11a28413511991ae44b11d64cdfa8ca2d7b1a383662d1af56daa2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255109706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0458c4356aa6b7d5249a13df29cb8ecc4d8b8468d3e6f7689c2a1433d36a132e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:48:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:04:40 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 03 Aug 2022 02:04:41 GMT
ENV GOSU_VER=1.12
# Wed, 03 Aug 2022 02:04:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Wed, 03 Aug 2022 02:05:20 GMT
ENV INFLUXDB_VERSION=2.3.0
# Wed, 03 Aug 2022 02:05:27 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 03 Aug 2022 02:05:27 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Wed, 03 Aug 2022 02:05:30 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 03 Aug 2022 02:05:31 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 03 Aug 2022 02:05:31 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 03 Aug 2022 02:05:31 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 03 Aug 2022 02:05:31 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:05:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:05:31 GMT
CMD ["influxd"]
# Wed, 03 Aug 2022 02:05:32 GMT
EXPOSE 8086
# Wed, 03 Aug 2022 02:05:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 03 Aug 2022 02:05:32 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 03 Aug 2022 02:05:32 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 03 Aug 2022 02:05:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe4e1c58b4af82939a918665dd1e7b5b636dd73c710b4bccb530edbb15470d2`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 7.9 MB (7856856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc915d298757b72963f0d061cc16ca4925e9f4481446b87a5297b4043ffc8033`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 10.0 MB (9998020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3d7f16384587e5b2713024237a979acb818cf5d1170a10733847d12297c86`  
		Last Modified: Wed, 03 Aug 2022 02:07:45 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dfe6b886df040caa48deed54f54000d2c9be265b2bdcf115eb9354b0bbe600`  
		Last Modified: Wed, 03 Aug 2022 02:07:45 GMT  
		Size: 961.0 KB (960957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e41d3761dd486fe1a434d05f15f8c6688d0fb90f99c879a1deb247bb8d67fe`  
		Last Modified: Wed, 03 Aug 2022 02:08:39 GMT  
		Size: 180.5 MB (180478682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2df79bbb0553afa811b5da9fd4a437f0a4bc3ba61fe29b2a69d98e23255f1c`  
		Last Modified: Wed, 03 Aug 2022 02:08:27 GMT  
		Size: 5.4 MB (5366855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0896686d78a120fea820c5a4b0d3347a3f6a9eb62b79f68e79e0ba7f315dad52`  
		Last Modified: Wed, 03 Aug 2022 02:08:27 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a722dc73e43e76046ffe757161aef52e6ac4a69b78fd9e5e87622b79110b3ad`  
		Last Modified: Wed, 03 Aug 2022 02:08:27 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0065159929d050506385ecea7d1671a145484af85bf999d31cbc4b2ae5ce160`  
		Last Modified: Wed, 03 Aug 2022 02:08:26 GMT  
		Size: 5.0 KB (5016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.3.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8a76932ada97fa381fa608b9436c924b2cd361b37a0955274a4cf8a341018dd2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253366217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934a6120cd876dc8fec6bd799ad918b7908533a258ddf61570bd22b684724da6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:25:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:25:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 22:43:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 02 Aug 2022 22:43:28 GMT
ENV GOSU_VER=1.12
# Tue, 02 Aug 2022 22:43:37 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Tue, 02 Aug 2022 22:44:50 GMT
ENV INFLUXDB_VERSION=2.3.0
# Tue, 02 Aug 2022 22:45:00 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Tue, 02 Aug 2022 22:45:01 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Tue, 02 Aug 2022 22:45:04 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Tue, 02 Aug 2022 22:45:05 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 02 Aug 2022 22:45:06 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 02 Aug 2022 22:45:08 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 02 Aug 2022 22:45:09 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Tue, 02 Aug 2022 22:45:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Aug 2022 22:45:10 GMT
CMD ["influxd"]
# Tue, 02 Aug 2022 22:45:11 GMT
EXPOSE 8086
# Tue, 02 Aug 2022 22:45:12 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 02 Aug 2022 22:45:13 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 02 Aug 2022 22:45:14 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 02 Aug 2022 22:45:15 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31ca5ccee8fca6610f14b5ed35ac33bb5f545532b6583e1461037a083c3d87b`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 7.7 MB (7719992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32de8e1f96ccb825d3be85704be7218044a19ff05ea1eea0222e8c942fbf6f8f`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 9.8 MB (9768645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8378fb3d56c5694f548622c9b57fa2f03ff1624a807548f4c01bce25fad6b571`  
		Last Modified: Tue, 02 Aug 2022 22:46:19 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092b709a97b7a0b81523c600a3f87245a3899a5ca52a86beb9e494dcce37903d`  
		Last Modified: Tue, 02 Aug 2022 22:46:19 GMT  
		Size: 896.3 KB (896336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4870cc0010a33207e631c9b15c816b6902cd0156d56ef8fa177c05fcd8965dca`  
		Last Modified: Tue, 02 Aug 2022 22:47:17 GMT  
		Size: 180.8 MB (180792442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5039f2de6ef31ea22211447d7d8d65f04cf1c0988963e52abff9795e407dfcfb`  
		Last Modified: Tue, 02 Aug 2022 22:47:03 GMT  
		Size: 5.0 MB (4952630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbc11d359af7d17fe9e54a3b384e00a496909e02b3c891496976d87599f9b80`  
		Last Modified: Tue, 02 Aug 2022 22:47:02 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36635655046d7471cb368b40d3fd0dd40a5debbe4b8e469984bd43478d628dae`  
		Last Modified: Tue, 02 Aug 2022 22:47:02 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6028b5b1e0d46991ba5429b26871d1f354de5aab63377d6bff04ffb311763b7`  
		Last Modified: Tue, 02 Aug 2022 22:47:02 GMT  
		Size: 5.0 KB (5013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.3.0-alpine`

```console
$ docker pull influxdb@sha256:362f614ea31cda29f820a125dc4fae94f48a0156da7f890d0b7a6dd68a9b445a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.3.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a8922160b8a4372f0d84f9720caee252b6de8378b48552a95de491ec278e4635
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198529290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cbf5e22f21fea51de882df79efc238b545fc8efd3b0269a81177feee236d2c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:23:24 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:23:25 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:23:44 GMT
ENV INFLUXDB_VERSION=2.3.0
# Mon, 22 Aug 2022 20:23:51 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:23:52 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Mon, 22 Aug 2022 20:23:55 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:23:55 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:23:55 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:23:55 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:23:55 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:23:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:23:56 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:23:56 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:23:56 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:23:56 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:23:56 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:23:56 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6402af9050b861838e26160dfa36debcd6dd6475ea0fd83bca7456ce75a5b625`  
		Last Modified: Mon, 22 Aug 2022 20:26:43 GMT  
		Size: 9.8 MB (9849332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e48e1ebaf1c86c438b7e1a5c14b907d4df63562a822fbdc21e2463a6d2dbf`  
		Last Modified: Mon, 22 Aug 2022 20:26:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd476b1b47490f505b607364334029547f95e8e7752153cbb81fd4be226ae13`  
		Last Modified: Mon, 22 Aug 2022 20:27:11 GMT  
		Size: 180.5 MB (180478621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c8ced105f1c13f3021b13254a6ccf60c5c1c5e628886cc4fe7c19c7ff64dcb`  
		Last Modified: Mon, 22 Aug 2022 20:26:59 GMT  
		Size: 5.4 MB (5366868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b657ad2643cfb6fd141e137fd9e1fe9e3a14ae3745a6da4a01fe4d124cd86213`  
		Last Modified: Mon, 22 Aug 2022 20:26:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a26a3547057bcc934954828c7f0472f61c2963a2d5ee848f49e1f69bb3327d1`  
		Last Modified: Mon, 22 Aug 2022 20:26:58 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6884cfd8ab752cbdb3c91ec4b5915d377d56f0190e286a3583c45c1e1ac45ebb`  
		Last Modified: Mon, 22 Aug 2022 20:26:58 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.3.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b56a8d30891b4ed59c1fe4cac2f0042d745eb95f63f1a1861dbcfbc1c6478c6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198160542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9095ecc8220964331c04a01acbba9e0cd1ae422ced482e7831710f477fde3b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:37:19 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:40:08 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:40:09 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:40:47 GMT
ENV INFLUXDB_VERSION=2.3.0
# Mon, 22 Aug 2022 20:41:03 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:41:03 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Mon, 22 Aug 2022 20:41:06 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:41:07 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:41:08 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:41:10 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:41:11 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:41:12 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:41:13 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:41:14 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:41:15 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:41:16 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:41:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d115c2e84067616c51d32a9aa355071965e141dcaab8f8a8b3d26939dab269`  
		Last Modified: Tue, 09 Aug 2022 20:39:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c4a50852ded4220bf7f48c74a648463f1cbaa41d1e64945009b0ab04ab97c`  
		Last Modified: Mon, 22 Aug 2022 20:43:04 GMT  
		Size: 9.7 MB (9686496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8279c4c64bc9372a4413cb0c0b4a8fcec42038f48bceba1672521f1cf362a277`  
		Last Modified: Mon, 22 Aug 2022 20:43:02 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9820298a9496926caa09329751eb724022580ae84ce1cafbfd1a0e47fa227fe8`  
		Last Modified: Mon, 22 Aug 2022 20:43:36 GMT  
		Size: 180.8 MB (180792403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e853e2fea33bedcafb331531f1243a608f2508afc7b718cc8a012c17d8bd4e5`  
		Last Modified: Mon, 22 Aug 2022 20:43:22 GMT  
		Size: 5.0 MB (4952634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5246659574b4dd9d3e77319f2327f068755e891823e55bdc91b44a1a8f1003`  
		Last Modified: Mon, 22 Aug 2022 20:43:22 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454ac9077d73973eee1e5ba9dcccc5ea90ef46dd851af12ddc04efedbf9a262b`  
		Last Modified: Mon, 22 Aug 2022 20:43:22 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4557fa8b2f50e5b1c3aca79df601f9a6a6db7fad0cf3d95d2a63e72f0c89795b`  
		Last Modified: Mon, 22 Aug 2022 20:43:22 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.4`

```console
$ docker pull influxdb@sha256:7054b633d0fafbd75620b0f9e2457b925309c3ec00fc7d3e099b4c2fd161414a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.4` - linux; amd64

```console
$ docker pull influxdb@sha256:68e5154224adf14d8c613f5828cf17803d184d25277e1acb4ab39a7edf6e2549
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261137286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0fe0105a7cbb0399396ebfedcb5155a2bee762a194fbf40eb8d75711b8b9b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:48:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:04:40 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 03 Aug 2022 02:04:41 GMT
ENV GOSU_VER=1.12
# Wed, 03 Aug 2022 02:04:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Mon, 22 Aug 2022 20:24:00 GMT
ENV INFLUXDB_VERSION=2.4.0
# Mon, 22 Aug 2022 20:24:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:24:09 GMT
ENV INFLUX_CLI_VERSION=2.4.0
# Mon, 22 Aug 2022 20:24:12 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:24:13 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:24:13 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:24:13 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:24:13 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:24:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:24:13 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:24:13 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:24:13 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:24:14 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:24:14 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:24:14 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe4e1c58b4af82939a918665dd1e7b5b636dd73c710b4bccb530edbb15470d2`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 7.9 MB (7856856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc915d298757b72963f0d061cc16ca4925e9f4481446b87a5297b4043ffc8033`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 10.0 MB (9998020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3d7f16384587e5b2713024237a979acb818cf5d1170a10733847d12297c86`  
		Last Modified: Wed, 03 Aug 2022 02:07:45 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dfe6b886df040caa48deed54f54000d2c9be265b2bdcf115eb9354b0bbe600`  
		Last Modified: Wed, 03 Aug 2022 02:07:45 GMT  
		Size: 961.0 KB (960957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1348d27a351d0ff0a11057d1da52e74456c6feb59f4a733795a131b5e36841e2`  
		Last Modified: Mon, 22 Aug 2022 20:27:35 GMT  
		Size: 185.8 MB (185802073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b706abeaeda2d358b4d7ccaa115b2febab7b7efdf855e8c459b19cc122c70359`  
		Last Modified: Mon, 22 Aug 2022 20:27:22 GMT  
		Size: 6.1 MB (6071046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3d50d00efd9194f617a61987c863815cfc60072b02b6a69e73f8b731dc1a9d`  
		Last Modified: Mon, 22 Aug 2022 20:27:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70d5662fe5a0ec7bf27936707de08ef56c67e197069056ce8e1da953f431b85`  
		Last Modified: Mon, 22 Aug 2022 20:27:21 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2b8d4f2197b9d484045c1bdc22cf63d94e7f1db35ef9275fbfed99dbb53747`  
		Last Modified: Mon, 22 Aug 2022 20:27:21 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.4` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c2fe1e06d17610d8f2422ca4f1846e225dedc1aa45ea5f3d20fb3d82c4046910
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255667242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7de96884448e034a4d36f235cede3d449fafea85ab2194134c60f437cb4182`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:25:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:25:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 22:43:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 02 Aug 2022 22:43:28 GMT
ENV GOSU_VER=1.12
# Tue, 02 Aug 2022 22:43:37 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Mon, 22 Aug 2022 20:41:23 GMT
ENV INFLUXDB_VERSION=2.4.0
# Mon, 22 Aug 2022 20:41:38 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:41:38 GMT
ENV INFLUX_CLI_VERSION=2.4.0
# Mon, 22 Aug 2022 20:41:43 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:41:44 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:41:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:41:47 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:41:48 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:41:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:41:49 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:41:50 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:41:51 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:41:52 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:41:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:41:54 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31ca5ccee8fca6610f14b5ed35ac33bb5f545532b6583e1461037a083c3d87b`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 7.7 MB (7719992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32de8e1f96ccb825d3be85704be7218044a19ff05ea1eea0222e8c942fbf6f8f`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 9.8 MB (9768645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8378fb3d56c5694f548622c9b57fa2f03ff1624a807548f4c01bce25fad6b571`  
		Last Modified: Tue, 02 Aug 2022 22:46:19 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092b709a97b7a0b81523c600a3f87245a3899a5ca52a86beb9e494dcce37903d`  
		Last Modified: Tue, 02 Aug 2022 22:46:19 GMT  
		Size: 896.3 KB (896336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0727c0f998a37b509a2cd0a6e9034dbbcea608f987536e6679b401cdf80442bd`  
		Last Modified: Mon, 22 Aug 2022 20:44:02 GMT  
		Size: 182.4 MB (182445455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c682f5df917d280bf06330302bed8362e13c8b352d982f96b6e29ddec1c1776e`  
		Last Modified: Mon, 22 Aug 2022 20:43:48 GMT  
		Size: 5.6 MB (5600641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5946861b5151652c39d733ff50717d6feed030f789a2ce1b11c3608dc9981f26`  
		Last Modified: Mon, 22 Aug 2022 20:43:47 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387314dde02e17c968f8021658d9d6d84ee61c8eff09e1ee7045a0b1096ca998`  
		Last Modified: Mon, 22 Aug 2022 20:43:47 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a42d8f46084bd204bf033534e88cd4ba6fbc2aced7918e3f5901dda042901e`  
		Last Modified: Mon, 22 Aug 2022 20:43:47 GMT  
		Size: 5.0 KB (5016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.4-alpine`

```console
$ docker pull influxdb@sha256:7cdfd116b08d0858766446468612a7d1b508f6eedda09167372c37e8b0abed29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.4-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6f0508f1834cc0eeeba394618b9e3fac6c279cd83b46ef80f3c6569989a03851
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204556947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00fe993fbb4c3a647e8a8d605112e71bf4ebcd9dd42ed3902ece5e5877a5cea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:23:24 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:23:25 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:24:17 GMT
ENV INFLUXDB_VERSION=2.4.0
# Mon, 22 Aug 2022 20:24:24 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:24:25 GMT
ENV INFLUX_CLI_VERSION=2.4.0
# Mon, 22 Aug 2022 20:24:27 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:24:28 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:24:28 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:24:28 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:24:28 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:24:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:24:28 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:24:28 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:24:29 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:24:29 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:24:29 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:24:29 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6402af9050b861838e26160dfa36debcd6dd6475ea0fd83bca7456ce75a5b625`  
		Last Modified: Mon, 22 Aug 2022 20:26:43 GMT  
		Size: 9.8 MB (9849332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e48e1ebaf1c86c438b7e1a5c14b907d4df63562a822fbdc21e2463a6d2dbf`  
		Last Modified: Mon, 22 Aug 2022 20:26:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6090bd6322587c0389ad7e821fc1b220abaa84fea246f6fc17b8da6536b75e06`  
		Last Modified: Mon, 22 Aug 2022 20:28:02 GMT  
		Size: 185.8 MB (185802071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f074e0862a2ae8b98660ed0eab954a18e20ab7244bbad52291249de2dbbd21`  
		Last Modified: Mon, 22 Aug 2022 20:27:49 GMT  
		Size: 6.1 MB (6071078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d0edd1fdfd0ad366e3d01eca9ac9ddcde5cdbcc27823f5735bfbc7ab26dd39`  
		Last Modified: Mon, 22 Aug 2022 20:27:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0ad10eabd449a6d520dd27ebeac3f5db06e0ec3b5ad83cbf321efbc3b663a0`  
		Last Modified: Mon, 22 Aug 2022 20:27:48 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248077695501b84babac21af1f23c1fc9e595b111dffbb8657f9b00f90d95897`  
		Last Modified: Mon, 22 Aug 2022 20:27:48 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.4-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:aec00d1d3bdd04865834b2ce5efbf9eb0087dd974fbfda851c9edf17bcd86ca1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 MB (200461612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9316463e8a256e525078cb0fd4cc1f9a559a00caf6276cc33dbef40a980a9068`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:37:19 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:40:08 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:40:09 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:42:00 GMT
ENV INFLUXDB_VERSION=2.4.0
# Mon, 22 Aug 2022 20:42:07 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:42:07 GMT
ENV INFLUX_CLI_VERSION=2.4.0
# Mon, 22 Aug 2022 20:42:10 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:42:11 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:42:12 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:42:14 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:42:15 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:42:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:42:16 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:42:17 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:42:19 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:42:20 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:42:21 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d115c2e84067616c51d32a9aa355071965e141dcaab8f8a8b3d26939dab269`  
		Last Modified: Tue, 09 Aug 2022 20:39:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c4a50852ded4220bf7f48c74a648463f1cbaa41d1e64945009b0ab04ab97c`  
		Last Modified: Mon, 22 Aug 2022 20:43:04 GMT  
		Size: 9.7 MB (9686496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8279c4c64bc9372a4413cb0c0b4a8fcec42038f48bceba1672521f1cf362a277`  
		Last Modified: Mon, 22 Aug 2022 20:43:02 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7297eb6832b83766a5181e62614f8bcb8e572cef2eaab4b32ea5164aff056eb9`  
		Last Modified: Mon, 22 Aug 2022 20:44:31 GMT  
		Size: 182.4 MB (182445450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a937fb0ab9fb1127943c02b2132570f00067589a6e9ad4f88e12b0f897227b`  
		Last Modified: Mon, 22 Aug 2022 20:44:17 GMT  
		Size: 5.6 MB (5600655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25361e1233670c2910e01baa942181c9bcecef679384f6176ef71c9052e1dde`  
		Last Modified: Mon, 22 Aug 2022 20:44:16 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d265faea80360c2fc8079279fe00a752e7ca06dd60c3ccc9d9bb05e59dc1dd`  
		Last Modified: Mon, 22 Aug 2022 20:44:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b117a445a9fe39c2069cc8b0d5818dc0a8f82a977ae2a05740bee4e09460cb`  
		Last Modified: Mon, 22 Aug 2022 20:44:16 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.4.0`

```console
$ docker pull influxdb@sha256:7054b633d0fafbd75620b0f9e2457b925309c3ec00fc7d3e099b4c2fd161414a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.4.0` - linux; amd64

```console
$ docker pull influxdb@sha256:68e5154224adf14d8c613f5828cf17803d184d25277e1acb4ab39a7edf6e2549
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261137286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0fe0105a7cbb0399396ebfedcb5155a2bee762a194fbf40eb8d75711b8b9b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:48:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:04:40 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 03 Aug 2022 02:04:41 GMT
ENV GOSU_VER=1.12
# Wed, 03 Aug 2022 02:04:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Mon, 22 Aug 2022 20:24:00 GMT
ENV INFLUXDB_VERSION=2.4.0
# Mon, 22 Aug 2022 20:24:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:24:09 GMT
ENV INFLUX_CLI_VERSION=2.4.0
# Mon, 22 Aug 2022 20:24:12 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:24:13 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:24:13 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:24:13 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:24:13 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:24:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:24:13 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:24:13 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:24:13 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:24:14 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:24:14 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:24:14 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe4e1c58b4af82939a918665dd1e7b5b636dd73c710b4bccb530edbb15470d2`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 7.9 MB (7856856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc915d298757b72963f0d061cc16ca4925e9f4481446b87a5297b4043ffc8033`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 10.0 MB (9998020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3d7f16384587e5b2713024237a979acb818cf5d1170a10733847d12297c86`  
		Last Modified: Wed, 03 Aug 2022 02:07:45 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dfe6b886df040caa48deed54f54000d2c9be265b2bdcf115eb9354b0bbe600`  
		Last Modified: Wed, 03 Aug 2022 02:07:45 GMT  
		Size: 961.0 KB (960957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1348d27a351d0ff0a11057d1da52e74456c6feb59f4a733795a131b5e36841e2`  
		Last Modified: Mon, 22 Aug 2022 20:27:35 GMT  
		Size: 185.8 MB (185802073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b706abeaeda2d358b4d7ccaa115b2febab7b7efdf855e8c459b19cc122c70359`  
		Last Modified: Mon, 22 Aug 2022 20:27:22 GMT  
		Size: 6.1 MB (6071046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3d50d00efd9194f617a61987c863815cfc60072b02b6a69e73f8b731dc1a9d`  
		Last Modified: Mon, 22 Aug 2022 20:27:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70d5662fe5a0ec7bf27936707de08ef56c67e197069056ce8e1da953f431b85`  
		Last Modified: Mon, 22 Aug 2022 20:27:21 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2b8d4f2197b9d484045c1bdc22cf63d94e7f1db35ef9275fbfed99dbb53747`  
		Last Modified: Mon, 22 Aug 2022 20:27:21 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.4.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c2fe1e06d17610d8f2422ca4f1846e225dedc1aa45ea5f3d20fb3d82c4046910
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255667242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7de96884448e034a4d36f235cede3d449fafea85ab2194134c60f437cb4182`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:25:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:25:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 22:43:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 02 Aug 2022 22:43:28 GMT
ENV GOSU_VER=1.12
# Tue, 02 Aug 2022 22:43:37 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Mon, 22 Aug 2022 20:41:23 GMT
ENV INFLUXDB_VERSION=2.4.0
# Mon, 22 Aug 2022 20:41:38 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:41:38 GMT
ENV INFLUX_CLI_VERSION=2.4.0
# Mon, 22 Aug 2022 20:41:43 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:41:44 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:41:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:41:47 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:41:48 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:41:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:41:49 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:41:50 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:41:51 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:41:52 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:41:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:41:54 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31ca5ccee8fca6610f14b5ed35ac33bb5f545532b6583e1461037a083c3d87b`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 7.7 MB (7719992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32de8e1f96ccb825d3be85704be7218044a19ff05ea1eea0222e8c942fbf6f8f`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 9.8 MB (9768645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8378fb3d56c5694f548622c9b57fa2f03ff1624a807548f4c01bce25fad6b571`  
		Last Modified: Tue, 02 Aug 2022 22:46:19 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092b709a97b7a0b81523c600a3f87245a3899a5ca52a86beb9e494dcce37903d`  
		Last Modified: Tue, 02 Aug 2022 22:46:19 GMT  
		Size: 896.3 KB (896336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0727c0f998a37b509a2cd0a6e9034dbbcea608f987536e6679b401cdf80442bd`  
		Last Modified: Mon, 22 Aug 2022 20:44:02 GMT  
		Size: 182.4 MB (182445455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c682f5df917d280bf06330302bed8362e13c8b352d982f96b6e29ddec1c1776e`  
		Last Modified: Mon, 22 Aug 2022 20:43:48 GMT  
		Size: 5.6 MB (5600641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5946861b5151652c39d733ff50717d6feed030f789a2ce1b11c3608dc9981f26`  
		Last Modified: Mon, 22 Aug 2022 20:43:47 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387314dde02e17c968f8021658d9d6d84ee61c8eff09e1ee7045a0b1096ca998`  
		Last Modified: Mon, 22 Aug 2022 20:43:47 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a42d8f46084bd204bf033534e88cd4ba6fbc2aced7918e3f5901dda042901e`  
		Last Modified: Mon, 22 Aug 2022 20:43:47 GMT  
		Size: 5.0 KB (5016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.4.0-alpine`

```console
$ docker pull influxdb@sha256:7cdfd116b08d0858766446468612a7d1b508f6eedda09167372c37e8b0abed29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.4.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6f0508f1834cc0eeeba394618b9e3fac6c279cd83b46ef80f3c6569989a03851
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204556947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00fe993fbb4c3a647e8a8d605112e71bf4ebcd9dd42ed3902ece5e5877a5cea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:23:24 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:23:25 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:24:17 GMT
ENV INFLUXDB_VERSION=2.4.0
# Mon, 22 Aug 2022 20:24:24 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:24:25 GMT
ENV INFLUX_CLI_VERSION=2.4.0
# Mon, 22 Aug 2022 20:24:27 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:24:28 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:24:28 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:24:28 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:24:28 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:24:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:24:28 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:24:28 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:24:29 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:24:29 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:24:29 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:24:29 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6402af9050b861838e26160dfa36debcd6dd6475ea0fd83bca7456ce75a5b625`  
		Last Modified: Mon, 22 Aug 2022 20:26:43 GMT  
		Size: 9.8 MB (9849332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e48e1ebaf1c86c438b7e1a5c14b907d4df63562a822fbdc21e2463a6d2dbf`  
		Last Modified: Mon, 22 Aug 2022 20:26:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6090bd6322587c0389ad7e821fc1b220abaa84fea246f6fc17b8da6536b75e06`  
		Last Modified: Mon, 22 Aug 2022 20:28:02 GMT  
		Size: 185.8 MB (185802071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f074e0862a2ae8b98660ed0eab954a18e20ab7244bbad52291249de2dbbd21`  
		Last Modified: Mon, 22 Aug 2022 20:27:49 GMT  
		Size: 6.1 MB (6071078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d0edd1fdfd0ad366e3d01eca9ac9ddcde5cdbcc27823f5735bfbc7ab26dd39`  
		Last Modified: Mon, 22 Aug 2022 20:27:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0ad10eabd449a6d520dd27ebeac3f5db06e0ec3b5ad83cbf321efbc3b663a0`  
		Last Modified: Mon, 22 Aug 2022 20:27:48 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248077695501b84babac21af1f23c1fc9e595b111dffbb8657f9b00f90d95897`  
		Last Modified: Mon, 22 Aug 2022 20:27:48 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.4.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:aec00d1d3bdd04865834b2ce5efbf9eb0087dd974fbfda851c9edf17bcd86ca1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 MB (200461612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9316463e8a256e525078cb0fd4cc1f9a559a00caf6276cc33dbef40a980a9068`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:37:19 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:40:08 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:40:09 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:42:00 GMT
ENV INFLUXDB_VERSION=2.4.0
# Mon, 22 Aug 2022 20:42:07 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:42:07 GMT
ENV INFLUX_CLI_VERSION=2.4.0
# Mon, 22 Aug 2022 20:42:10 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:42:11 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:42:12 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:42:14 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:42:15 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:42:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:42:16 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:42:17 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:42:19 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:42:20 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:42:21 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d115c2e84067616c51d32a9aa355071965e141dcaab8f8a8b3d26939dab269`  
		Last Modified: Tue, 09 Aug 2022 20:39:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c4a50852ded4220bf7f48c74a648463f1cbaa41d1e64945009b0ab04ab97c`  
		Last Modified: Mon, 22 Aug 2022 20:43:04 GMT  
		Size: 9.7 MB (9686496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8279c4c64bc9372a4413cb0c0b4a8fcec42038f48bceba1672521f1cf362a277`  
		Last Modified: Mon, 22 Aug 2022 20:43:02 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7297eb6832b83766a5181e62614f8bcb8e572cef2eaab4b32ea5164aff056eb9`  
		Last Modified: Mon, 22 Aug 2022 20:44:31 GMT  
		Size: 182.4 MB (182445450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a937fb0ab9fb1127943c02b2132570f00067589a6e9ad4f88e12b0f897227b`  
		Last Modified: Mon, 22 Aug 2022 20:44:17 GMT  
		Size: 5.6 MB (5600655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25361e1233670c2910e01baa942181c9bcecef679384f6176ef71c9052e1dde`  
		Last Modified: Mon, 22 Aug 2022 20:44:16 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d265faea80360c2fc8079279fe00a752e7ca06dd60c3ccc9d9bb05e59dc1dd`  
		Last Modified: Mon, 22 Aug 2022 20:44:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b117a445a9fe39c2069cc8b0d5818dc0a8f82a977ae2a05740bee4e09460cb`  
		Last Modified: Mon, 22 Aug 2022 20:44:16 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:7cdfd116b08d0858766446468612a7d1b508f6eedda09167372c37e8b0abed29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6f0508f1834cc0eeeba394618b9e3fac6c279cd83b46ef80f3c6569989a03851
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204556947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00fe993fbb4c3a647e8a8d605112e71bf4ebcd9dd42ed3902ece5e5877a5cea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:23:24 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:23:25 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:24:17 GMT
ENV INFLUXDB_VERSION=2.4.0
# Mon, 22 Aug 2022 20:24:24 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:24:25 GMT
ENV INFLUX_CLI_VERSION=2.4.0
# Mon, 22 Aug 2022 20:24:27 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:24:28 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:24:28 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:24:28 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:24:28 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:24:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:24:28 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:24:28 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:24:29 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:24:29 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:24:29 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:24:29 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6402af9050b861838e26160dfa36debcd6dd6475ea0fd83bca7456ce75a5b625`  
		Last Modified: Mon, 22 Aug 2022 20:26:43 GMT  
		Size: 9.8 MB (9849332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e48e1ebaf1c86c438b7e1a5c14b907d4df63562a822fbdc21e2463a6d2dbf`  
		Last Modified: Mon, 22 Aug 2022 20:26:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6090bd6322587c0389ad7e821fc1b220abaa84fea246f6fc17b8da6536b75e06`  
		Last Modified: Mon, 22 Aug 2022 20:28:02 GMT  
		Size: 185.8 MB (185802071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f074e0862a2ae8b98660ed0eab954a18e20ab7244bbad52291249de2dbbd21`  
		Last Modified: Mon, 22 Aug 2022 20:27:49 GMT  
		Size: 6.1 MB (6071078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d0edd1fdfd0ad366e3d01eca9ac9ddcde5cdbcc27823f5735bfbc7ab26dd39`  
		Last Modified: Mon, 22 Aug 2022 20:27:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0ad10eabd449a6d520dd27ebeac3f5db06e0ec3b5ad83cbf321efbc3b663a0`  
		Last Modified: Mon, 22 Aug 2022 20:27:48 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248077695501b84babac21af1f23c1fc9e595b111dffbb8657f9b00f90d95897`  
		Last Modified: Mon, 22 Aug 2022 20:27:48 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:aec00d1d3bdd04865834b2ce5efbf9eb0087dd974fbfda851c9edf17bcd86ca1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 MB (200461612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9316463e8a256e525078cb0fd4cc1f9a559a00caf6276cc33dbef40a980a9068`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:37:19 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:40:08 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:40:09 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:42:00 GMT
ENV INFLUXDB_VERSION=2.4.0
# Mon, 22 Aug 2022 20:42:07 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:42:07 GMT
ENV INFLUX_CLI_VERSION=2.4.0
# Mon, 22 Aug 2022 20:42:10 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:42:11 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:42:12 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:42:14 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:42:15 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:42:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:42:16 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:42:17 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:42:19 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:42:20 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:42:21 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d115c2e84067616c51d32a9aa355071965e141dcaab8f8a8b3d26939dab269`  
		Last Modified: Tue, 09 Aug 2022 20:39:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c4a50852ded4220bf7f48c74a648463f1cbaa41d1e64945009b0ab04ab97c`  
		Last Modified: Mon, 22 Aug 2022 20:43:04 GMT  
		Size: 9.7 MB (9686496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8279c4c64bc9372a4413cb0c0b4a8fcec42038f48bceba1672521f1cf362a277`  
		Last Modified: Mon, 22 Aug 2022 20:43:02 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7297eb6832b83766a5181e62614f8bcb8e572cef2eaab4b32ea5164aff056eb9`  
		Last Modified: Mon, 22 Aug 2022 20:44:31 GMT  
		Size: 182.4 MB (182445450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a937fb0ab9fb1127943c02b2132570f00067589a6e9ad4f88e12b0f897227b`  
		Last Modified: Mon, 22 Aug 2022 20:44:17 GMT  
		Size: 5.6 MB (5600655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25361e1233670c2910e01baa942181c9bcecef679384f6176ef71c9052e1dde`  
		Last Modified: Mon, 22 Aug 2022 20:44:16 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d265faea80360c2fc8079279fe00a752e7ca06dd60c3ccc9d9bb05e59dc1dd`  
		Last Modified: Mon, 22 Aug 2022 20:44:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b117a445a9fe39c2069cc8b0d5818dc0a8f82a977ae2a05740bee4e09460cb`  
		Last Modified: Mon, 22 Aug 2022 20:44:16 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data`

```console
$ docker pull influxdb@sha256:96d2ba932c6f83edbd5a81a35f1fcbc29a453aac31360ffb7ece49f3a0fb6b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:428f0a943f4d1bb2821b1129b3f18cf70a863d0ee76bfb58b6b5b3b165a18ac2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127741811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdab6d751f8f38c2628ec4deb6338d9c17dfe13138e74ecb2f737e230802a5f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 03 Aug 2022 02:04:04 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 03 Aug 2022 02:04:09 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 03 Aug 2022 02:04:09 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 03 Aug 2022 02:04:09 GMT
EXPOSE 8086
# Wed, 03 Aug 2022 02:04:09 GMT
VOLUME [/var/lib/influxdb]
# Wed, 03 Aug 2022 02:04:10 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:04:10 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 03 Aug 2022 02:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:04:10 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c5bfaf0100c41f5215b47473f5f76d5aec8fbb92e515eff6e4037e1992288c`  
		Last Modified: Wed, 03 Aug 2022 02:06:43 GMT  
		Size: 56.7 MB (56705063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fecda5610f26727ec646dd115dbdeb639b2bfca3e6a099e10db99d96749cc9`  
		Last Modified: Wed, 03 Aug 2022 02:06:36 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c581908d052c6b5a0a693b80b21529731e1c859dfbf858e9c826d50d5f529b2`  
		Last Modified: Wed, 03 Aug 2022 02:06:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4195b4a1bce05cd25771565d8307ec366a139995c6cc09b606d8187dd997ec`  
		Last Modified: Wed, 03 Aug 2022 02:06:36 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:3ae2d7877a2ca613d44fc532fdfd48feff4e80bea5346e0d10416d0ca6fb31a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c97c879631f76b6bc00095e53a9a5c30f15b9333611581458ba91ca0884f3469
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60822331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf7673e1fbd0a4bc7479f3211f3049aed4d80055fef6375acbcd1814832ea71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:35:16 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Tue, 09 Aug 2022 20:35:25 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 20:35:26 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 09 Aug 2022 20:35:26 GMT
EXPOSE 8086
# Tue, 09 Aug 2022 20:35:26 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Aug 2022 20:35:26 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 09 Aug 2022 20:35:26 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 09 Aug 2022 20:35:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 20:35:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660d3aa692c8b0d29b4e7e0ffac0a02c11599f26cc0bd002756e9e6b76108cd8`  
		Last Modified: Tue, 09 Aug 2022 20:38:42 GMT  
		Size: 56.5 MB (56503646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa39318d497281db1f9a02388ac2fd99a5e9ad63f66e041c00b44cbcf1759f23`  
		Last Modified: Tue, 09 Aug 2022 20:38:34 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32b49f32e3c793a399105f5b26a556202ced39b82314e099cb5a9a56ae3acb0`  
		Last Modified: Tue, 09 Aug 2022 20:38:34 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d76fd0d307652bc45d42778a79476cd91b78e515dd1b95714e35721de95fae`  
		Last Modified: Tue, 09 Aug 2022 20:38:34 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:7054b633d0fafbd75620b0f9e2457b925309c3ec00fc7d3e099b4c2fd161414a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:68e5154224adf14d8c613f5828cf17803d184d25277e1acb4ab39a7edf6e2549
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261137286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0fe0105a7cbb0399396ebfedcb5155a2bee762a194fbf40eb8d75711b8b9b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:48:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:04:40 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 03 Aug 2022 02:04:41 GMT
ENV GOSU_VER=1.12
# Wed, 03 Aug 2022 02:04:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Mon, 22 Aug 2022 20:24:00 GMT
ENV INFLUXDB_VERSION=2.4.0
# Mon, 22 Aug 2022 20:24:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:24:09 GMT
ENV INFLUX_CLI_VERSION=2.4.0
# Mon, 22 Aug 2022 20:24:12 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:24:13 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:24:13 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:24:13 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:24:13 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:24:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:24:13 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:24:13 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:24:13 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:24:14 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:24:14 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:24:14 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe4e1c58b4af82939a918665dd1e7b5b636dd73c710b4bccb530edbb15470d2`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 7.9 MB (7856856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc915d298757b72963f0d061cc16ca4925e9f4481446b87a5297b4043ffc8033`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 10.0 MB (9998020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae3d7f16384587e5b2713024237a979acb818cf5d1170a10733847d12297c86`  
		Last Modified: Wed, 03 Aug 2022 02:07:45 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dfe6b886df040caa48deed54f54000d2c9be265b2bdcf115eb9354b0bbe600`  
		Last Modified: Wed, 03 Aug 2022 02:07:45 GMT  
		Size: 961.0 KB (960957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1348d27a351d0ff0a11057d1da52e74456c6feb59f4a733795a131b5e36841e2`  
		Last Modified: Mon, 22 Aug 2022 20:27:35 GMT  
		Size: 185.8 MB (185802073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b706abeaeda2d358b4d7ccaa115b2febab7b7efdf855e8c459b19cc122c70359`  
		Last Modified: Mon, 22 Aug 2022 20:27:22 GMT  
		Size: 6.1 MB (6071046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3d50d00efd9194f617a61987c863815cfc60072b02b6a69e73f8b731dc1a9d`  
		Last Modified: Mon, 22 Aug 2022 20:27:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70d5662fe5a0ec7bf27936707de08ef56c67e197069056ce8e1da953f431b85`  
		Last Modified: Mon, 22 Aug 2022 20:27:21 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2b8d4f2197b9d484045c1bdc22cf63d94e7f1db35ef9275fbfed99dbb53747`  
		Last Modified: Mon, 22 Aug 2022 20:27:21 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c2fe1e06d17610d8f2422ca4f1846e225dedc1aa45ea5f3d20fb3d82c4046910
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255667242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7de96884448e034a4d36f235cede3d449fafea85ab2194134c60f437cb4182`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:25:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:25:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 22:43:27 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 02 Aug 2022 22:43:28 GMT
ENV GOSU_VER=1.12
# Tue, 02 Aug 2022 22:43:37 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Mon, 22 Aug 2022 20:41:23 GMT
ENV INFLUXDB_VERSION=2.4.0
# Mon, 22 Aug 2022 20:41:38 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:41:38 GMT
ENV INFLUX_CLI_VERSION=2.4.0
# Mon, 22 Aug 2022 20:41:43 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:41:44 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:41:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:41:47 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:41:48 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:41:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:41:49 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:41:50 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:41:51 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:41:52 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:41:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:41:54 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31ca5ccee8fca6610f14b5ed35ac33bb5f545532b6583e1461037a083c3d87b`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 7.7 MB (7719992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32de8e1f96ccb825d3be85704be7218044a19ff05ea1eea0222e8c942fbf6f8f`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 9.8 MB (9768645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8378fb3d56c5694f548622c9b57fa2f03ff1624a807548f4c01bce25fad6b571`  
		Last Modified: Tue, 02 Aug 2022 22:46:19 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092b709a97b7a0b81523c600a3f87245a3899a5ca52a86beb9e494dcce37903d`  
		Last Modified: Tue, 02 Aug 2022 22:46:19 GMT  
		Size: 896.3 KB (896336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0727c0f998a37b509a2cd0a6e9034dbbcea608f987536e6679b401cdf80442bd`  
		Last Modified: Mon, 22 Aug 2022 20:44:02 GMT  
		Size: 182.4 MB (182445455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c682f5df917d280bf06330302bed8362e13c8b352d982f96b6e29ddec1c1776e`  
		Last Modified: Mon, 22 Aug 2022 20:43:48 GMT  
		Size: 5.6 MB (5600641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5946861b5151652c39d733ff50717d6feed030f789a2ce1b11c3608dc9981f26`  
		Last Modified: Mon, 22 Aug 2022 20:43:47 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387314dde02e17c968f8021658d9d6d84ee61c8eff09e1ee7045a0b1096ca998`  
		Last Modified: Mon, 22 Aug 2022 20:43:47 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a42d8f46084bd204bf033534e88cd4ba6fbc2aced7918e3f5901dda042901e`  
		Last Modified: Mon, 22 Aug 2022 20:43:47 GMT  
		Size: 5.0 KB (5016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:5e345117ba9f8143da42364749f5fba2289c9a916ca5ef0688f3b1efa6b97d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3b7b709c16fcc6f1418f42ae901cdff9553eb2556a3ed39c1b94e0a53847d202
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94448300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269924d4772c2a43ff87d66fe3b3c36a9e5b728d1edc1b63b809cb07b2a268dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 02 Aug 2022 01:19:54 GMT
ADD file:d0f758e50c654c225f6c7f03e8a579efc9106437051573bdbae5e63b1c4b2c1f in / 
# Tue, 02 Aug 2022 01:19:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:46:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 03 Aug 2022 02:03:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 03 Aug 2022 02:04:04 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 03 Aug 2022 02:04:17 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 03 Aug 2022 02:04:17 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 03 Aug 2022 02:04:17 GMT
EXPOSE 8091
# Wed, 03 Aug 2022 02:04:18 GMT
VOLUME [/var/lib/influxdb]
# Wed, 03 Aug 2022 02:04:18 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 03 Aug 2022 02:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Aug 2022 02:04:18 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452`  
		Last Modified: Tue, 02 Aug 2022 01:23:44 GMT  
		Size: 55.0 MB (54999331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 5.2 MB (5156256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a`  
		Last Modified: Tue, 02 Aug 2022 02:18:26 GMT  
		Size: 10.9 MB (10876485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caa2264e70c4ed390b55cf4207fecfed772b9576bfb2e5c75781b0ed41df3fc`  
		Last Modified: Wed, 03 Aug 2022 02:06:17 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200d1c964c659220d3808f865050cb12346d90f4ef8b119143f59fc6f5380bf`  
		Last Modified: Wed, 03 Aug 2022 02:07:00 GMT  
		Size: 23.4 MB (23412758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9431f49f5357a73efefcea8ce35acb4a54df1b73b66c5ae29001e1294b836ef7`  
		Last Modified: Wed, 03 Aug 2022 02:06:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155e3e30f68132af9a5c0902bc1c7e817b709acf97e82f34c92b563f500339fd`  
		Last Modified: Wed, 03 Aug 2022 02:06:57 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:1bc53a804fca50ef4f8ff62269b97fc2f999f3f1b4b2c286b9a1d1e6252f1841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b2295d4b7e378ebe952bd3db3eee150fc33b5c432bc6bd6ed03b233d07764186
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27610491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daffb717093e5bdc9c615118ce300a424b46c357b7e071101f2a78ceb3ccc024`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 20:35:04 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 20:35:16 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Tue, 09 Aug 2022 20:35:36 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 20:35:36 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 09 Aug 2022 20:35:37 GMT
EXPOSE 8091
# Tue, 09 Aug 2022 20:35:37 GMT
VOLUME [/var/lib/influxdb]
# Tue, 09 Aug 2022 20:35:37 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 09 Aug 2022 20:35:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 20:35:37 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d486be743febca6fc2475ff27102b9faad6318945d0696b0013a7a8a5331f9`  
		Last Modified: Tue, 09 Aug 2022 20:38:17 GMT  
		Size: 1.5 MB (1489248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85effd48049aab32e47b63df4632902515f5c87326ec4d45f173490d9040e308`  
		Last Modified: Tue, 09 Aug 2022 20:38:58 GMT  
		Size: 23.3 MB (23293005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83a163fb6c3d2277185ea1bd9a4aee51518e3d8b101a46364ffeb99db61367f`  
		Last Modified: Tue, 09 Aug 2022 20:38:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef0f697d368b5ad70ca2b594e9b44589e36b36e30957e81d64e7f960a99db90`  
		Last Modified: Tue, 09 Aug 2022 20:38:55 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
