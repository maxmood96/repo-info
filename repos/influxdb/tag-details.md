<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.7`](#influxdb17)
-	[`influxdb:1.7-alpine`](#influxdb17-alpine)
-	[`influxdb:1.7-data`](#influxdb17-data)
-	[`influxdb:1.7-data-alpine`](#influxdb17-data-alpine)
-	[`influxdb:1.7-meta`](#influxdb17-meta)
-	[`influxdb:1.7-meta-alpine`](#influxdb17-meta-alpine)
-	[`influxdb:1.7.11`](#influxdb1711)
-	[`influxdb:1.7.11-alpine`](#influxdb1711-alpine)
-	[`influxdb:1.7.11-data`](#influxdb1711-data)
-	[`influxdb:1.7.11-data-alpine`](#influxdb1711-data-alpine)
-	[`influxdb:1.7.11-meta`](#influxdb1711-meta)
-	[`influxdb:1.7.11-meta-alpine`](#influxdb1711-meta-alpine)
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
-	[`influxdb:1.9.6-data`](#influxdb196-data)
-	[`influxdb:1.9.6-data-alpine`](#influxdb196-data-alpine)
-	[`influxdb:1.9.6-meta`](#influxdb196-meta)
-	[`influxdb:1.9.6-meta-alpine`](#influxdb196-meta-alpine)
-	[`influxdb:2.0`](#influxdb20)
-	[`influxdb:2.0-alpine`](#influxdb20-alpine)
-	[`influxdb:2.0.9`](#influxdb209)
-	[`influxdb:2.0.9-alpine`](#influxdb209-alpine)
-	[`influxdb:2.1`](#influxdb21)
-	[`influxdb:2.1-alpine`](#influxdb21-alpine)
-	[`influxdb:2.1.1`](#influxdb211)
-	[`influxdb:2.1.1-alpine`](#influxdb211-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:data`](#influxdbdata)
-	[`influxdb:data-alpine`](#influxdbdata-alpine)
-	[`influxdb:latest`](#influxdblatest)
-	[`influxdb:meta`](#influxdbmeta)
-	[`influxdb:meta-alpine`](#influxdbmeta-alpine)

## `influxdb:1.7`

```console
$ docker pull influxdb@sha256:efe439fd06d0d99fd00bd2dc0637227d387ebcbfcc95f3e22ba81437a8f6abbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7` - linux; amd64

```console
$ docker pull influxdb@sha256:2eb372aaa8f3446e6876b8095d97f9a4e90711593995806f1158f4c988b9765e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122363065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9475026d4e23a49d6963de15ad39b79c0cd00ad3d836ad409e9670557078264`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:04:31 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 30 Mar 2022 23:04:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 30 Mar 2022 23:04:37 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:04:37 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:04:37 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:04:37 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:04:37 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:04:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:04:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755d2fad847f1bd785ce676d17a87c630ad32314a59e11b1e22afe4f479527a5`  
		Last Modified: Wed, 30 Mar 2022 23:07:25 GMT  
		Size: 61.3 MB (61285835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8886e2b914461cfdc5b9bd1d02320b38b9ab60b2f5fdd48026d40f0a99c06d53`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f93d29c3a730e3e4fb478aaf8dcdb21c5ffd4cb2a717bb781e5062a3379da05`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cf424748421919fcc72a47ed35f43dc76287a808756dabf4111ec1f2d65583`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:069bd61d81f0ef2d7f5af1f14b145c726fa7347cadf60edc112887502aecafcd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113504070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd92dd0f9b7d79a1eed394d7b7a63bf43c1748b61d8f4da162085f5e77e1f803`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:25 GMT
ADD file:e869f7223f16639eccabff7b2c6a85a7e6b075d0933c31f2fecae79c1c26d5be in / 
# Thu, 17 Mar 2022 09:36:26 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 03:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:03:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 20 Mar 2022 17:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 20 Mar 2022 17:38:38 GMT
ENV INFLUXDB_VERSION=1.7.11
# Sun, 20 Mar 2022 17:38:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 20 Mar 2022 17:38:52 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 20 Mar 2022 17:38:53 GMT
EXPOSE 8086
# Sun, 20 Mar 2022 17:38:53 GMT
VOLUME [/var/lib/influxdb]
# Sun, 20 Mar 2022 17:38:54 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 20 Mar 2022 17:38:54 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 20 Mar 2022 17:38:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 20 Mar 2022 17:38:55 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a9f775cd9058b832779f6c0dd1ca0fbb1417961dd87ca3ba6200f41aa283371b`  
		Last Modified: Thu, 17 Mar 2022 09:53:00 GMT  
		Size: 42.2 MB (42151366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5c76f62b4a80636807fcffcd72fa68808c0faab499371e9e49ea3805cb8de8`  
		Last Modified: Sat, 19 Mar 2022 03:37:42 GMT  
		Size: 10.0 MB (9956816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe67020a39019149bd81805e6b89528643f4464d33964fe8bd1c39ed3c68dfd`  
		Last Modified: Sat, 19 Mar 2022 03:37:39 GMT  
		Size: 3.9 MB (3921814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dabf083c89b4d5b61d293c482bbff189bed8dfdba4ced2a3eb85a1ee237b61`  
		Last Modified: Sun, 20 Mar 2022 17:39:53 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dfca2cf831bf60d2b97d2938ac859247efbb96bb2a960f1141037f26a4c68a`  
		Last Modified: Sun, 20 Mar 2022 17:40:24 GMT  
		Size: 57.5 MB (57469503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be9c740677876b1ab6a1ce25bd545099f0461b4452bca1d65321ee5e0012e01`  
		Last Modified: Sun, 20 Mar 2022 17:39:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09983857e81734debea688a64193486cbd25e3cc0c953263d6e4699ebd9c1365`  
		Last Modified: Sun, 20 Mar 2022 17:39:53 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a5baf65aefa3c81d0e3dc250c0e65f7223a9e5ad819dd3b3c0e40f5a8ca384`  
		Last Modified: Sun, 20 Mar 2022 17:39:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:85107388fbe2fc713c2ada722c157cfeef0d209e2f5cbbcdd68d57cbe72e891a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114514974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddef062c446b2a10bdb80bf17a3068c75902cf061aa4dd614d53245d624465b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:21 GMT
ADD file:cfa91852b5b893603b656848cb1329c06041fea5cfef841978456c7266e6ac11 in / 
# Tue, 29 Mar 2022 00:45:22 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:18:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:21:07 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 30 Mar 2022 23:21:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 30 Mar 2022 23:21:14 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:21:14 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:21:15 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:21:17 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:21:18 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:21:19 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0b62b1ed6f218f82ac797884bd7a8c5dcdcdd8d003f3946678c53900cc537d7b`  
		Last Modified: Tue, 29 Mar 2022 00:53:52 GMT  
		Size: 43.2 MB (43212837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e309f576f536ef1eb431f346fb1a09b23c355e6ec7657db9b1b5d59d58c839`  
		Last Modified: Wed, 30 Mar 2022 02:27:51 GMT  
		Size: 10.2 MB (10217976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91984a52400cf1b768b1f46910222bcf8cb584650c23a648535dab2f65b3ef9`  
		Last Modified: Wed, 30 Mar 2022 02:27:51 GMT  
		Size: 3.9 MB (3874485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5e9af97a9e4a8158f582fd42b5462fe38123e2b8259780646271ccb9b37805`  
		Last Modified: Wed, 30 Mar 2022 23:23:17 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c980000988ae72771634495a4fa6551410c563d708d83e93d449765f5b6eb0b7`  
		Last Modified: Wed, 30 Mar 2022 23:23:24 GMT  
		Size: 57.2 MB (57205134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3763ca7e643d35a728b6ada0809d6465bea1bcaee4541aa29714d40f6fd80646`  
		Last Modified: Wed, 30 Mar 2022 23:23:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca9f78e9b446a57afdecff407266e0ab59562435d72ac41ac5d153865a2a4ed`  
		Last Modified: Wed, 30 Mar 2022 23:23:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd0c32c1ec6e70375444ad836185bc1859454817699fea5d2b6fb497d44e0b1`  
		Last Modified: Wed, 30 Mar 2022 23:23:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-alpine`

```console
$ docker pull influxdb@sha256:ce7ad891a3a584ba67c497b0ffc3e6a709ebf6d9db3a660243ea342daac91e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b14de2daf5ffbabb74411ae6fbc697cc7b7187213f0b818c030dfcb854078b20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7189d62b8f0af5c09a7f96686271b84b7e545d6ea052305cdbc05f34ad73cbf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:21:05 GMT
ENV INFLUXDB_VERSION=1.7.11
# Tue, 29 Mar 2022 17:21:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:21:21 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 29 Mar 2022 17:21:21 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:21:21 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:21:21 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:21:21 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 29 Mar 2022 17:21:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:21:21 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e076925cf8808d222bc77ee63d0d288717d55567274b12ecf906f862554def4`  
		Last Modified: Tue, 29 Mar 2022 17:24:21 GMT  
		Size: 61.0 MB (61034479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511089bccd198323cec4a8da72bbe5d2aea986d1e25d07861beb847a3478bef6`  
		Last Modified: Tue, 29 Mar 2022 17:24:13 GMT  
		Size: 253.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4026681744665c287f290498d59d2d4e306ef6160df77bb26d470475e2935fc6`  
		Last Modified: Tue, 29 Mar 2022 17:24:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cb81bf323798a7d3a37146b81a967171c19ff4aff8fa0cff9988cb097d40dd`  
		Last Modified: Tue, 29 Mar 2022 17:24:13 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data`

```console
$ docker pull influxdb@sha256:438b3f35b8218f257a99204f4959a8df3b3c4ee2cc9be9a33bfc39b005c13911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:d3a21785141df03d045425bd57427164b4abee7cda09fcc88547764fea3a5442
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149026882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4af24788454acc1056690bd54ded600c1904db7abef2209508ff1a50e71724`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:04:43 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 30 Mar 2022 23:04:51 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:04:52 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:04:52 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:04:52 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:04:52 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:04:53 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:04:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:04:53 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94a0407f4d22fc717be0d030b6699a3a2755ef557b91ef0b2c8299e41561c22`  
		Last Modified: Wed, 30 Mar 2022 23:07:47 GMT  
		Size: 87.9 MB (87949596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36709090acd93ca0eac6f7a9b0355b1742291dfe7a1587a3f1faffd34b55b24f`  
		Last Modified: Wed, 30 Mar 2022 23:07:35 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8435c27c8ff8af9833bd07d7276e8ae3aeacba68329e63700be89da83be3a3`  
		Last Modified: Wed, 30 Mar 2022 23:07:35 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a409a44fad2d4d86131f7abdbf87ea3b081121228ce23857c54a63fc1a3a79ff`  
		Last Modified: Wed, 30 Mar 2022 23:07:35 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data-alpine`

```console
$ docker pull influxdb@sha256:90434c9573e8696b5bc81a1d730e577542abbd722879207e6eaee9464b3d2a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b752f49fb6b16df33a1e06a3faba95f72a02b98311123a32f127a64a0e8ddbbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91936464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569ded59ee467f75b04349cae1c0093d43f46022f05c317c409091fd33c68cd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:21:29 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Tue, 29 Mar 2022 17:21:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:21:41 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 29 Mar 2022 17:21:41 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:21:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:21:41 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:21:41 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 29 Mar 2022 17:21:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:21:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03735692d99f06b9a4fd996e8efd92951f31c13084615de309526374bac40f8e`  
		Last Modified: Tue, 29 Mar 2022 17:24:43 GMT  
		Size: 87.6 MB (87640797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71267ad952c6b61a23286c971097f78c65e810a5da936bb3ce473457f56d9e2`  
		Last Modified: Tue, 29 Mar 2022 17:24:32 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086e1aa48eba2e4d0695e4f97d3522640bcf1f3c01bc9bfba261c39ea780018d`  
		Last Modified: Tue, 29 Mar 2022 17:24:32 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b58e86566d540397649f45d155ae7171cac505b64c00bf1090f316e08747ffd`  
		Last Modified: Tue, 29 Mar 2022 17:24:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta`

```console
$ docker pull influxdb@sha256:47f2386dbe0e08a55da25961db7f1ae98c378eb81a26e63a76ca740e387a2aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:7609609326134cba5aa8b7ccc4d1cf572aba4f3535447340b04e65b300e00d60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84210349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377198068e457c2755e6b42151fc00d3962b2e1fe9b385585fa8a102be182999`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:04:43 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 30 Mar 2022 23:05:02 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:02 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 30 Mar 2022 23:05:02 GMT
EXPOSE 8091
# Wed, 30 Mar 2022 23:05:02 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:02 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:02 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cc7f27da30f807e370f331d5e7b560a416a6ab30e5e992b31942ae447f7c4b`  
		Last Modified: Wed, 30 Mar 2022 23:08:00 GMT  
		Size: 23.1 MB (23134265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b516f2a43fad083756ac867903690495f082fb0a82b39d89b1ae5cf5f1ee24`  
		Last Modified: Wed, 30 Mar 2022 23:07:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a015078f683fcee8eb32b7c3a751569f937a2b152f8fae78dcbd06be29433ed`  
		Last Modified: Wed, 30 Mar 2022 23:07:57 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta-alpine`

```console
$ docker pull influxdb@sha256:ec04d5bf4fb1b5f8d7fa987e0695d07bfb0d66b03c97c994c1f064883a052dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b8a2f16fbbb9cf82cfe7cc43d6858b62063120e39dfba9d2c8e999de8a0c3813
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27298010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c800d27de23a1117c816823727e79f4f54cabf632fa29833f26a0a84760ae48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:21:29 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Tue, 29 Mar 2022 17:21:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:21:52 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 29 Mar 2022 17:21:52 GMT
EXPOSE 8091
# Tue, 29 Mar 2022 17:21:52 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:21:52 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:21:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:21:52 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe06438f6ba5be331b742668af23082228e19a081b36b9df48564ce3cc04f40`  
		Last Modified: Tue, 29 Mar 2022 17:24:57 GMT  
		Size: 23.0 MB (23003547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a296536c3760a6bf110a0c4977d5bb1f393fb730b6b8882d2f9c6a2fd5c3b602`  
		Last Modified: Tue, 29 Mar 2022 17:24:54 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b86840ee882e7b42201f40c18c47da9f36aff17ad640437795c488006a9293`  
		Last Modified: Tue, 29 Mar 2022 17:24:54 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11`

```console
$ docker pull influxdb@sha256:efe439fd06d0d99fd00bd2dc0637227d387ebcbfcc95f3e22ba81437a8f6abbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7.11` - linux; amd64

```console
$ docker pull influxdb@sha256:2eb372aaa8f3446e6876b8095d97f9a4e90711593995806f1158f4c988b9765e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122363065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9475026d4e23a49d6963de15ad39b79c0cd00ad3d836ad409e9670557078264`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:04:31 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 30 Mar 2022 23:04:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 30 Mar 2022 23:04:37 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:04:37 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:04:37 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:04:37 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:04:37 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:04:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:04:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755d2fad847f1bd785ce676d17a87c630ad32314a59e11b1e22afe4f479527a5`  
		Last Modified: Wed, 30 Mar 2022 23:07:25 GMT  
		Size: 61.3 MB (61285835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8886e2b914461cfdc5b9bd1d02320b38b9ab60b2f5fdd48026d40f0a99c06d53`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f93d29c3a730e3e4fb478aaf8dcdb21c5ffd4cb2a717bb781e5062a3379da05`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cf424748421919fcc72a47ed35f43dc76287a808756dabf4111ec1f2d65583`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.11` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:069bd61d81f0ef2d7f5af1f14b145c726fa7347cadf60edc112887502aecafcd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113504070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd92dd0f9b7d79a1eed394d7b7a63bf43c1748b61d8f4da162085f5e77e1f803`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:25 GMT
ADD file:e869f7223f16639eccabff7b2c6a85a7e6b075d0933c31f2fecae79c1c26d5be in / 
# Thu, 17 Mar 2022 09:36:26 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 03:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:03:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 20 Mar 2022 17:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 20 Mar 2022 17:38:38 GMT
ENV INFLUXDB_VERSION=1.7.11
# Sun, 20 Mar 2022 17:38:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 20 Mar 2022 17:38:52 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 20 Mar 2022 17:38:53 GMT
EXPOSE 8086
# Sun, 20 Mar 2022 17:38:53 GMT
VOLUME [/var/lib/influxdb]
# Sun, 20 Mar 2022 17:38:54 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 20 Mar 2022 17:38:54 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 20 Mar 2022 17:38:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 20 Mar 2022 17:38:55 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a9f775cd9058b832779f6c0dd1ca0fbb1417961dd87ca3ba6200f41aa283371b`  
		Last Modified: Thu, 17 Mar 2022 09:53:00 GMT  
		Size: 42.2 MB (42151366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5c76f62b4a80636807fcffcd72fa68808c0faab499371e9e49ea3805cb8de8`  
		Last Modified: Sat, 19 Mar 2022 03:37:42 GMT  
		Size: 10.0 MB (9956816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe67020a39019149bd81805e6b89528643f4464d33964fe8bd1c39ed3c68dfd`  
		Last Modified: Sat, 19 Mar 2022 03:37:39 GMT  
		Size: 3.9 MB (3921814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dabf083c89b4d5b61d293c482bbff189bed8dfdba4ced2a3eb85a1ee237b61`  
		Last Modified: Sun, 20 Mar 2022 17:39:53 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dfca2cf831bf60d2b97d2938ac859247efbb96bb2a960f1141037f26a4c68a`  
		Last Modified: Sun, 20 Mar 2022 17:40:24 GMT  
		Size: 57.5 MB (57469503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be9c740677876b1ab6a1ce25bd545099f0461b4452bca1d65321ee5e0012e01`  
		Last Modified: Sun, 20 Mar 2022 17:39:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09983857e81734debea688a64193486cbd25e3cc0c953263d6e4699ebd9c1365`  
		Last Modified: Sun, 20 Mar 2022 17:39:53 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a5baf65aefa3c81d0e3dc250c0e65f7223a9e5ad819dd3b3c0e40f5a8ca384`  
		Last Modified: Sun, 20 Mar 2022 17:39:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:85107388fbe2fc713c2ada722c157cfeef0d209e2f5cbbcdd68d57cbe72e891a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114514974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddef062c446b2a10bdb80bf17a3068c75902cf061aa4dd614d53245d624465b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:21 GMT
ADD file:cfa91852b5b893603b656848cb1329c06041fea5cfef841978456c7266e6ac11 in / 
# Tue, 29 Mar 2022 00:45:22 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:18:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:21:07 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 30 Mar 2022 23:21:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 30 Mar 2022 23:21:14 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:21:14 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:21:15 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:21:17 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:21:18 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:21:19 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0b62b1ed6f218f82ac797884bd7a8c5dcdcdd8d003f3946678c53900cc537d7b`  
		Last Modified: Tue, 29 Mar 2022 00:53:52 GMT  
		Size: 43.2 MB (43212837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e309f576f536ef1eb431f346fb1a09b23c355e6ec7657db9b1b5d59d58c839`  
		Last Modified: Wed, 30 Mar 2022 02:27:51 GMT  
		Size: 10.2 MB (10217976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91984a52400cf1b768b1f46910222bcf8cb584650c23a648535dab2f65b3ef9`  
		Last Modified: Wed, 30 Mar 2022 02:27:51 GMT  
		Size: 3.9 MB (3874485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5e9af97a9e4a8158f582fd42b5462fe38123e2b8259780646271ccb9b37805`  
		Last Modified: Wed, 30 Mar 2022 23:23:17 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c980000988ae72771634495a4fa6551410c563d708d83e93d449765f5b6eb0b7`  
		Last Modified: Wed, 30 Mar 2022 23:23:24 GMT  
		Size: 57.2 MB (57205134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3763ca7e643d35a728b6ada0809d6465bea1bcaee4541aa29714d40f6fd80646`  
		Last Modified: Wed, 30 Mar 2022 23:23:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca9f78e9b446a57afdecff407266e0ab59562435d72ac41ac5d153865a2a4ed`  
		Last Modified: Wed, 30 Mar 2022 23:23:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd0c32c1ec6e70375444ad836185bc1859454817699fea5d2b6fb497d44e0b1`  
		Last Modified: Wed, 30 Mar 2022 23:23:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-alpine`

```console
$ docker pull influxdb@sha256:ce7ad891a3a584ba67c497b0ffc3e6a709ebf6d9db3a660243ea342daac91e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.7.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b14de2daf5ffbabb74411ae6fbc697cc7b7187213f0b818c030dfcb854078b20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7189d62b8f0af5c09a7f96686271b84b7e545d6ea052305cdbc05f34ad73cbf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:21:05 GMT
ENV INFLUXDB_VERSION=1.7.11
# Tue, 29 Mar 2022 17:21:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:21:21 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 29 Mar 2022 17:21:21 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:21:21 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:21:21 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:21:21 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 29 Mar 2022 17:21:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:21:21 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e076925cf8808d222bc77ee63d0d288717d55567274b12ecf906f862554def4`  
		Last Modified: Tue, 29 Mar 2022 17:24:21 GMT  
		Size: 61.0 MB (61034479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511089bccd198323cec4a8da72bbe5d2aea986d1e25d07861beb847a3478bef6`  
		Last Modified: Tue, 29 Mar 2022 17:24:13 GMT  
		Size: 253.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4026681744665c287f290498d59d2d4e306ef6160df77bb26d470475e2935fc6`  
		Last Modified: Tue, 29 Mar 2022 17:24:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cb81bf323798a7d3a37146b81a967171c19ff4aff8fa0cff9988cb097d40dd`  
		Last Modified: Tue, 29 Mar 2022 17:24:13 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-data`

```console
$ docker pull influxdb@sha256:438b3f35b8218f257a99204f4959a8df3b3c4ee2cc9be9a33bfc39b005c13911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.7.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:d3a21785141df03d045425bd57427164b4abee7cda09fcc88547764fea3a5442
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149026882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4af24788454acc1056690bd54ded600c1904db7abef2209508ff1a50e71724`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:04:43 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 30 Mar 2022 23:04:51 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:04:52 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:04:52 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:04:52 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:04:52 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:04:53 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:04:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:04:53 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94a0407f4d22fc717be0d030b6699a3a2755ef557b91ef0b2c8299e41561c22`  
		Last Modified: Wed, 30 Mar 2022 23:07:47 GMT  
		Size: 87.9 MB (87949596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36709090acd93ca0eac6f7a9b0355b1742291dfe7a1587a3f1faffd34b55b24f`  
		Last Modified: Wed, 30 Mar 2022 23:07:35 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8435c27c8ff8af9833bd07d7276e8ae3aeacba68329e63700be89da83be3a3`  
		Last Modified: Wed, 30 Mar 2022 23:07:35 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a409a44fad2d4d86131f7abdbf87ea3b081121228ce23857c54a63fc1a3a79ff`  
		Last Modified: Wed, 30 Mar 2022 23:07:35 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-data-alpine`

```console
$ docker pull influxdb@sha256:90434c9573e8696b5bc81a1d730e577542abbd722879207e6eaee9464b3d2a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.7.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b752f49fb6b16df33a1e06a3faba95f72a02b98311123a32f127a64a0e8ddbbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91936464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569ded59ee467f75b04349cae1c0093d43f46022f05c317c409091fd33c68cd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:21:29 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Tue, 29 Mar 2022 17:21:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:21:41 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 29 Mar 2022 17:21:41 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:21:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:21:41 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:21:41 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 29 Mar 2022 17:21:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:21:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03735692d99f06b9a4fd996e8efd92951f31c13084615de309526374bac40f8e`  
		Last Modified: Tue, 29 Mar 2022 17:24:43 GMT  
		Size: 87.6 MB (87640797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71267ad952c6b61a23286c971097f78c65e810a5da936bb3ce473457f56d9e2`  
		Last Modified: Tue, 29 Mar 2022 17:24:32 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086e1aa48eba2e4d0695e4f97d3522640bcf1f3c01bc9bfba261c39ea780018d`  
		Last Modified: Tue, 29 Mar 2022 17:24:32 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b58e86566d540397649f45d155ae7171cac505b64c00bf1090f316e08747ffd`  
		Last Modified: Tue, 29 Mar 2022 17:24:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-meta`

```console
$ docker pull influxdb@sha256:47f2386dbe0e08a55da25961db7f1ae98c378eb81a26e63a76ca740e387a2aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.7.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:7609609326134cba5aa8b7ccc4d1cf572aba4f3535447340b04e65b300e00d60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84210349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377198068e457c2755e6b42151fc00d3962b2e1fe9b385585fa8a102be182999`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:04:43 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 30 Mar 2022 23:05:02 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:02 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 30 Mar 2022 23:05:02 GMT
EXPOSE 8091
# Wed, 30 Mar 2022 23:05:02 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:02 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:02 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cc7f27da30f807e370f331d5e7b560a416a6ab30e5e992b31942ae447f7c4b`  
		Last Modified: Wed, 30 Mar 2022 23:08:00 GMT  
		Size: 23.1 MB (23134265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b516f2a43fad083756ac867903690495f082fb0a82b39d89b1ae5cf5f1ee24`  
		Last Modified: Wed, 30 Mar 2022 23:07:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a015078f683fcee8eb32b7c3a751569f937a2b152f8fae78dcbd06be29433ed`  
		Last Modified: Wed, 30 Mar 2022 23:07:57 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-meta-alpine`

```console
$ docker pull influxdb@sha256:ec04d5bf4fb1b5f8d7fa987e0695d07bfb0d66b03c97c994c1f064883a052dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.7.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b8a2f16fbbb9cf82cfe7cc43d6858b62063120e39dfba9d2c8e999de8a0c3813
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27298010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c800d27de23a1117c816823727e79f4f54cabf632fa29833f26a0a84760ae48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:21:29 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Tue, 29 Mar 2022 17:21:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:21:52 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 29 Mar 2022 17:21:52 GMT
EXPOSE 8091
# Tue, 29 Mar 2022 17:21:52 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:21:52 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:21:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:21:52 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe06438f6ba5be331b742668af23082228e19a081b36b9df48564ce3cc04f40`  
		Last Modified: Tue, 29 Mar 2022 17:24:57 GMT  
		Size: 23.0 MB (23003547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a296536c3760a6bf110a0c4977d5bb1f393fb730b6b8882d2f9c6a2fd5c3b602`  
		Last Modified: Tue, 29 Mar 2022 17:24:54 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b86840ee882e7b42201f40c18c47da9f36aff17ad640437795c488006a9293`  
		Last Modified: Tue, 29 Mar 2022 17:24:54 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:fd8c9d4f91672a02a9ffee83e4b200f2988ba0f2cacb008139a62f882778bc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:4dc8aa1263b63b14b4e2fa4e692e7127ce0a9e43924405b4bdbbc311bb4118ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115967376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9eb7b5252d2a347b3993df10fe3a458bf0a0398d002eb3bf63e0273fbfddc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:07 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 30 Mar 2022 23:05:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 30 Mar 2022 23:05:13 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:13 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:13 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:13 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:13 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:13 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca272d9f078b66187b887ca31b8ca4afa85dfdd1750b13ef1b5bf599499c5d9`  
		Last Modified: Wed, 30 Mar 2022 23:08:18 GMT  
		Size: 54.9 MB (54890147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2740ef6abdea6a96813cfb0092535131c034ff3d6cbb1092ebe16a3b155f2672`  
		Last Modified: Wed, 30 Mar 2022 23:08:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a5ae9b77009c830ef5631cb3b5794ff6322d5c6b7fca8a470efcd5fad250f9`  
		Last Modified: Wed, 30 Mar 2022 23:08:11 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc28277163b44cf773f9c177ede9f406f7798b6ff10fcceb4cbdd00613c213a`  
		Last Modified: Wed, 30 Mar 2022 23:08:11 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:42c2d969737adabfa9e9cef4dd217270f9cfb97f29d41361066a15762b182faa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107651964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01be217e9dea728fb4bcfad6a8fe368c299761168a4555da6397b4e11d024eeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:25 GMT
ADD file:e869f7223f16639eccabff7b2c6a85a7e6b075d0933c31f2fecae79c1c26d5be in / 
# Thu, 17 Mar 2022 09:36:26 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 03:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:03:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 20 Mar 2022 17:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 20 Mar 2022 17:39:07 GMT
ENV INFLUXDB_VERSION=1.8.10
# Sun, 20 Mar 2022 17:39:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 20 Mar 2022 17:39:20 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 20 Mar 2022 17:39:21 GMT
EXPOSE 8086
# Sun, 20 Mar 2022 17:39:21 GMT
VOLUME [/var/lib/influxdb]
# Sun, 20 Mar 2022 17:39:22 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 20 Mar 2022 17:39:22 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 20 Mar 2022 17:39:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 20 Mar 2022 17:39:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a9f775cd9058b832779f6c0dd1ca0fbb1417961dd87ca3ba6200f41aa283371b`  
		Last Modified: Thu, 17 Mar 2022 09:53:00 GMT  
		Size: 42.2 MB (42151366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5c76f62b4a80636807fcffcd72fa68808c0faab499371e9e49ea3805cb8de8`  
		Last Modified: Sat, 19 Mar 2022 03:37:42 GMT  
		Size: 10.0 MB (9956816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe67020a39019149bd81805e6b89528643f4464d33964fe8bd1c39ed3c68dfd`  
		Last Modified: Sat, 19 Mar 2022 03:37:39 GMT  
		Size: 3.9 MB (3921814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dabf083c89b4d5b61d293c482bbff189bed8dfdba4ced2a3eb85a1ee237b61`  
		Last Modified: Sun, 20 Mar 2022 17:39:53 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf56b940c1e9e2377291092f96b90d3d6baebf7a7a5b5e3c9aa61027f44957aa`  
		Last Modified: Sun, 20 Mar 2022 17:41:03 GMT  
		Size: 51.6 MB (51617401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b229066ab98468dc3100a4ad4992dc41f3a2b21e8e51b3de41f319491ad92de`  
		Last Modified: Sun, 20 Mar 2022 17:40:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41298bb0edb20b21c1a3ed42b80bed690cf420b93a9a3fc42b7f8fc1a8ee77fa`  
		Last Modified: Sun, 20 Mar 2022 17:40:36 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71729132b21a6611ce18e480b3ac7544e35ede9d70ca8bca70d358d88dbed17`  
		Last Modified: Sun, 20 Mar 2022 17:40:36 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:578963c45259268acb301239a3a3679806fad07c65dd91d8e2d164e9287977aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108544173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbc97103507192438f04f90864fd11c5e3ce05489afa1499826c40c1610b7c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:21 GMT
ADD file:cfa91852b5b893603b656848cb1329c06041fea5cfef841978456c7266e6ac11 in / 
# Tue, 29 Mar 2022 00:45:22 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:18:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:21:25 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 30 Mar 2022 23:21:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 30 Mar 2022 23:21:32 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:21:32 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:21:33 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:21:35 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:21:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:21:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:21:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0b62b1ed6f218f82ac797884bd7a8c5dcdcdd8d003f3946678c53900cc537d7b`  
		Last Modified: Tue, 29 Mar 2022 00:53:52 GMT  
		Size: 43.2 MB (43212837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e309f576f536ef1eb431f346fb1a09b23c355e6ec7657db9b1b5d59d58c839`  
		Last Modified: Wed, 30 Mar 2022 02:27:51 GMT  
		Size: 10.2 MB (10217976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91984a52400cf1b768b1f46910222bcf8cb584650c23a648535dab2f65b3ef9`  
		Last Modified: Wed, 30 Mar 2022 02:27:51 GMT  
		Size: 3.9 MB (3874485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5e9af97a9e4a8158f582fd42b5462fe38123e2b8259780646271ccb9b37805`  
		Last Modified: Wed, 30 Mar 2022 23:23:17 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40959cbe31a72fcd483ea95f1fe359da1f38d3bf7dddfed89189c6db7fd725dc`  
		Last Modified: Wed, 30 Mar 2022 23:23:42 GMT  
		Size: 51.2 MB (51234333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc9046408609c0e444fb18f8431d85bb7e297e3a30a1641ac91c1d82f74e105`  
		Last Modified: Wed, 30 Mar 2022 23:23:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62b2947a2cb7cb742e6a5ff31431072f7ce1f1710ca12e4e51615c604cf797c`  
		Last Modified: Wed, 30 Mar 2022 23:23:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6d029ae6b6f2c7d9ebbe7df6c12f7870c915a71096fb42671d734cc03fe061`  
		Last Modified: Wed, 30 Mar 2022 23:23:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:3a7ee21e418ea85c0125b0c9fc771ea9fe629f4b17a73a67042b5345f6677416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9d51efa7b2591519f27f29f588a4c6f59c1fbd327512c4754d2a02a3451665fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58955168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d4ef3f8ac8b36a2639580f500cbb2e6321f068596518e75789ab6dc4b6b300`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:21:57 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 29 Mar 2022 17:22:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:22:03 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 29 Mar 2022 17:22:03 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:22:03 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:22:03 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:22:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 29 Mar 2022 17:22:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:22:04 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df3676fea4f0fe6d154ad252e13d58dfa1883fdacf1c982d3d284d229ea424`  
		Last Modified: Tue, 29 Mar 2022 17:25:15 GMT  
		Size: 54.7 MB (54659557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34dda1acf2654b26c6dc4ac5b6e7fd1a6346be37a778833c969dbf51893cd9a8`  
		Last Modified: Tue, 29 Mar 2022 17:25:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e08c95eb86b32bb2159bcee213ca44758e0664cf303658aa2b743b5f49a4eb8`  
		Last Modified: Tue, 29 Mar 2022 17:25:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50b7ac0c8cdef10c0181240f921654e6352a4b67b713b81a7de3260cd2f462f`  
		Last Modified: Tue, 29 Mar 2022 17:25:08 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data`

```console
$ docker pull influxdb@sha256:be2d5a7bd5ff0644383defcce1f7769ae89363d5867ac5b2615ae2731dcb6c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:0790872efd83e02d8fdd2faf7a2ff410f9ff50a007b58c517d14c783d48130d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117786452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276cebfb7edd0645264657425ddb00bb2bcb80b7dce64169b9281067ebc0707c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:18 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 30 Mar 2022 23:05:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:25 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:25 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edcfcb7a5161abd03b61b6153c6f903029bcfb2d9efa4a6556918c51a064af1`  
		Last Modified: Wed, 30 Mar 2022 23:08:36 GMT  
		Size: 56.7 MB (56709163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97289aef350957936b3a19d68c846a790247f957e99f5d9f0e9c628bc74e2d0f`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1caefc2f0645fadbdce8da95cfbe3bdf21d1712e3d4b95577a26a55d97debc`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fc4496b0657c51da18c2c520e35381f811fe8d8a7eb3c3f4b15209a3b00900`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data-alpine`

```console
$ docker pull influxdb@sha256:c3940c85422166cb6f158b97538004d73d21ce81f43a839fdab8c39b310c792a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:962baad1407568923fe45b600affa45466137ff4ef33a9d78299b95414d2f038
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60799373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3eee20845f355d9c17fa9824fadcfcb89bd4ba85d232ee3e46e100a3ec0af8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:08 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Tue, 29 Mar 2022 17:22:16 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:22:17 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 29 Mar 2022 17:22:17 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:22:17 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:22:17 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:22:17 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 29 Mar 2022 17:22:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:22:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07f289a640480e497bcb4cbf35f9903f519c0a4eca2e05512508a7725996c4d`  
		Last Modified: Tue, 29 Mar 2022 17:25:34 GMT  
		Size: 56.5 MB (56503709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ad694584956eac20bc9efecae61954abfa8ca0cf15116b2e5267f770f92e48`  
		Last Modified: Tue, 29 Mar 2022 17:25:27 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b163e6403d18c50a34a61fa4c5cbc219a7e6d50b23be842f8602b82f4ff642d9`  
		Last Modified: Tue, 29 Mar 2022 17:25:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b6760863cdb198fa9847fb23452a52a071d03107434a688207f9aab4c1a3c3`  
		Last Modified: Tue, 29 Mar 2022 17:25:27 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta`

```console
$ docker pull influxdb@sha256:4727e7c393e16502a487921e0fcae07eaaf9e00ecf3b22b37562e86d6867188b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c50786838735ef2c78c51e7238a4404520063b935751ce517157749b2904aa5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84493011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0e1d0ea12729ab4474843f41d7a88f5a1870ec065e3fe58185c6b0098c0ce1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:18 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 30 Mar 2022 23:05:32 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:32 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 30 Mar 2022 23:05:32 GMT
EXPOSE 8091
# Wed, 30 Mar 2022 23:05:32 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:33 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:33 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c487c418525e877d8128d62ac4dc164cba44ce112d1bc88171390368ce61ad53`  
		Last Modified: Wed, 30 Mar 2022 23:08:52 GMT  
		Size: 23.4 MB (23416930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720a75a54e3c5d1a6d4ca4261fc76d135e3e9c04b6804de3b56615706c8fdf17`  
		Last Modified: Wed, 30 Mar 2022 23:08:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feee196124cbe471a1e4ff40944ed9de1949b39f539001874ba0f125d28314d5`  
		Last Modified: Wed, 30 Mar 2022 23:08:49 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta-alpine`

```console
$ docker pull influxdb@sha256:2b31a82b424e3f0f93bc6b6d76569c55284d1d54a240d1495e5941f6fabc3a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:de1490581ec83ecc04551ed923bd4c9a9da5f2faa88c84ece23d8d5578b91407
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27587442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e859d256d7ddf403eb8cb6b19028bf170c200a756ce865dbf96421e5b5cbbe10`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:08 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Tue, 29 Mar 2022 17:22:27 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:22:27 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 29 Mar 2022 17:22:27 GMT
EXPOSE 8091
# Tue, 29 Mar 2022 17:22:27 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:22:27 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:22:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:22:27 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1724c466e7e91d37ac61a8791b771bb11953b76ba241a1b93fd755ca213ec3`  
		Last Modified: Tue, 29 Mar 2022 17:25:53 GMT  
		Size: 23.3 MB (23292976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1289b71d892126db0c08ceb7478ffcea1aafc961900dadb1570cf7935b356b1`  
		Last Modified: Tue, 29 Mar 2022 17:25:48 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edf276a80534e8819ddd932f9b6f428da7a8ab0cd040b1919e940975ede5688`  
		Last Modified: Tue, 29 Mar 2022 17:25:48 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10`

```console
$ docker pull influxdb@sha256:fd8c9d4f91672a02a9ffee83e4b200f2988ba0f2cacb008139a62f882778bc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.10` - linux; amd64

```console
$ docker pull influxdb@sha256:4dc8aa1263b63b14b4e2fa4e692e7127ce0a9e43924405b4bdbbc311bb4118ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115967376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9eb7b5252d2a347b3993df10fe3a458bf0a0398d002eb3bf63e0273fbfddc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:07 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 30 Mar 2022 23:05:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 30 Mar 2022 23:05:13 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:13 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:13 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:13 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:13 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:13 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca272d9f078b66187b887ca31b8ca4afa85dfdd1750b13ef1b5bf599499c5d9`  
		Last Modified: Wed, 30 Mar 2022 23:08:18 GMT  
		Size: 54.9 MB (54890147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2740ef6abdea6a96813cfb0092535131c034ff3d6cbb1092ebe16a3b155f2672`  
		Last Modified: Wed, 30 Mar 2022 23:08:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a5ae9b77009c830ef5631cb3b5794ff6322d5c6b7fca8a470efcd5fad250f9`  
		Last Modified: Wed, 30 Mar 2022 23:08:11 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc28277163b44cf773f9c177ede9f406f7798b6ff10fcceb4cbdd00613c213a`  
		Last Modified: Wed, 30 Mar 2022 23:08:11 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:42c2d969737adabfa9e9cef4dd217270f9cfb97f29d41361066a15762b182faa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107651964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01be217e9dea728fb4bcfad6a8fe368c299761168a4555da6397b4e11d024eeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:25 GMT
ADD file:e869f7223f16639eccabff7b2c6a85a7e6b075d0933c31f2fecae79c1c26d5be in / 
# Thu, 17 Mar 2022 09:36:26 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 03:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:03:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 20 Mar 2022 17:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 20 Mar 2022 17:39:07 GMT
ENV INFLUXDB_VERSION=1.8.10
# Sun, 20 Mar 2022 17:39:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 20 Mar 2022 17:39:20 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 20 Mar 2022 17:39:21 GMT
EXPOSE 8086
# Sun, 20 Mar 2022 17:39:21 GMT
VOLUME [/var/lib/influxdb]
# Sun, 20 Mar 2022 17:39:22 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 20 Mar 2022 17:39:22 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 20 Mar 2022 17:39:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 20 Mar 2022 17:39:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a9f775cd9058b832779f6c0dd1ca0fbb1417961dd87ca3ba6200f41aa283371b`  
		Last Modified: Thu, 17 Mar 2022 09:53:00 GMT  
		Size: 42.2 MB (42151366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5c76f62b4a80636807fcffcd72fa68808c0faab499371e9e49ea3805cb8de8`  
		Last Modified: Sat, 19 Mar 2022 03:37:42 GMT  
		Size: 10.0 MB (9956816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe67020a39019149bd81805e6b89528643f4464d33964fe8bd1c39ed3c68dfd`  
		Last Modified: Sat, 19 Mar 2022 03:37:39 GMT  
		Size: 3.9 MB (3921814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dabf083c89b4d5b61d293c482bbff189bed8dfdba4ced2a3eb85a1ee237b61`  
		Last Modified: Sun, 20 Mar 2022 17:39:53 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf56b940c1e9e2377291092f96b90d3d6baebf7a7a5b5e3c9aa61027f44957aa`  
		Last Modified: Sun, 20 Mar 2022 17:41:03 GMT  
		Size: 51.6 MB (51617401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b229066ab98468dc3100a4ad4992dc41f3a2b21e8e51b3de41f319491ad92de`  
		Last Modified: Sun, 20 Mar 2022 17:40:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41298bb0edb20b21c1a3ed42b80bed690cf420b93a9a3fc42b7f8fc1a8ee77fa`  
		Last Modified: Sun, 20 Mar 2022 17:40:36 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71729132b21a6611ce18e480b3ac7544e35ede9d70ca8bca70d358d88dbed17`  
		Last Modified: Sun, 20 Mar 2022 17:40:36 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:578963c45259268acb301239a3a3679806fad07c65dd91d8e2d164e9287977aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108544173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbc97103507192438f04f90864fd11c5e3ce05489afa1499826c40c1610b7c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:21 GMT
ADD file:cfa91852b5b893603b656848cb1329c06041fea5cfef841978456c7266e6ac11 in / 
# Tue, 29 Mar 2022 00:45:22 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:18:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:21:25 GMT
ENV INFLUXDB_VERSION=1.8.10
# Wed, 30 Mar 2022 23:21:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 30 Mar 2022 23:21:32 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:21:32 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:21:33 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:21:35 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:21:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:21:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:21:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0b62b1ed6f218f82ac797884bd7a8c5dcdcdd8d003f3946678c53900cc537d7b`  
		Last Modified: Tue, 29 Mar 2022 00:53:52 GMT  
		Size: 43.2 MB (43212837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e309f576f536ef1eb431f346fb1a09b23c355e6ec7657db9b1b5d59d58c839`  
		Last Modified: Wed, 30 Mar 2022 02:27:51 GMT  
		Size: 10.2 MB (10217976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91984a52400cf1b768b1f46910222bcf8cb584650c23a648535dab2f65b3ef9`  
		Last Modified: Wed, 30 Mar 2022 02:27:51 GMT  
		Size: 3.9 MB (3874485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5e9af97a9e4a8158f582fd42b5462fe38123e2b8259780646271ccb9b37805`  
		Last Modified: Wed, 30 Mar 2022 23:23:17 GMT  
		Size: 2.8 KB (2824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40959cbe31a72fcd483ea95f1fe359da1f38d3bf7dddfed89189c6db7fd725dc`  
		Last Modified: Wed, 30 Mar 2022 23:23:42 GMT  
		Size: 51.2 MB (51234333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc9046408609c0e444fb18f8431d85bb7e297e3a30a1641ac91c1d82f74e105`  
		Last Modified: Wed, 30 Mar 2022 23:23:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62b2947a2cb7cb742e6a5ff31431072f7ce1f1710ca12e4e51615c604cf797c`  
		Last Modified: Wed, 30 Mar 2022 23:23:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6d029ae6b6f2c7d9ebbe7df6c12f7870c915a71096fb42671d734cc03fe061`  
		Last Modified: Wed, 30 Mar 2022 23:23:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-alpine`

```console
$ docker pull influxdb@sha256:3a7ee21e418ea85c0125b0c9fc771ea9fe629f4b17a73a67042b5345f6677416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9d51efa7b2591519f27f29f588a4c6f59c1fbd327512c4754d2a02a3451665fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58955168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d4ef3f8ac8b36a2639580f500cbb2e6321f068596518e75789ab6dc4b6b300`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:21:57 GMT
ENV INFLUXDB_VERSION=1.8.10
# Tue, 29 Mar 2022 17:22:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:22:03 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 29 Mar 2022 17:22:03 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:22:03 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:22:03 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:22:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 29 Mar 2022 17:22:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:22:04 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df3676fea4f0fe6d154ad252e13d58dfa1883fdacf1c982d3d284d229ea424`  
		Last Modified: Tue, 29 Mar 2022 17:25:15 GMT  
		Size: 54.7 MB (54659557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34dda1acf2654b26c6dc4ac5b6e7fd1a6346be37a778833c969dbf51893cd9a8`  
		Last Modified: Tue, 29 Mar 2022 17:25:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e08c95eb86b32bb2159bcee213ca44758e0664cf303658aa2b743b5f49a4eb8`  
		Last Modified: Tue, 29 Mar 2022 17:25:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50b7ac0c8cdef10c0181240f921654e6352a4b67b713b81a7de3260cd2f462f`  
		Last Modified: Tue, 29 Mar 2022 17:25:08 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-data`

```console
$ docker pull influxdb@sha256:be2d5a7bd5ff0644383defcce1f7769ae89363d5867ac5b2615ae2731dcb6c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:0790872efd83e02d8fdd2faf7a2ff410f9ff50a007b58c517d14c783d48130d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117786452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276cebfb7edd0645264657425ddb00bb2bcb80b7dce64169b9281067ebc0707c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:18 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 30 Mar 2022 23:05:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:25 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:25 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edcfcb7a5161abd03b61b6153c6f903029bcfb2d9efa4a6556918c51a064af1`  
		Last Modified: Wed, 30 Mar 2022 23:08:36 GMT  
		Size: 56.7 MB (56709163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97289aef350957936b3a19d68c846a790247f957e99f5d9f0e9c628bc74e2d0f`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1caefc2f0645fadbdce8da95cfbe3bdf21d1712e3d4b95577a26a55d97debc`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fc4496b0657c51da18c2c520e35381f811fe8d8a7eb3c3f4b15209a3b00900`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-data-alpine`

```console
$ docker pull influxdb@sha256:c3940c85422166cb6f158b97538004d73d21ce81f43a839fdab8c39b310c792a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:962baad1407568923fe45b600affa45466137ff4ef33a9d78299b95414d2f038
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60799373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3eee20845f355d9c17fa9824fadcfcb89bd4ba85d232ee3e46e100a3ec0af8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:08 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Tue, 29 Mar 2022 17:22:16 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:22:17 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 29 Mar 2022 17:22:17 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:22:17 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:22:17 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:22:17 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 29 Mar 2022 17:22:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:22:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07f289a640480e497bcb4cbf35f9903f519c0a4eca2e05512508a7725996c4d`  
		Last Modified: Tue, 29 Mar 2022 17:25:34 GMT  
		Size: 56.5 MB (56503709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ad694584956eac20bc9efecae61954abfa8ca0cf15116b2e5267f770f92e48`  
		Last Modified: Tue, 29 Mar 2022 17:25:27 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b163e6403d18c50a34a61fa4c5cbc219a7e6d50b23be842f8602b82f4ff642d9`  
		Last Modified: Tue, 29 Mar 2022 17:25:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b6760863cdb198fa9847fb23452a52a071d03107434a688207f9aab4c1a3c3`  
		Last Modified: Tue, 29 Mar 2022 17:25:27 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-meta`

```console
$ docker pull influxdb@sha256:4727e7c393e16502a487921e0fcae07eaaf9e00ecf3b22b37562e86d6867188b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c50786838735ef2c78c51e7238a4404520063b935751ce517157749b2904aa5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84493011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0e1d0ea12729ab4474843f41d7a88f5a1870ec065e3fe58185c6b0098c0ce1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:18 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 30 Mar 2022 23:05:32 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:32 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 30 Mar 2022 23:05:32 GMT
EXPOSE 8091
# Wed, 30 Mar 2022 23:05:32 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:33 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:33 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c487c418525e877d8128d62ac4dc164cba44ce112d1bc88171390368ce61ad53`  
		Last Modified: Wed, 30 Mar 2022 23:08:52 GMT  
		Size: 23.4 MB (23416930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720a75a54e3c5d1a6d4ca4261fc76d135e3e9c04b6804de3b56615706c8fdf17`  
		Last Modified: Wed, 30 Mar 2022 23:08:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feee196124cbe471a1e4ff40944ed9de1949b39f539001874ba0f125d28314d5`  
		Last Modified: Wed, 30 Mar 2022 23:08:49 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.10-meta-alpine`

```console
$ docker pull influxdb@sha256:2b31a82b424e3f0f93bc6b6d76569c55284d1d54a240d1495e5941f6fabc3a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.8.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:de1490581ec83ecc04551ed923bd4c9a9da5f2faa88c84ece23d8d5578b91407
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27587442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e859d256d7ddf403eb8cb6b19028bf170c200a756ce865dbf96421e5b5cbbe10`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:08 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Tue, 29 Mar 2022 17:22:27 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:22:27 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 29 Mar 2022 17:22:27 GMT
EXPOSE 8091
# Tue, 29 Mar 2022 17:22:27 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:22:27 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:22:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:22:27 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1724c466e7e91d37ac61a8791b771bb11953b76ba241a1b93fd755ca213ec3`  
		Last Modified: Tue, 29 Mar 2022 17:25:53 GMT  
		Size: 23.3 MB (23292976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1289b71d892126db0c08ceb7478ffcea1aafc961900dadb1570cf7935b356b1`  
		Last Modified: Tue, 29 Mar 2022 17:25:48 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edf276a80534e8819ddd932f9b6f428da7a8ab0cd040b1919e940975ede5688`  
		Last Modified: Tue, 29 Mar 2022 17:25:48 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-data`

```console
$ docker pull influxdb@sha256:56b57de30ed18a3c48edf6b410685fe67808c5c1d892581146a69bd0dc145169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:6db64a003dd0be8e2fa3da8a8e79dcac9bc9c9f58213a6573085eca106b815c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88681465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0baf120185e11fa5d2e9cdcc89c96e5e56c90fb0724a96d3520b24b970e091`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:37 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Wed, 30 Mar 2022 23:05:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:41 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:41 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:42 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:42 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:42 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:42 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8f4a3d69c0c22b0e3d9e7e16969bf31ec608f5e24ef4978686b771811323e8`  
		Last Modified: Wed, 30 Mar 2022 23:09:10 GMT  
		Size: 27.6 MB (27604178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782474e6ac637e1f5dda88d1471243b88c53b7a3e7da56d72c38c0b9033c0a8`  
		Last Modified: Wed, 30 Mar 2022 23:09:06 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204739d56240853dfc71df7d11f0c188c2274e7fac0c4751483c66ef50b3733c`  
		Last Modified: Wed, 30 Mar 2022 23:09:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692811b49ad9c8a8b3bfc755a24b5417049e41abb78cb11ae5dd7793fbec7488`  
		Last Modified: Wed, 30 Mar 2022 23:09:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-data-alpine`

```console
$ docker pull influxdb@sha256:2c7fd54b2e220e1ee89c1140282eb6a02db76152631cc0d2a488aeee8d7d3cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b5e6b6568e16957d69ca9e583ffdd320dfa788823c5506e53f2e776af6200643
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 MB (31863057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae688938cada9836473dd4a74689fa22a514a82c0e4ea90eb630c659c495d230`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:31 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Tue, 29 Mar 2022 17:22:40 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:22:40 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 29 Mar 2022 17:22:40 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:22:40 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:22:40 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:22:40 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 29 Mar 2022 17:22:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:22:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d6eab0057d068b8807fee3089b02d1cae60bdaf6511b64bf7c4eb9af81b16c`  
		Last Modified: Tue, 29 Mar 2022 17:26:11 GMT  
		Size: 27.6 MB (27567388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fcd376f29d11c57dd9654d57c33b9aed8deba9245d493c4bb54166180bc880`  
		Last Modified: Tue, 29 Mar 2022 17:26:06 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec80af5ddbbd367b62c2995a959f17a3b728bab5db669fef351e8531ff93c0e`  
		Last Modified: Tue, 29 Mar 2022 17:26:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451761f81444a680e974837029f8d5c36fae234d0f8ba8f3365225915aaedb63`  
		Last Modified: Tue, 29 Mar 2022 17:26:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-meta`

```console
$ docker pull influxdb@sha256:eac0abfaed7a464f600047316adad3ee4c125165df3673fcbd0becb8530aab04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:535fc0aea9cf89ee24662a1b14b4734ca83a3b7d7fd5dfce34cee5e246a1289b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71515678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e8d639defc213c82c7aed0f2a72075d27885be90321bc4279575c49d2a9cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:37 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Wed, 30 Mar 2022 23:05:49 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:49 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 30 Mar 2022 23:05:50 GMT
EXPOSE 8091
# Wed, 30 Mar 2022 23:05:50 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:50 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:50 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a5ef3432923cab0a78b3334a4e681c9607f4d2034b9e92bae5a6867a6f0e2e`  
		Last Modified: Wed, 30 Mar 2022 23:09:23 GMT  
		Size: 10.4 MB (10439599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5771b52e55eed00db367d41862776a7f7ddb2ad8720e7243fd3112547bcd3ad`  
		Last Modified: Wed, 30 Mar 2022 23:09:21 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa824f3a6a3f28dbcc27ae20c996bd6f260bcce0b366d3a511e43e37560e884`  
		Last Modified: Wed, 30 Mar 2022 23:09:21 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9-meta-alpine`

```console
$ docker pull influxdb@sha256:a4029cf63db946014271c3e906830da686ba3aa222806f8bb52c4cf78814dbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:bde690f6657dffdd253fdf00725d5d1a23f5943a962d68143c065b71cefe619d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14704110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a60240b19ed0453230d2124da5bce9296a6490bac9865c2146b4b00d06d82f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:31 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Tue, 29 Mar 2022 17:22:49 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     (rm -rf /root/.gnupg || true) &&     rm -rf *.tar.gz* /usr/src &&     apk del .build-deps
# Tue, 29 Mar 2022 17:22:49 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 29 Mar 2022 17:22:49 GMT
EXPOSE 8091
# Tue, 29 Mar 2022 17:22:49 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:22:49 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:22:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:22:49 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7334cb38c98268485e71f891aaaa1fc520eb3fb6a247a339e496a7e783502c7`  
		Last Modified: Tue, 29 Mar 2022 17:26:26 GMT  
		Size: 10.4 MB (10409643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09331c2fd09f0fe5e059ddb807f1420a3469d3c58af83668bb416a1a61dc2104`  
		Last Modified: Tue, 29 Mar 2022 17:26:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f0a95fd76a13dd625de84dea9f75c03a9808f63d0fc3a875124976645bf39f`  
		Last Modified: Tue, 29 Mar 2022 17:26:23 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.6-data`

```console
$ docker pull influxdb@sha256:56b57de30ed18a3c48edf6b410685fe67808c5c1d892581146a69bd0dc145169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.6-data` - linux; amd64

```console
$ docker pull influxdb@sha256:6db64a003dd0be8e2fa3da8a8e79dcac9bc9c9f58213a6573085eca106b815c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88681465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0baf120185e11fa5d2e9cdcc89c96e5e56c90fb0724a96d3520b24b970e091`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:37 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Wed, 30 Mar 2022 23:05:41 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:41 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:41 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:42 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:42 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:42 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:42 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8f4a3d69c0c22b0e3d9e7e16969bf31ec608f5e24ef4978686b771811323e8`  
		Last Modified: Wed, 30 Mar 2022 23:09:10 GMT  
		Size: 27.6 MB (27604178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782474e6ac637e1f5dda88d1471243b88c53b7a3e7da56d72c38c0b9033c0a8`  
		Last Modified: Wed, 30 Mar 2022 23:09:06 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204739d56240853dfc71df7d11f0c188c2274e7fac0c4751483c66ef50b3733c`  
		Last Modified: Wed, 30 Mar 2022 23:09:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692811b49ad9c8a8b3bfc755a24b5417049e41abb78cb11ae5dd7793fbec7488`  
		Last Modified: Wed, 30 Mar 2022 23:09:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.6-data-alpine`

```console
$ docker pull influxdb@sha256:2c7fd54b2e220e1ee89c1140282eb6a02db76152631cc0d2a488aeee8d7d3cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.6-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b5e6b6568e16957d69ca9e583ffdd320dfa788823c5506e53f2e776af6200643
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 MB (31863057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae688938cada9836473dd4a74689fa22a514a82c0e4ea90eb630c659c495d230`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:31 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Tue, 29 Mar 2022 17:22:40 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:22:40 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 29 Mar 2022 17:22:40 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:22:40 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:22:40 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:22:40 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 29 Mar 2022 17:22:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:22:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d6eab0057d068b8807fee3089b02d1cae60bdaf6511b64bf7c4eb9af81b16c`  
		Last Modified: Tue, 29 Mar 2022 17:26:11 GMT  
		Size: 27.6 MB (27567388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fcd376f29d11c57dd9654d57c33b9aed8deba9245d493c4bb54166180bc880`  
		Last Modified: Tue, 29 Mar 2022 17:26:06 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec80af5ddbbd367b62c2995a959f17a3b728bab5db669fef351e8531ff93c0e`  
		Last Modified: Tue, 29 Mar 2022 17:26:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451761f81444a680e974837029f8d5c36fae234d0f8ba8f3365225915aaedb63`  
		Last Modified: Tue, 29 Mar 2022 17:26:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.6-meta`

```console
$ docker pull influxdb@sha256:eac0abfaed7a464f600047316adad3ee4c125165df3673fcbd0becb8530aab04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.6-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:535fc0aea9cf89ee24662a1b14b4734ca83a3b7d7fd5dfce34cee5e246a1289b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71515678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e8d639defc213c82c7aed0f2a72075d27885be90321bc4279575c49d2a9cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:37 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Wed, 30 Mar 2022 23:05:49 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:49 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 30 Mar 2022 23:05:50 GMT
EXPOSE 8091
# Wed, 30 Mar 2022 23:05:50 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:50 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:50 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a5ef3432923cab0a78b3334a4e681c9607f4d2034b9e92bae5a6867a6f0e2e`  
		Last Modified: Wed, 30 Mar 2022 23:09:23 GMT  
		Size: 10.4 MB (10439599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5771b52e55eed00db367d41862776a7f7ddb2ad8720e7243fd3112547bcd3ad`  
		Last Modified: Wed, 30 Mar 2022 23:09:21 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa824f3a6a3f28dbcc27ae20c996bd6f260bcce0b366d3a511e43e37560e884`  
		Last Modified: Wed, 30 Mar 2022 23:09:21 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.9.6-meta-alpine`

```console
$ docker pull influxdb@sha256:a4029cf63db946014271c3e906830da686ba3aa222806f8bb52c4cf78814dbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:1.9.6-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:bde690f6657dffdd253fdf00725d5d1a23f5943a962d68143c065b71cefe619d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14704110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a60240b19ed0453230d2124da5bce9296a6490bac9865c2146b4b00d06d82f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:31 GMT
ENV INFLUXDB_VERSION=1.9.6-c1.9.6
# Tue, 29 Mar 2022 17:22:49 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     (rm -rf /root/.gnupg || true) &&     rm -rf *.tar.gz* /usr/src &&     apk del .build-deps
# Tue, 29 Mar 2022 17:22:49 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 29 Mar 2022 17:22:49 GMT
EXPOSE 8091
# Tue, 29 Mar 2022 17:22:49 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:22:49 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:22:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:22:49 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7334cb38c98268485e71f891aaaa1fc520eb3fb6a247a339e496a7e783502c7`  
		Last Modified: Tue, 29 Mar 2022 17:26:26 GMT  
		Size: 10.4 MB (10409643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09331c2fd09f0fe5e059ddb807f1420a3469d3c58af83668bb416a1a61dc2104`  
		Last Modified: Tue, 29 Mar 2022 17:26:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f0a95fd76a13dd625de84dea9f75c03a9808f63d0fc3a875124976645bf39f`  
		Last Modified: Tue, 29 Mar 2022 17:26:23 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0`

```console
$ docker pull influxdb@sha256:3199b22c3d83d478287411931aec7582a6965fc9d73e171e6b273bc0ac394a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0` - linux; amd64

```console
$ docker pull influxdb@sha256:a5c915c7a450dd496002b7d37e6dd1a05dedbe62fbc861bdc0e6c26d75053e92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172350398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cb9a90c58041fa6402d6be3beaf1be8486a435afa98c1a31e447ed7c4c1c57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:05:55 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:05:55 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:05:58 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:05:58 GMT
ENV INFLUXDB_VERSION=2.0.9
# Wed, 30 Mar 2022 23:06:06 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 30 Mar 2022 23:06:07 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:06:07 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:06:07 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:06:07 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Wed, 30 Mar 2022 23:06:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:06:08 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:06:08 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:06:08 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:06:08 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:06:08 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:06:08 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210cc72c8f1796931ac2ce388819651f4b4cdb5bd99623547bae5660a73770e1`  
		Last Modified: Wed, 30 Mar 2022 23:09:35 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13436eca631d5b01be4a00ba60c559399662574e1abe8f93a9a0aa4fc3536f57`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 961.0 KB (960962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba69ef51e285543b380c5080feb794e437d77b322bf5406d02a4c18275fbd65d`  
		Last Modified: Wed, 30 Mar 2022 23:09:41 GMT  
		Size: 103.1 MB (103090642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fbfa930edbd4fc7d357c7a01e6bfb508f894cc4470d44fa4a2ec16c9106dc6`  
		Last Modified: Wed, 30 Mar 2022 23:09:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1607d0a086cd9cd79754f90b38c8b1b2178f8b1e55eda9792a6579668c62ec44`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e797924e061d7121c18647921bb3060c5cda9ddbfc761fc1ce35ca9e635c7f1`  
		Last Modified: Wed, 30 Mar 2022 23:09:32 GMT  
		Size: 4.9 KB (4945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:73273667c46d64d6f0f20e1b406ec9f8bf6fd26339596502cb521a4159a427e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.1 MB (174143023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c81bb401efe03a2c2c07755d5ce66854d5abbae522398facc17cf93eaf7e1fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:43 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:21:44 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:21:48 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:21:48 GMT
ENV INFLUXDB_VERSION=2.0.9
# Wed, 30 Mar 2022 23:21:56 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 30 Mar 2022 23:21:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:21:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:22:00 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:22:01 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Wed, 30 Mar 2022 23:22:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:22:02 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:22:03 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:22:04 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:22:05 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:22:06 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:22:07 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852f48a9439fa6ebf298c8036cafc7a4fed044921009c423f090fa5c2f7a799a`  
		Last Modified: Wed, 30 Mar 2022 23:23:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c67ea50143c728fffa089fbfcf7df1b1a2e800ab3350e2aed93291eaaaf1fa7`  
		Last Modified: Wed, 30 Mar 2022 23:23:54 GMT  
		Size: 896.3 KB (896337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa8eee3bbcc2a05e10b509b77092c4fab995de116ba9ee1c668d259a60c89c4`  
		Last Modified: Wed, 30 Mar 2022 23:24:04 GMT  
		Size: 106.5 MB (106526968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f993776c3f37c52edc4f5c89071e074e1a78766f272870f599922677f8c2abe`  
		Last Modified: Wed, 30 Mar 2022 23:23:53 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc91e1f3f901d572ac0b49d1ce356d88cf33d04792aa68bfd5474b4bca602e2f`  
		Last Modified: Wed, 30 Mar 2022 23:23:53 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51fbe92bcf55b7ddb8c97ba90bd7b75ba1fecb276b3a637cf8156bba81c6b29`  
		Last Modified: Wed, 30 Mar 2022 23:23:53 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0-alpine`

```console
$ docker pull influxdb@sha256:dbc07a577735decdfa85a5969132a20611662f6cc19fc3821269166b8245d966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c6f25554b44ed1ce53747e10e9bda9045a4b8d6892c9dc3ff78648ef27552735
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116713326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8385d2229c7b967b23e1000e4f83e0cc5e99eeabc8b5fab7d49b70201642325a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:22:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:56 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 29 Mar 2022 17:22:56 GMT
ENV GOSU_VER=1.12
# Tue, 29 Mar 2022 17:22:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Mar 2022 17:22:59 GMT
ENV INFLUXDB_VERSION=2.0.9
# Tue, 29 Mar 2022 17:23:07 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Tue, 29 Mar 2022 17:23:08 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 29 Mar 2022 17:23:08 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 29 Mar 2022 17:23:08 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 29 Mar 2022 17:23:08 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Tue, 29 Mar 2022 17:23:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:23:08 GMT
CMD ["influxd"]
# Tue, 29 Mar 2022 17:23:08 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:23:08 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 29 Mar 2022 17:23:09 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 29 Mar 2022 17:23:09 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 29 Mar 2022 17:23:09 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54f939f5c2396bf88421fc5bbf7a5ec37257cf48535c4da43cb6d9ed1da8f2c`  
		Last Modified: Tue, 29 Mar 2022 17:26:42 GMT  
		Size: 9.8 MB (9836775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6498eb56d88fa614863cfc9ae7e046351e0ca756946077b3d892cba7ecc4455`  
		Last Modified: Tue, 29 Mar 2022 17:26:40 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e026a7e4cc2b9efd9bf03aaabaab62ebe77e5a742bc4c29f4334212b6d9d2a5`  
		Last Modified: Tue, 29 Mar 2022 17:26:38 GMT  
		Size: 960.6 KB (960613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78239d27cf04a15c73a8ef03cf2ce75b66addaf1fe1da903c0af442c19fe2acb`  
		Last Modified: Tue, 29 Mar 2022 17:26:46 GMT  
		Size: 103.1 MB (103090679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c2414424c8bb22982a311cb094c9830fcd1e75969989c498c9f681b4e58f95`  
		Last Modified: Tue, 29 Mar 2022 17:26:38 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1206d13e266aa12a09872dc361d543f8efbdf8a64d51368a172f7e05e8c63d`  
		Last Modified: Tue, 29 Mar 2022 17:26:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff91636003176eba73bd720e8c259de685838aff88b72f5af2e8a0e11e0ae5f`  
		Last Modified: Tue, 29 Mar 2022 17:26:38 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:dda981f6f49da91ccbf99d17fd1ad10ec11c261b1b684a73aa2c86c45d9a5377
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119819806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a027902951a09dccb50b6f82e4897f14bd9179124de2eb90c517c3d85e5396bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:12 GMT
ADD file:d0894581cf2fb7d7911ecb25bf0368675197db96d762977964ffc3a7ae8c774c in / 
# Tue, 29 Mar 2022 00:40:13 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 11:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 11:55:20 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 29 Mar 2022 11:55:21 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 29 Mar 2022 11:55:22 GMT
ENV GOSU_VER=1.12
# Tue, 29 Mar 2022 11:55:26 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Mar 2022 11:55:27 GMT
ENV INFLUXDB_VERSION=2.0.9
# Tue, 29 Mar 2022 11:55:40 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Tue, 29 Mar 2022 11:55:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 29 Mar 2022 11:55:42 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 29 Mar 2022 11:55:44 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 29 Mar 2022 11:55:45 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Tue, 29 Mar 2022 11:55:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 11:55:46 GMT
CMD ["influxd"]
# Tue, 29 Mar 2022 11:55:47 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 11:55:48 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 29 Mar 2022 11:55:49 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 29 Mar 2022 11:55:50 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 29 Mar 2022 11:55:51 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:810d54c7e01bab9975c1fb485c543715b76de7708166132520dfec0fc32c3754`  
		Last Modified: Tue, 29 Mar 2022 00:41:26 GMT  
		Size: 2.7 MB (2717494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d05fbec0985dd4e2437413ad065a5e9de75bd6c2b3d8ddf507f114b646ae286`  
		Last Modified: Tue, 29 Mar 2022 11:57:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1d1662bf96050f7b6919306a6d549c24ffdd1b8c572aeb04f46aaed1f1261b`  
		Last Modified: Tue, 29 Mar 2022 11:57:14 GMT  
		Size: 9.7 MB (9672483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0f2be565408f265515dccdc66af14c3289ea56a405f7ddc1377cb21ee637b7`  
		Last Modified: Tue, 29 Mar 2022 11:57:12 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e0a53cc77406effa83102261ce01a8855c9bd7c7ed944976b69bb337a8dda7`  
		Last Modified: Tue, 29 Mar 2022 11:57:10 GMT  
		Size: 896.1 KB (896076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dac3e9348b0d2266c4ba73b58002c390560eb7ea10e62fdf8df626b62c2b8d5`  
		Last Modified: Tue, 29 Mar 2022 11:57:21 GMT  
		Size: 106.5 MB (106526971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3356f6d8a9bba2b1e98bbfb1f8673356d980faaf9056b4858ad410f28323f534`  
		Last Modified: Tue, 29 Mar 2022 11:57:10 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214c9f61b85c8b804e0949dcfe0cc4897a7bc9c3258d4e6cb9c053660342fc3`  
		Last Modified: Tue, 29 Mar 2022 11:57:10 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc1166df3f370637b58fb18236949d2eb77fb8c068d5c877e8c98857efbf017`  
		Last Modified: Tue, 29 Mar 2022 11:57:10 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0.9`

```console
$ docker pull influxdb@sha256:3199b22c3d83d478287411931aec7582a6965fc9d73e171e6b273bc0ac394a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0.9` - linux; amd64

```console
$ docker pull influxdb@sha256:a5c915c7a450dd496002b7d37e6dd1a05dedbe62fbc861bdc0e6c26d75053e92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172350398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cb9a90c58041fa6402d6be3beaf1be8486a435afa98c1a31e447ed7c4c1c57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:05:55 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:05:55 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:05:58 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:05:58 GMT
ENV INFLUXDB_VERSION=2.0.9
# Wed, 30 Mar 2022 23:06:06 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 30 Mar 2022 23:06:07 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:06:07 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:06:07 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:06:07 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Wed, 30 Mar 2022 23:06:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:06:08 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:06:08 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:06:08 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:06:08 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:06:08 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:06:08 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210cc72c8f1796931ac2ce388819651f4b4cdb5bd99623547bae5660a73770e1`  
		Last Modified: Wed, 30 Mar 2022 23:09:35 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13436eca631d5b01be4a00ba60c559399662574e1abe8f93a9a0aa4fc3536f57`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 961.0 KB (960962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba69ef51e285543b380c5080feb794e437d77b322bf5406d02a4c18275fbd65d`  
		Last Modified: Wed, 30 Mar 2022 23:09:41 GMT  
		Size: 103.1 MB (103090642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fbfa930edbd4fc7d357c7a01e6bfb508f894cc4470d44fa4a2ec16c9106dc6`  
		Last Modified: Wed, 30 Mar 2022 23:09:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1607d0a086cd9cd79754f90b38c8b1b2178f8b1e55eda9792a6579668c62ec44`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e797924e061d7121c18647921bb3060c5cda9ddbfc761fc1ce35ca9e635c7f1`  
		Last Modified: Wed, 30 Mar 2022 23:09:32 GMT  
		Size: 4.9 KB (4945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0.9` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:73273667c46d64d6f0f20e1b406ec9f8bf6fd26339596502cb521a4159a427e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.1 MB (174143023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c81bb401efe03a2c2c07755d5ce66854d5abbae522398facc17cf93eaf7e1fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:43 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:21:44 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:21:48 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:21:48 GMT
ENV INFLUXDB_VERSION=2.0.9
# Wed, 30 Mar 2022 23:21:56 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 30 Mar 2022 23:21:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:21:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:22:00 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:22:01 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Wed, 30 Mar 2022 23:22:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:22:02 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:22:03 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:22:04 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:22:05 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:22:06 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:22:07 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852f48a9439fa6ebf298c8036cafc7a4fed044921009c423f090fa5c2f7a799a`  
		Last Modified: Wed, 30 Mar 2022 23:23:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c67ea50143c728fffa089fbfcf7df1b1a2e800ab3350e2aed93291eaaaf1fa7`  
		Last Modified: Wed, 30 Mar 2022 23:23:54 GMT  
		Size: 896.3 KB (896337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa8eee3bbcc2a05e10b509b77092c4fab995de116ba9ee1c668d259a60c89c4`  
		Last Modified: Wed, 30 Mar 2022 23:24:04 GMT  
		Size: 106.5 MB (106526968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f993776c3f37c52edc4f5c89071e074e1a78766f272870f599922677f8c2abe`  
		Last Modified: Wed, 30 Mar 2022 23:23:53 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc91e1f3f901d572ac0b49d1ce356d88cf33d04792aa68bfd5474b4bca602e2f`  
		Last Modified: Wed, 30 Mar 2022 23:23:53 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51fbe92bcf55b7ddb8c97ba90bd7b75ba1fecb276b3a637cf8156bba81c6b29`  
		Last Modified: Wed, 30 Mar 2022 23:23:53 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0.9-alpine`

```console
$ docker pull influxdb@sha256:dbc07a577735decdfa85a5969132a20611662f6cc19fc3821269166b8245d966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0.9-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c6f25554b44ed1ce53747e10e9bda9045a4b8d6892c9dc3ff78648ef27552735
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116713326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8385d2229c7b967b23e1000e4f83e0cc5e99eeabc8b5fab7d49b70201642325a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:22:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:56 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 29 Mar 2022 17:22:56 GMT
ENV GOSU_VER=1.12
# Tue, 29 Mar 2022 17:22:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Mar 2022 17:22:59 GMT
ENV INFLUXDB_VERSION=2.0.9
# Tue, 29 Mar 2022 17:23:07 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Tue, 29 Mar 2022 17:23:08 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 29 Mar 2022 17:23:08 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 29 Mar 2022 17:23:08 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 29 Mar 2022 17:23:08 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Tue, 29 Mar 2022 17:23:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:23:08 GMT
CMD ["influxd"]
# Tue, 29 Mar 2022 17:23:08 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:23:08 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 29 Mar 2022 17:23:09 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 29 Mar 2022 17:23:09 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 29 Mar 2022 17:23:09 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54f939f5c2396bf88421fc5bbf7a5ec37257cf48535c4da43cb6d9ed1da8f2c`  
		Last Modified: Tue, 29 Mar 2022 17:26:42 GMT  
		Size: 9.8 MB (9836775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6498eb56d88fa614863cfc9ae7e046351e0ca756946077b3d892cba7ecc4455`  
		Last Modified: Tue, 29 Mar 2022 17:26:40 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e026a7e4cc2b9efd9bf03aaabaab62ebe77e5a742bc4c29f4334212b6d9d2a5`  
		Last Modified: Tue, 29 Mar 2022 17:26:38 GMT  
		Size: 960.6 KB (960613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78239d27cf04a15c73a8ef03cf2ce75b66addaf1fe1da903c0af442c19fe2acb`  
		Last Modified: Tue, 29 Mar 2022 17:26:46 GMT  
		Size: 103.1 MB (103090679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c2414424c8bb22982a311cb094c9830fcd1e75969989c498c9f681b4e58f95`  
		Last Modified: Tue, 29 Mar 2022 17:26:38 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1206d13e266aa12a09872dc361d543f8efbdf8a64d51368a172f7e05e8c63d`  
		Last Modified: Tue, 29 Mar 2022 17:26:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff91636003176eba73bd720e8c259de685838aff88b72f5af2e8a0e11e0ae5f`  
		Last Modified: Tue, 29 Mar 2022 17:26:38 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0.9-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:dda981f6f49da91ccbf99d17fd1ad10ec11c261b1b684a73aa2c86c45d9a5377
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119819806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a027902951a09dccb50b6f82e4897f14bd9179124de2eb90c517c3d85e5396bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:12 GMT
ADD file:d0894581cf2fb7d7911ecb25bf0368675197db96d762977964ffc3a7ae8c774c in / 
# Tue, 29 Mar 2022 00:40:13 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 11:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 11:55:20 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 29 Mar 2022 11:55:21 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 29 Mar 2022 11:55:22 GMT
ENV GOSU_VER=1.12
# Tue, 29 Mar 2022 11:55:26 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Mar 2022 11:55:27 GMT
ENV INFLUXDB_VERSION=2.0.9
# Tue, 29 Mar 2022 11:55:40 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Tue, 29 Mar 2022 11:55:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 29 Mar 2022 11:55:42 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 29 Mar 2022 11:55:44 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 29 Mar 2022 11:55:45 GMT
COPY file:f5ca019f6dbd57be875676710efe0403265acecd892fdd8af6f1b2af0b5129bb in /entrypoint.sh 
# Tue, 29 Mar 2022 11:55:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 11:55:46 GMT
CMD ["influxd"]
# Tue, 29 Mar 2022 11:55:47 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 11:55:48 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 29 Mar 2022 11:55:49 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 29 Mar 2022 11:55:50 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 29 Mar 2022 11:55:51 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:810d54c7e01bab9975c1fb485c543715b76de7708166132520dfec0fc32c3754`  
		Last Modified: Tue, 29 Mar 2022 00:41:26 GMT  
		Size: 2.7 MB (2717494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d05fbec0985dd4e2437413ad065a5e9de75bd6c2b3d8ddf507f114b646ae286`  
		Last Modified: Tue, 29 Mar 2022 11:57:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1d1662bf96050f7b6919306a6d549c24ffdd1b8c572aeb04f46aaed1f1261b`  
		Last Modified: Tue, 29 Mar 2022 11:57:14 GMT  
		Size: 9.7 MB (9672483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0f2be565408f265515dccdc66af14c3289ea56a405f7ddc1377cb21ee637b7`  
		Last Modified: Tue, 29 Mar 2022 11:57:12 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e0a53cc77406effa83102261ce01a8855c9bd7c7ed944976b69bb337a8dda7`  
		Last Modified: Tue, 29 Mar 2022 11:57:10 GMT  
		Size: 896.1 KB (896076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dac3e9348b0d2266c4ba73b58002c390560eb7ea10e62fdf8df626b62c2b8d5`  
		Last Modified: Tue, 29 Mar 2022 11:57:21 GMT  
		Size: 106.5 MB (106526971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3356f6d8a9bba2b1e98bbfb1f8673356d980faaf9056b4858ad410f28323f534`  
		Last Modified: Tue, 29 Mar 2022 11:57:10 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214c9f61b85c8b804e0949dcfe0cc4897a7bc9c3258d4e6cb9c053660342fc3`  
		Last Modified: Tue, 29 Mar 2022 11:57:10 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc1166df3f370637b58fb18236949d2eb77fb8c068d5c877e8c98857efbf017`  
		Last Modified: Tue, 29 Mar 2022 11:57:10 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.1`

```console
$ docker pull influxdb@sha256:2f6855f9556b71dbcae60e1065f4710559f14e1cd94c7c3ee9768b64c4e1e4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.1` - linux; amd64

```console
$ docker pull influxdb@sha256:6c3cc5ef911b8c16979f710651675456caf5688ee61775e9d7dd8aefa188dacf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182909101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c756b1d9ee5bf83999f7cbadd8b511e748b4e0d38095bc8421d56e7e24216c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:05:55 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:05:55 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:05:58 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:06:12 GMT
ENV INFLUXDB_VERSION=2.1.1
# Wed, 30 Mar 2022 23:06:22 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 30 Mar 2022 23:06:22 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Wed, 30 Mar 2022 23:06:26 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 30 Mar 2022 23:06:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:06:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:06:26 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:06:27 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:06:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:06:27 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:06:27 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:06:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210cc72c8f1796931ac2ce388819651f4b4cdb5bd99623547bae5660a73770e1`  
		Last Modified: Wed, 30 Mar 2022 23:09:35 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13436eca631d5b01be4a00ba60c559399662574e1abe8f93a9a0aa4fc3536f57`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 961.0 KB (960962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793e652a43b509f8be74eb5064294d379224d59cf97316124fb499858445ef1`  
		Last Modified: Wed, 30 Mar 2022 23:10:07 GMT  
		Size: 108.3 MB (108324795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b482d9f0118895e8c347c58cbd312d1dfcca4330cf1ff83adc712580775e64f`  
		Last Modified: Wed, 30 Mar 2022 23:09:59 GMT  
		Size: 5.3 MB (5324479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2947646d0e18c37cc4fcc392b2cd653b762a7940fed46ee905128f6dbca79cea`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3282f6fa09cdf60983e54f1483883179f885470a104eeb790e88ab1be5d18d0`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ed2126a186f0abce1171df1dc7e227f047395d57632f220dfc30630bbcfd2f`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.1` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b3905f1e9ffb41a7f9fd0ce44eed59301256f1186fd7549ea2f622141215815d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183414472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90d3dc0511263ca69dbd9901272be8f4e080ce9403cda81ae40ce68d78efbef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:43 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:21:44 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:21:48 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:22:18 GMT
ENV INFLUXDB_VERSION=2.1.1
# Wed, 30 Mar 2022 23:22:25 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 30 Mar 2022 23:22:25 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Wed, 30 Mar 2022 23:22:29 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 30 Mar 2022 23:22:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:22:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:22:32 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:22:33 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:22:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:22:34 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:22:35 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:22:36 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:22:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:22:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:22:39 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852f48a9439fa6ebf298c8036cafc7a4fed044921009c423f090fa5c2f7a799a`  
		Last Modified: Wed, 30 Mar 2022 23:23:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c67ea50143c728fffa089fbfcf7df1b1a2e800ab3350e2aed93291eaaaf1fa7`  
		Last Modified: Wed, 30 Mar 2022 23:23:54 GMT  
		Size: 896.3 KB (896337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6874725511156ff9e815819dffafee7879b8bab6820901484dab85ba06bf9b76`  
		Last Modified: Wed, 30 Mar 2022 23:24:26 GMT  
		Size: 110.9 MB (110891613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4fe266bd0bca43087df62a3f30c9fb7668277a6f5f8ca3b039aff3f0a02816`  
		Last Modified: Wed, 30 Mar 2022 23:24:18 GMT  
		Size: 4.9 MB (4906728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c13758147cee9ae50ab7e4622cd7b280b4931b06e268aee29bbc31d97b978fc`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea839f94b295d7eafff699c715006e4e6695743e971d7c314ccb624ea0c670e`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282331cef6cbe0a9aa18ba4dfc9d6e08a6888c6110f8b2f856e4e15e0c61fe1b`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.1-alpine`

```console
$ docker pull influxdb@sha256:0efcbce50b73b301b26155700e74af8deb57c9b31d98938633e6cafcffc7fdc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.1-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ffbdbaead0eead210dd1775f25a7c3f18026eaa6d5c3607a080d31450d237263
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212eddb5079147383f90fa1e58361e29cbbf828f6237f9a2c770f40106995438`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:22:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:56 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 29 Mar 2022 17:22:56 GMT
ENV GOSU_VER=1.12
# Tue, 29 Mar 2022 17:22:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Mar 2022 17:23:15 GMT
ENV INFLUXDB_VERSION=2.1.1
# Tue, 29 Mar 2022 17:23:22 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Tue, 29 Mar 2022 17:23:23 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Tue, 29 Mar 2022 17:23:26 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Tue, 29 Mar 2022 17:23:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 29 Mar 2022 17:23:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 29 Mar 2022 17:23:26 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 29 Mar 2022 17:23:27 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Tue, 29 Mar 2022 17:23:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:23:27 GMT
CMD ["influxd"]
# Tue, 29 Mar 2022 17:23:27 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:23:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 29 Mar 2022 17:23:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 29 Mar 2022 17:23:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 29 Mar 2022 17:23:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54f939f5c2396bf88421fc5bbf7a5ec37257cf48535c4da43cb6d9ed1da8f2c`  
		Last Modified: Tue, 29 Mar 2022 17:26:42 GMT  
		Size: 9.8 MB (9836775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6498eb56d88fa614863cfc9ae7e046351e0ca756946077b3d892cba7ecc4455`  
		Last Modified: Tue, 29 Mar 2022 17:26:40 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e026a7e4cc2b9efd9bf03aaabaab62ebe77e5a742bc4c29f4334212b6d9d2a5`  
		Last Modified: Tue, 29 Mar 2022 17:26:38 GMT  
		Size: 960.6 KB (960613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49465b4c6717933ae61b016e1329b4a872a6680e9ba12b999f78379dbbf6481`  
		Last Modified: Tue, 29 Mar 2022 17:27:06 GMT  
		Size: 108.3 MB (108324794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a258054a4458994b79a99613a9a28cf1f4cefd23277b78529824b759431ea0f`  
		Last Modified: Tue, 29 Mar 2022 17:26:59 GMT  
		Size: 5.3 MB (5324482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76f2868aaa9343cc3fa34a86924283389ae8c51a85effffaceab5669f44149b`  
		Last Modified: Tue, 29 Mar 2022 17:26:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f774547a4e5516dc78049766850def302e08785f61738696f4b2fd3a4a77ed`  
		Last Modified: Tue, 29 Mar 2022 17:26:58 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab14f515b10e3468c6aa853adb26510fd536d7317b72ab755a92e23a6eeb5ff`  
		Last Modified: Tue, 29 Mar 2022 17:26:58 GMT  
		Size: 5.0 KB (5017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ddff68e6377af62bd283f4e9f143d2b9d2b9ea3df07d68144e54d8e5136f5949
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129091224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b620a352032301f93661396eb1fca8a4107e72d45b1409b8c9bf0c7fae7f4a8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:12 GMT
ADD file:d0894581cf2fb7d7911ecb25bf0368675197db96d762977964ffc3a7ae8c774c in / 
# Tue, 29 Mar 2022 00:40:13 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 11:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 11:55:20 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 29 Mar 2022 11:55:21 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 29 Mar 2022 11:55:22 GMT
ENV GOSU_VER=1.12
# Tue, 29 Mar 2022 11:55:26 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Mar 2022 11:56:05 GMT
ENV INFLUXDB_VERSION=2.1.1
# Tue, 29 Mar 2022 11:56:14 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Tue, 29 Mar 2022 11:56:14 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Tue, 29 Mar 2022 11:56:19 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Tue, 29 Mar 2022 11:56:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 29 Mar 2022 11:56:21 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 29 Mar 2022 11:56:23 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 29 Mar 2022 11:56:24 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Tue, 29 Mar 2022 11:56:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 11:56:25 GMT
CMD ["influxd"]
# Tue, 29 Mar 2022 11:56:26 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 11:56:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 29 Mar 2022 11:56:28 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 29 Mar 2022 11:56:29 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 29 Mar 2022 11:56:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:810d54c7e01bab9975c1fb485c543715b76de7708166132520dfec0fc32c3754`  
		Last Modified: Tue, 29 Mar 2022 00:41:26 GMT  
		Size: 2.7 MB (2717494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d05fbec0985dd4e2437413ad065a5e9de75bd6c2b3d8ddf507f114b646ae286`  
		Last Modified: Tue, 29 Mar 2022 11:57:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1d1662bf96050f7b6919306a6d549c24ffdd1b8c572aeb04f46aaed1f1261b`  
		Last Modified: Tue, 29 Mar 2022 11:57:14 GMT  
		Size: 9.7 MB (9672483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0f2be565408f265515dccdc66af14c3289ea56a405f7ddc1377cb21ee637b7`  
		Last Modified: Tue, 29 Mar 2022 11:57:12 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e0a53cc77406effa83102261ce01a8855c9bd7c7ed944976b69bb337a8dda7`  
		Last Modified: Tue, 29 Mar 2022 11:57:10 GMT  
		Size: 896.1 KB (896076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81bc505e8165f74a9d27dd342d7d3d79f685491cb6e9c9abe729578c8149061`  
		Last Modified: Tue, 29 Mar 2022 11:57:43 GMT  
		Size: 110.9 MB (110891593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22645a3eccc37c9e1f2aed8d97dacd06be4b114efca585f300ea4ed68802df0`  
		Last Modified: Tue, 29 Mar 2022 11:57:35 GMT  
		Size: 4.9 MB (4906732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e37f4bf83c351e8926f204ee2d9f204cfea970ac8b5ab3e31f98d5659d5d0f`  
		Last Modified: Tue, 29 Mar 2022 11:57:34 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d4a874b49998b6c39fca72812e50c58c6e1d1c9538d5118d6e4e89dcf088bd`  
		Last Modified: Tue, 29 Mar 2022 11:57:34 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1d3f354f0bfd5fec69a97e80a505a7f3fa26c0952106699c8e0078bb699901`  
		Last Modified: Tue, 29 Mar 2022 11:57:34 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.1.1`

```console
$ docker pull influxdb@sha256:2f6855f9556b71dbcae60e1065f4710559f14e1cd94c7c3ee9768b64c4e1e4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.1.1` - linux; amd64

```console
$ docker pull influxdb@sha256:6c3cc5ef911b8c16979f710651675456caf5688ee61775e9d7dd8aefa188dacf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182909101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c756b1d9ee5bf83999f7cbadd8b511e748b4e0d38095bc8421d56e7e24216c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:05:55 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:05:55 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:05:58 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:06:12 GMT
ENV INFLUXDB_VERSION=2.1.1
# Wed, 30 Mar 2022 23:06:22 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 30 Mar 2022 23:06:22 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Wed, 30 Mar 2022 23:06:26 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 30 Mar 2022 23:06:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:06:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:06:26 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:06:27 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:06:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:06:27 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:06:27 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:06:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210cc72c8f1796931ac2ce388819651f4b4cdb5bd99623547bae5660a73770e1`  
		Last Modified: Wed, 30 Mar 2022 23:09:35 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13436eca631d5b01be4a00ba60c559399662574e1abe8f93a9a0aa4fc3536f57`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 961.0 KB (960962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793e652a43b509f8be74eb5064294d379224d59cf97316124fb499858445ef1`  
		Last Modified: Wed, 30 Mar 2022 23:10:07 GMT  
		Size: 108.3 MB (108324795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b482d9f0118895e8c347c58cbd312d1dfcca4330cf1ff83adc712580775e64f`  
		Last Modified: Wed, 30 Mar 2022 23:09:59 GMT  
		Size: 5.3 MB (5324479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2947646d0e18c37cc4fcc392b2cd653b762a7940fed46ee905128f6dbca79cea`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3282f6fa09cdf60983e54f1483883179f885470a104eeb790e88ab1be5d18d0`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ed2126a186f0abce1171df1dc7e227f047395d57632f220dfc30630bbcfd2f`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.1.1` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b3905f1e9ffb41a7f9fd0ce44eed59301256f1186fd7549ea2f622141215815d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183414472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90d3dc0511263ca69dbd9901272be8f4e080ce9403cda81ae40ce68d78efbef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:43 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:21:44 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:21:48 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:22:18 GMT
ENV INFLUXDB_VERSION=2.1.1
# Wed, 30 Mar 2022 23:22:25 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 30 Mar 2022 23:22:25 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Wed, 30 Mar 2022 23:22:29 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 30 Mar 2022 23:22:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:22:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:22:32 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:22:33 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:22:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:22:34 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:22:35 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:22:36 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:22:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:22:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:22:39 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852f48a9439fa6ebf298c8036cafc7a4fed044921009c423f090fa5c2f7a799a`  
		Last Modified: Wed, 30 Mar 2022 23:23:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c67ea50143c728fffa089fbfcf7df1b1a2e800ab3350e2aed93291eaaaf1fa7`  
		Last Modified: Wed, 30 Mar 2022 23:23:54 GMT  
		Size: 896.3 KB (896337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6874725511156ff9e815819dffafee7879b8bab6820901484dab85ba06bf9b76`  
		Last Modified: Wed, 30 Mar 2022 23:24:26 GMT  
		Size: 110.9 MB (110891613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4fe266bd0bca43087df62a3f30c9fb7668277a6f5f8ca3b039aff3f0a02816`  
		Last Modified: Wed, 30 Mar 2022 23:24:18 GMT  
		Size: 4.9 MB (4906728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c13758147cee9ae50ab7e4622cd7b280b4931b06e268aee29bbc31d97b978fc`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea839f94b295d7eafff699c715006e4e6695743e971d7c314ccb624ea0c670e`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282331cef6cbe0a9aa18ba4dfc9d6e08a6888c6110f8b2f856e4e15e0c61fe1b`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.1.1-alpine`

```console
$ docker pull influxdb@sha256:0efcbce50b73b301b26155700e74af8deb57c9b31d98938633e6cafcffc7fdc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.1.1-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ffbdbaead0eead210dd1775f25a7c3f18026eaa6d5c3607a080d31450d237263
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212eddb5079147383f90fa1e58361e29cbbf828f6237f9a2c770f40106995438`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:22:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:56 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 29 Mar 2022 17:22:56 GMT
ENV GOSU_VER=1.12
# Tue, 29 Mar 2022 17:22:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Mar 2022 17:23:15 GMT
ENV INFLUXDB_VERSION=2.1.1
# Tue, 29 Mar 2022 17:23:22 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Tue, 29 Mar 2022 17:23:23 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Tue, 29 Mar 2022 17:23:26 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Tue, 29 Mar 2022 17:23:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 29 Mar 2022 17:23:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 29 Mar 2022 17:23:26 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 29 Mar 2022 17:23:27 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Tue, 29 Mar 2022 17:23:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:23:27 GMT
CMD ["influxd"]
# Tue, 29 Mar 2022 17:23:27 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:23:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 29 Mar 2022 17:23:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 29 Mar 2022 17:23:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 29 Mar 2022 17:23:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54f939f5c2396bf88421fc5bbf7a5ec37257cf48535c4da43cb6d9ed1da8f2c`  
		Last Modified: Tue, 29 Mar 2022 17:26:42 GMT  
		Size: 9.8 MB (9836775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6498eb56d88fa614863cfc9ae7e046351e0ca756946077b3d892cba7ecc4455`  
		Last Modified: Tue, 29 Mar 2022 17:26:40 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e026a7e4cc2b9efd9bf03aaabaab62ebe77e5a742bc4c29f4334212b6d9d2a5`  
		Last Modified: Tue, 29 Mar 2022 17:26:38 GMT  
		Size: 960.6 KB (960613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49465b4c6717933ae61b016e1329b4a872a6680e9ba12b999f78379dbbf6481`  
		Last Modified: Tue, 29 Mar 2022 17:27:06 GMT  
		Size: 108.3 MB (108324794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a258054a4458994b79a99613a9a28cf1f4cefd23277b78529824b759431ea0f`  
		Last Modified: Tue, 29 Mar 2022 17:26:59 GMT  
		Size: 5.3 MB (5324482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76f2868aaa9343cc3fa34a86924283389ae8c51a85effffaceab5669f44149b`  
		Last Modified: Tue, 29 Mar 2022 17:26:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f774547a4e5516dc78049766850def302e08785f61738696f4b2fd3a4a77ed`  
		Last Modified: Tue, 29 Mar 2022 17:26:58 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab14f515b10e3468c6aa853adb26510fd536d7317b72ab755a92e23a6eeb5ff`  
		Last Modified: Tue, 29 Mar 2022 17:26:58 GMT  
		Size: 5.0 KB (5017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.1.1-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ddff68e6377af62bd283f4e9f143d2b9d2b9ea3df07d68144e54d8e5136f5949
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129091224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b620a352032301f93661396eb1fca8a4107e72d45b1409b8c9bf0c7fae7f4a8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:12 GMT
ADD file:d0894581cf2fb7d7911ecb25bf0368675197db96d762977964ffc3a7ae8c774c in / 
# Tue, 29 Mar 2022 00:40:13 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 11:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 11:55:20 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 29 Mar 2022 11:55:21 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 29 Mar 2022 11:55:22 GMT
ENV GOSU_VER=1.12
# Tue, 29 Mar 2022 11:55:26 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Mar 2022 11:56:05 GMT
ENV INFLUXDB_VERSION=2.1.1
# Tue, 29 Mar 2022 11:56:14 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Tue, 29 Mar 2022 11:56:14 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Tue, 29 Mar 2022 11:56:19 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Tue, 29 Mar 2022 11:56:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 29 Mar 2022 11:56:21 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 29 Mar 2022 11:56:23 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 29 Mar 2022 11:56:24 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Tue, 29 Mar 2022 11:56:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 11:56:25 GMT
CMD ["influxd"]
# Tue, 29 Mar 2022 11:56:26 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 11:56:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 29 Mar 2022 11:56:28 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 29 Mar 2022 11:56:29 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 29 Mar 2022 11:56:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:810d54c7e01bab9975c1fb485c543715b76de7708166132520dfec0fc32c3754`  
		Last Modified: Tue, 29 Mar 2022 00:41:26 GMT  
		Size: 2.7 MB (2717494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d05fbec0985dd4e2437413ad065a5e9de75bd6c2b3d8ddf507f114b646ae286`  
		Last Modified: Tue, 29 Mar 2022 11:57:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1d1662bf96050f7b6919306a6d549c24ffdd1b8c572aeb04f46aaed1f1261b`  
		Last Modified: Tue, 29 Mar 2022 11:57:14 GMT  
		Size: 9.7 MB (9672483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0f2be565408f265515dccdc66af14c3289ea56a405f7ddc1377cb21ee637b7`  
		Last Modified: Tue, 29 Mar 2022 11:57:12 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e0a53cc77406effa83102261ce01a8855c9bd7c7ed944976b69bb337a8dda7`  
		Last Modified: Tue, 29 Mar 2022 11:57:10 GMT  
		Size: 896.1 KB (896076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81bc505e8165f74a9d27dd342d7d3d79f685491cb6e9c9abe729578c8149061`  
		Last Modified: Tue, 29 Mar 2022 11:57:43 GMT  
		Size: 110.9 MB (110891593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22645a3eccc37c9e1f2aed8d97dacd06be4b114efca585f300ea4ed68802df0`  
		Last Modified: Tue, 29 Mar 2022 11:57:35 GMT  
		Size: 4.9 MB (4906732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e37f4bf83c351e8926f204ee2d9f204cfea970ac8b5ab3e31f98d5659d5d0f`  
		Last Modified: Tue, 29 Mar 2022 11:57:34 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d4a874b49998b6c39fca72812e50c58c6e1d1c9538d5118d6e4e89dcf088bd`  
		Last Modified: Tue, 29 Mar 2022 11:57:34 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1d3f354f0bfd5fec69a97e80a505a7f3fa26c0952106699c8e0078bb699901`  
		Last Modified: Tue, 29 Mar 2022 11:57:34 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:0efcbce50b73b301b26155700e74af8deb57c9b31d98938633e6cafcffc7fdc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ffbdbaead0eead210dd1775f25a7c3f18026eaa6d5c3607a080d31450d237263
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212eddb5079147383f90fa1e58361e29cbbf828f6237f9a2c770f40106995438`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:22:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:56 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 29 Mar 2022 17:22:56 GMT
ENV GOSU_VER=1.12
# Tue, 29 Mar 2022 17:22:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Mar 2022 17:23:15 GMT
ENV INFLUXDB_VERSION=2.1.1
# Tue, 29 Mar 2022 17:23:22 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Tue, 29 Mar 2022 17:23:23 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Tue, 29 Mar 2022 17:23:26 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Tue, 29 Mar 2022 17:23:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 29 Mar 2022 17:23:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 29 Mar 2022 17:23:26 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 29 Mar 2022 17:23:27 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Tue, 29 Mar 2022 17:23:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:23:27 GMT
CMD ["influxd"]
# Tue, 29 Mar 2022 17:23:27 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:23:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 29 Mar 2022 17:23:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 29 Mar 2022 17:23:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 29 Mar 2022 17:23:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54f939f5c2396bf88421fc5bbf7a5ec37257cf48535c4da43cb6d9ed1da8f2c`  
		Last Modified: Tue, 29 Mar 2022 17:26:42 GMT  
		Size: 9.8 MB (9836775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6498eb56d88fa614863cfc9ae7e046351e0ca756946077b3d892cba7ecc4455`  
		Last Modified: Tue, 29 Mar 2022 17:26:40 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e026a7e4cc2b9efd9bf03aaabaab62ebe77e5a742bc4c29f4334212b6d9d2a5`  
		Last Modified: Tue, 29 Mar 2022 17:26:38 GMT  
		Size: 960.6 KB (960613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49465b4c6717933ae61b016e1329b4a872a6680e9ba12b999f78379dbbf6481`  
		Last Modified: Tue, 29 Mar 2022 17:27:06 GMT  
		Size: 108.3 MB (108324794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a258054a4458994b79a99613a9a28cf1f4cefd23277b78529824b759431ea0f`  
		Last Modified: Tue, 29 Mar 2022 17:26:59 GMT  
		Size: 5.3 MB (5324482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76f2868aaa9343cc3fa34a86924283389ae8c51a85effffaceab5669f44149b`  
		Last Modified: Tue, 29 Mar 2022 17:26:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f774547a4e5516dc78049766850def302e08785f61738696f4b2fd3a4a77ed`  
		Last Modified: Tue, 29 Mar 2022 17:26:58 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab14f515b10e3468c6aa853adb26510fd536d7317b72ab755a92e23a6eeb5ff`  
		Last Modified: Tue, 29 Mar 2022 17:26:58 GMT  
		Size: 5.0 KB (5017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ddff68e6377af62bd283f4e9f143d2b9d2b9ea3df07d68144e54d8e5136f5949
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129091224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b620a352032301f93661396eb1fca8a4107e72d45b1409b8c9bf0c7fae7f4a8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:12 GMT
ADD file:d0894581cf2fb7d7911ecb25bf0368675197db96d762977964ffc3a7ae8c774c in / 
# Tue, 29 Mar 2022 00:40:13 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 11:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 11:55:20 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Tue, 29 Mar 2022 11:55:21 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 29 Mar 2022 11:55:22 GMT
ENV GOSU_VER=1.12
# Tue, 29 Mar 2022 11:55:26 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Mar 2022 11:56:05 GMT
ENV INFLUXDB_VERSION=2.1.1
# Tue, 29 Mar 2022 11:56:14 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Tue, 29 Mar 2022 11:56:14 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Tue, 29 Mar 2022 11:56:19 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Tue, 29 Mar 2022 11:56:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 29 Mar 2022 11:56:21 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 29 Mar 2022 11:56:23 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 29 Mar 2022 11:56:24 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Tue, 29 Mar 2022 11:56:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 11:56:25 GMT
CMD ["influxd"]
# Tue, 29 Mar 2022 11:56:26 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 11:56:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 29 Mar 2022 11:56:28 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 29 Mar 2022 11:56:29 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 29 Mar 2022 11:56:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:810d54c7e01bab9975c1fb485c543715b76de7708166132520dfec0fc32c3754`  
		Last Modified: Tue, 29 Mar 2022 00:41:26 GMT  
		Size: 2.7 MB (2717494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d05fbec0985dd4e2437413ad065a5e9de75bd6c2b3d8ddf507f114b646ae286`  
		Last Modified: Tue, 29 Mar 2022 11:57:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1d1662bf96050f7b6919306a6d549c24ffdd1b8c572aeb04f46aaed1f1261b`  
		Last Modified: Tue, 29 Mar 2022 11:57:14 GMT  
		Size: 9.7 MB (9672483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0f2be565408f265515dccdc66af14c3289ea56a405f7ddc1377cb21ee637b7`  
		Last Modified: Tue, 29 Mar 2022 11:57:12 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e0a53cc77406effa83102261ce01a8855c9bd7c7ed944976b69bb337a8dda7`  
		Last Modified: Tue, 29 Mar 2022 11:57:10 GMT  
		Size: 896.1 KB (896076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81bc505e8165f74a9d27dd342d7d3d79f685491cb6e9c9abe729578c8149061`  
		Last Modified: Tue, 29 Mar 2022 11:57:43 GMT  
		Size: 110.9 MB (110891593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22645a3eccc37c9e1f2aed8d97dacd06be4b114efca585f300ea4ed68802df0`  
		Last Modified: Tue, 29 Mar 2022 11:57:35 GMT  
		Size: 4.9 MB (4906732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e37f4bf83c351e8926f204ee2d9f204cfea970ac8b5ab3e31f98d5659d5d0f`  
		Last Modified: Tue, 29 Mar 2022 11:57:34 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d4a874b49998b6c39fca72812e50c58c6e1d1c9538d5118d6e4e89dcf088bd`  
		Last Modified: Tue, 29 Mar 2022 11:57:34 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1d3f354f0bfd5fec69a97e80a505a7f3fa26c0952106699c8e0078bb699901`  
		Last Modified: Tue, 29 Mar 2022 11:57:34 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data`

```console
$ docker pull influxdb@sha256:be2d5a7bd5ff0644383defcce1f7769ae89363d5867ac5b2615ae2731dcb6c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:0790872efd83e02d8fdd2faf7a2ff410f9ff50a007b58c517d14c783d48130d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117786452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276cebfb7edd0645264657425ddb00bb2bcb80b7dce64169b9281067ebc0707c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:18 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 30 Mar 2022 23:05:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:25 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:25 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edcfcb7a5161abd03b61b6153c6f903029bcfb2d9efa4a6556918c51a064af1`  
		Last Modified: Wed, 30 Mar 2022 23:08:36 GMT  
		Size: 56.7 MB (56709163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97289aef350957936b3a19d68c846a790247f957e99f5d9f0e9c628bc74e2d0f`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1caefc2f0645fadbdce8da95cfbe3bdf21d1712e3d4b95577a26a55d97debc`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fc4496b0657c51da18c2c520e35381f811fe8d8a7eb3c3f4b15209a3b00900`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:c3940c85422166cb6f158b97538004d73d21ce81f43a839fdab8c39b310c792a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:962baad1407568923fe45b600affa45466137ff4ef33a9d78299b95414d2f038
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60799373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3eee20845f355d9c17fa9824fadcfcb89bd4ba85d232ee3e46e100a3ec0af8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:08 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Tue, 29 Mar 2022 17:22:16 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:22:17 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 29 Mar 2022 17:22:17 GMT
EXPOSE 8086
# Tue, 29 Mar 2022 17:22:17 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:22:17 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:22:17 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 29 Mar 2022 17:22:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:22:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07f289a640480e497bcb4cbf35f9903f519c0a4eca2e05512508a7725996c4d`  
		Last Modified: Tue, 29 Mar 2022 17:25:34 GMT  
		Size: 56.5 MB (56503709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ad694584956eac20bc9efecae61954abfa8ca0cf15116b2e5267f770f92e48`  
		Last Modified: Tue, 29 Mar 2022 17:25:27 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b163e6403d18c50a34a61fa4c5cbc219a7e6d50b23be842f8602b82f4ff642d9`  
		Last Modified: Tue, 29 Mar 2022 17:25:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b6760863cdb198fa9847fb23452a52a071d03107434a688207f9aab4c1a3c3`  
		Last Modified: Tue, 29 Mar 2022 17:25:27 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:2f6855f9556b71dbcae60e1065f4710559f14e1cd94c7c3ee9768b64c4e1e4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:6c3cc5ef911b8c16979f710651675456caf5688ee61775e9d7dd8aefa188dacf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182909101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c756b1d9ee5bf83999f7cbadd8b511e748b4e0d38095bc8421d56e7e24216c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:05:55 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:05:55 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:05:58 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:06:12 GMT
ENV INFLUXDB_VERSION=2.1.1
# Wed, 30 Mar 2022 23:06:22 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 30 Mar 2022 23:06:22 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Wed, 30 Mar 2022 23:06:26 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 30 Mar 2022 23:06:26 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:06:26 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:06:26 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:06:27 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:06:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:06:27 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:06:27 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:06:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:06:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210cc72c8f1796931ac2ce388819651f4b4cdb5bd99623547bae5660a73770e1`  
		Last Modified: Wed, 30 Mar 2022 23:09:35 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13436eca631d5b01be4a00ba60c559399662574e1abe8f93a9a0aa4fc3536f57`  
		Last Modified: Wed, 30 Mar 2022 23:09:33 GMT  
		Size: 961.0 KB (960962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793e652a43b509f8be74eb5064294d379224d59cf97316124fb499858445ef1`  
		Last Modified: Wed, 30 Mar 2022 23:10:07 GMT  
		Size: 108.3 MB (108324795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b482d9f0118895e8c347c58cbd312d1dfcca4330cf1ff83adc712580775e64f`  
		Last Modified: Wed, 30 Mar 2022 23:09:59 GMT  
		Size: 5.3 MB (5324479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2947646d0e18c37cc4fcc392b2cd653b762a7940fed46ee905128f6dbca79cea`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3282f6fa09cdf60983e54f1483883179f885470a104eeb790e88ab1be5d18d0`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ed2126a186f0abce1171df1dc7e227f047395d57632f220dfc30630bbcfd2f`  
		Last Modified: Wed, 30 Mar 2022 23:09:58 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b3905f1e9ffb41a7f9fd0ce44eed59301256f1186fd7549ea2f622141215815d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183414472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90d3dc0511263ca69dbd9901272be8f4e080ce9403cda81ae40ce68d78efbef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:21:43 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 30 Mar 2022 23:21:44 GMT
ENV GOSU_VER=1.12
# Wed, 30 Mar 2022 23:21:48 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 30 Mar 2022 23:22:18 GMT
ENV INFLUXDB_VERSION=2.1.1
# Wed, 30 Mar 2022 23:22:25 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 30 Mar 2022 23:22:25 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Wed, 30 Mar 2022 23:22:29 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 30 Mar 2022 23:22:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 30 Mar 2022 23:22:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 30 Mar 2022 23:22:32 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 30 Mar 2022 23:22:33 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:22:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:22:34 GMT
CMD ["influxd"]
# Wed, 30 Mar 2022 23:22:35 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:22:36 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 30 Mar 2022 23:22:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 30 Mar 2022 23:22:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 30 Mar 2022 23:22:39 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852f48a9439fa6ebf298c8036cafc7a4fed044921009c423f090fa5c2f7a799a`  
		Last Modified: Wed, 30 Mar 2022 23:23:55 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c67ea50143c728fffa089fbfcf7df1b1a2e800ab3350e2aed93291eaaaf1fa7`  
		Last Modified: Wed, 30 Mar 2022 23:23:54 GMT  
		Size: 896.3 KB (896337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6874725511156ff9e815819dffafee7879b8bab6820901484dab85ba06bf9b76`  
		Last Modified: Wed, 30 Mar 2022 23:24:26 GMT  
		Size: 110.9 MB (110891613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4fe266bd0bca43087df62a3f30c9fb7668277a6f5f8ca3b039aff3f0a02816`  
		Last Modified: Wed, 30 Mar 2022 23:24:18 GMT  
		Size: 4.9 MB (4906728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c13758147cee9ae50ab7e4622cd7b280b4931b06e268aee29bbc31d97b978fc`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea839f94b295d7eafff699c715006e4e6695743e971d7c314ccb624ea0c670e`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282331cef6cbe0a9aa18ba4dfc9d6e08a6888c6110f8b2f856e4e15e0c61fe1b`  
		Last Modified: Wed, 30 Mar 2022 23:24:17 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:4727e7c393e16502a487921e0fcae07eaaf9e00ecf3b22b37562e86d6867188b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c50786838735ef2c78c51e7238a4404520063b935751ce517157749b2904aa5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84493011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0e1d0ea12729ab4474843f41d7a88f5a1870ec065e3fe58185c6b0098c0ce1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:18 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 30 Mar 2022 23:05:32 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:32 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 30 Mar 2022 23:05:32 GMT
EXPOSE 8091
# Wed, 30 Mar 2022 23:05:32 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:33 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:33 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c487c418525e877d8128d62ac4dc164cba44ce112d1bc88171390368ce61ad53`  
		Last Modified: Wed, 30 Mar 2022 23:08:52 GMT  
		Size: 23.4 MB (23416930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720a75a54e3c5d1a6d4ca4261fc76d135e3e9c04b6804de3b56615706c8fdf17`  
		Last Modified: Wed, 30 Mar 2022 23:08:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feee196124cbe471a1e4ff40944ed9de1949b39f539001874ba0f125d28314d5`  
		Last Modified: Wed, 30 Mar 2022 23:08:49 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:2b31a82b424e3f0f93bc6b6d76569c55284d1d54a240d1495e5941f6fabc3a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:de1490581ec83ecc04551ed923bd4c9a9da5f2faa88c84ece23d8d5578b91407
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27587442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e859d256d7ddf403eb8cb6b19028bf170c200a756ce865dbf96421e5b5cbbe10`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 17:21:05 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 17:22:08 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Tue, 29 Mar 2022 17:22:27 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 17:22:27 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 29 Mar 2022 17:22:27 GMT
EXPOSE 8091
# Tue, 29 Mar 2022 17:22:27 GMT
VOLUME [/var/lib/influxdb]
# Tue, 29 Mar 2022 17:22:27 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 29 Mar 2022 17:22:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 17:22:27 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efb26cdde3530076f11310fff34e6e3ebfcff3c4300be8b7da35e0b8608e393`  
		Last Modified: Tue, 29 Mar 2022 17:24:14 GMT  
		Size: 1.5 MB (1475364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1724c466e7e91d37ac61a8791b771bb11953b76ba241a1b93fd755ca213ec3`  
		Last Modified: Tue, 29 Mar 2022 17:25:53 GMT  
		Size: 23.3 MB (23292976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1289b71d892126db0c08ceb7478ffcea1aafc961900dadb1570cf7935b356b1`  
		Last Modified: Tue, 29 Mar 2022 17:25:48 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edf276a80534e8819ddd932f9b6f428da7a8ab0cd040b1919e940975ede5688`  
		Last Modified: Tue, 29 Mar 2022 17:25:48 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
