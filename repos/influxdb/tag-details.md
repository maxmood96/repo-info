<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.7`](#influxdb17)
-	[`influxdb:1.7-alpine`](#influxdb17-alpine)
-	[`influxdb:1.7-data`](#influxdb17-data)
-	[`influxdb:1.7-data-alpine`](#influxdb17-data-alpine)
-	[`influxdb:1.7-meta`](#influxdb17-meta)
-	[`influxdb:1.7-meta-alpine`](#influxdb17-meta-alpine)
-	[`influxdb:1.7.10`](#influxdb1710)
-	[`influxdb:1.7.10-alpine`](#influxdb1710-alpine)
-	[`influxdb:1.7.10-data`](#influxdb1710-data)
-	[`influxdb:1.7.10-data-alpine`](#influxdb1710-data-alpine)
-	[`influxdb:1.7.10-meta`](#influxdb1710-meta)
-	[`influxdb:1.7.10-meta-alpine`](#influxdb1710-meta-alpine)
-	[`influxdb:1.8`](#influxdb18)
-	[`influxdb:1.8-alpine`](#influxdb18-alpine)
-	[`influxdb:1.8-data`](#influxdb18-data)
-	[`influxdb:1.8-data-alpine`](#influxdb18-data-alpine)
-	[`influxdb:1.8-meta`](#influxdb18-meta)
-	[`influxdb:1.8-meta-alpine`](#influxdb18-meta-alpine)
-	[`influxdb:1.8.3-data`](#influxdb183-data)
-	[`influxdb:1.8.3-data-alpine`](#influxdb183-data-alpine)
-	[`influxdb:1.8.3-meta`](#influxdb183-meta)
-	[`influxdb:1.8.3-meta-alpine`](#influxdb183-meta-alpine)
-	[`influxdb:1.8.4`](#influxdb184)
-	[`influxdb:1.8.4-alpine`](#influxdb184-alpine)
-	[`influxdb:2.0`](#influxdb20)
-	[`influxdb:2.0-alpine`](#influxdb20-alpine)
-	[`influxdb:2.0.4`](#influxdb204)
-	[`influxdb:2.0.4-alpine`](#influxdb204-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:data`](#influxdbdata)
-	[`influxdb:data-alpine`](#influxdbdata-alpine)
-	[`influxdb:latest`](#influxdblatest)
-	[`influxdb:meta`](#influxdbmeta)
-	[`influxdb:meta-alpine`](#influxdbmeta-alpine)

## `influxdb:1.7`

```console
$ docker pull influxdb@sha256:2237aebdede06a162b2a475848aae58b36a3c5616d2895800134d7d15375dd63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7` - linux; amd64

```console
$ docker pull influxdb@sha256:d0bab180fd96f4fdb6540ad7643093d8caf21faa7f530b3e814f7fae0434708a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125092813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5616230bf2a9013175f05c816c89d00097b2cf7eb527d3b3fd9c90d70acf2d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:55:55 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 10 Feb 2021 04:56:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Feb 2021 04:56:03 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:56:03 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:56:03 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:03 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:56:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:04 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f0c925438df84d4762925974fa9b347adb5dce48715acd5b548b9fec6ccff4`  
		Last Modified: Wed, 10 Feb 2021 04:58:08 GMT  
		Size: 64.1 MB (64097822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3495c03e1256c3827908e7c1e30fe4076e2286b9dc1d88b8b5d5bd90d804463b`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0281ac5a9a9620a1c9b83ccaa9823614869d84d631aafcc5fa1e86e6734d426`  
		Last Modified: Wed, 10 Feb 2021 04:57:59 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0891697c6072b912191fa07c825ea350448ac9d6fbf7c60aae7134cef65104c`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:e72ebe3ef14212c7b49a759e52306b341b3a8142e6a21ce583dc966ee92ca7eb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116597301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e61860be06449fa113b1ba45909cbd5ad80d9be82daa7c2f54a7b576156bad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:05:10 GMT
ADD file:36669d020402a086f914d75419118f4daa1cbeeed645c1a77fe62cac0e804b59 in / 
# Fri, 12 Mar 2021 02:05:15 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:40:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 20:09:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 20:09:29 GMT
ENV INFLUXDB_VERSION=1.7.10
# Fri, 12 Mar 2021 20:09:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Fri, 12 Mar 2021 20:09:42 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 12 Mar 2021 20:09:43 GMT
EXPOSE 8086
# Fri, 12 Mar 2021 20:09:43 GMT
VOLUME [/var/lib/influxdb]
# Fri, 12 Mar 2021 20:09:44 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 12 Mar 2021 20:09:45 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 12 Mar 2021 20:09:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 20:09:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:87fcebbbbffa651ca8743935928db6e5acd0bef83a84d1dcc331b6a5dd2dd3a5`  
		Last Modified: Fri, 12 Mar 2021 02:14:09 GMT  
		Size: 42.1 MB (42120188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23db22a6953922b4d37e712f7abfd57e9d0b445d547049f3ae1aff068cd82b05`  
		Last Modified: Fri, 12 Mar 2021 03:50:06 GMT  
		Size: 9.9 MB (9915047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd48c000dbbac1ab4f6cc2b3bbdbd339981893df53383b9f000686f4a1c445b9`  
		Last Modified: Fri, 12 Mar 2021 03:50:04 GMT  
		Size: 3.9 MB (3921108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3176cabfa396c35e5640014ce46bfaa13e9007e5a47f2608a70aab36eb8e`  
		Last Modified: Fri, 12 Mar 2021 20:10:26 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84035ace2e3da053310110cb3181938ac094a0d52935d0c0a62d3d124a813a5`  
		Last Modified: Fri, 12 Mar 2021 20:10:42 GMT  
		Size: 60.6 MB (60636388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa09ea45d4e8cae42a5677ef9312fd14f7095777a92c307a10627e0b048efdc`  
		Last Modified: Fri, 12 Mar 2021 20:10:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b1f453a1cc0eebffbd9fa9260c53189e41a5adb512cbf205d7953ce204c4d3`  
		Last Modified: Fri, 12 Mar 2021 20:10:26 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7042a2b636d6aeff4f7f97ff4b93357ab63f8c1f4243421dfc27e21cd20c429`  
		Last Modified: Fri, 12 Mar 2021 20:10:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:afa19a02206bed160d8ab3a888c07292b42deca2704970505df293f163790a53
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117591382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1f484b197eaa256b21d66461ccb056a820d1a05c1c3908a9d36a193ed7caa7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 22:02:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 22:02:21 GMT
ENV INFLUXDB_VERSION=1.7.10
# Fri, 12 Mar 2021 22:02:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Fri, 12 Mar 2021 22:02:49 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 12 Mar 2021 22:02:51 GMT
EXPOSE 8086
# Fri, 12 Mar 2021 22:02:53 GMT
VOLUME [/var/lib/influxdb]
# Fri, 12 Mar 2021 22:02:54 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 12 Mar 2021 22:02:56 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 12 Mar 2021 22:02:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 22:02:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680b71a7b1637cdab80389ba3468f3abae4d50d7ebe782252d744b21c7ec7d99`  
		Last Modified: Fri, 12 Mar 2021 22:04:46 GMT  
		Size: 2.9 KB (2859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4790b1048e8db5a736643ab714c77a701a3c07206b0cc8687bbf9ac0aafd2f60`  
		Last Modified: Fri, 12 Mar 2021 22:05:03 GMT  
		Size: 60.1 MB (60128621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b00298a38effc46f9de8eb3bea02be8e7c963351626203ce623a6efb185df09`  
		Last Modified: Fri, 12 Mar 2021 22:04:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55726c0e53acd1d10fec203d7d1e4491316036caf74f8024abb04c262e772f6b`  
		Last Modified: Fri, 12 Mar 2021 22:04:46 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293afe590684a128fd6f0c169322550438a0fd704ecab6271a4a69f7a40c1181`  
		Last Modified: Fri, 12 Mar 2021 22:04:46 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-alpine`

```console
$ docker pull influxdb@sha256:910fe461d38ffc4ce8d3b58d251ef57238fa357d2e7b4e630776075bd1860658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e7cebbd98c3e01bfa7235e1fa4062d61afde9b436a1473e841cf03b38e4d6259
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68073050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9902deb5e5d6501a2ce2a4fdbaa97a1c92698ca1be78a67e31f036b4802cf444`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:21:16 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:21:16 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 24 Feb 2021 20:21:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:21:25 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 24 Feb 2021 20:21:25 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:21:25 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Feb 2021 20:21:26 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:21:26 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Feb 2021 20:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:21:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9587daa31955a7d1e8a3f596d61db5ef65bb6338a51db3fba1e5b13a41ce47d`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.4 MB (1430585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b737fe8f89a20d659a5974d6fd2bea9256f6bc7c0e4b83f73b68fe645bd444`  
		Last Modified: Wed, 24 Feb 2021 20:24:19 GMT  
		Size: 63.8 MB (63841107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34844d7466fefaef69070c9de3c4aaa469519b2f43b2d47acd056fda775e647`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc74754a5950d5c197810f90df9e65185df2bc30756e578a1358fa2701b79b1`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2481502c58271f088abe18e7de8045f9f37981de2e0b0b89a6cc0411d869f03f`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data`

```console
$ docker pull influxdb@sha256:4af280a9420a33eccb8fbcc5ebf6c073759b5fe9309f1fada837860bc32a7872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a58844cf163a4c4f289134a50d4fbf055806d77d8b101962c15904fcef08060e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148908169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb96bda809ce7fad53c4783719ee9d16e4f4055f19a59e0aad401167ccbd57f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:56:12 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 10 Feb 2021 04:56:22 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:56:22 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:56:22 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:56:23 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:23 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:23 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:56:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7726fa0aee1911fd933abaf235a87e9ffe1b2634ca67cd6816ed91df579ad587`  
		Last Modified: Wed, 10 Feb 2021 04:58:27 GMT  
		Size: 87.9 MB (87913121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4339ee43e029207b966b143a846da54c5c13ff540f26a49a6b33fde7a7f2a`  
		Last Modified: Wed, 10 Feb 2021 04:58:14 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e1aaf6a49d5b0be78daa7e32333521838a3454702e6bbbfacff86075bd911e`  
		Last Modified: Wed, 10 Feb 2021 04:58:14 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3429ae36607fca2ac5eccda45c507332cf32273f7dd66839ef20b3833adf50ed`  
		Last Modified: Wed, 10 Feb 2021 04:58:14 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data-alpine`

```console
$ docker pull influxdb@sha256:c11a8d9e5486e473be15539f0b4e1e838b417e1d9ec98aaf68e2c76dfff66e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e0052bb0a30daa6fafd1284f58c5b314bbbd46fc71bc3a7ae68160fd37a0b99f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91835615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2548917c38313670d067bb830d3c2e74827084a0b1f77411a43281d6014e23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:21:16 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:21:36 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 24 Feb 2021 20:21:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:21:48 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 24 Feb 2021 20:21:48 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:21:48 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Feb 2021 20:21:48 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:21:49 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Feb 2021 20:21:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:21:49 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9587daa31955a7d1e8a3f596d61db5ef65bb6338a51db3fba1e5b13a41ce47d`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.4 MB (1430585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b674b0db6226660e499a4ee0f904641f0ef9f40003b8c9cae9e4e0f31fa0a8`  
		Last Modified: Wed, 24 Feb 2021 20:24:42 GMT  
		Size: 87.6 MB (87603613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7156423c4742f09db354630e8f0fdd44d0adf904d689afd3fbb23f6ad14c4e`  
		Last Modified: Wed, 24 Feb 2021 20:24:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580b1bc51556d4d6572514a1ad0a73ac207f5076d64c1f1bd9c1bb2d2470f0e`  
		Last Modified: Wed, 24 Feb 2021 20:24:29 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805327c2b8def0883ffb1290fd7b08108db4e1e485b131704a28467a3220ba0e`  
		Last Modified: Wed, 24 Feb 2021 20:24:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta`

```console
$ docker pull influxdb@sha256:bd2ade536a4d86c0fbb698e8bd82336be74f991d3aa623a1e83959fbff6df71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:0ef3b034d2c4d595316a40f463e392c906705fed078984b245b3aa6dcdb41f40
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84127444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec9dbe621d18f119a21ce994e923cecfd0608928b8cb8da95cdd9d639fdec97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:56:12 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 10 Feb 2021 04:56:35 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:56:36 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Feb 2021 04:56:36 GMT
EXPOSE 8091
# Wed, 10 Feb 2021 04:56:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:36 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:37 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37485044ae75fc05a5c133877602f1e563f02702daa88e69dbaf6964262eafa7`  
		Last Modified: Wed, 10 Feb 2021 04:58:36 GMT  
		Size: 23.1 MB (23133606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee04e9fe70d35e8397f670bec3673cf5beb018e5952b9b65d9231d4b708462fa`  
		Last Modified: Wed, 10 Feb 2021 04:58:32 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3984387e1cc482d4c47e13155cc6cced0ecd5d4c215de9081209b028d257259a`  
		Last Modified: Wed, 10 Feb 2021 04:58:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta-alpine`

```console
$ docker pull influxdb@sha256:2ec9073c1839a53ff3800f0755033932155ef3029dee7731b977db95d0db7809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5a175a321491f3b1c373371d5e559b6927e5ff1c5ad18c0263b4dab9b0f2ea48
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27233429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3207cdcafa6f723ac556403026e44a556235a9debfad2ea620eef98c7ddf44ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:21:16 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:21:36 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 24 Feb 2021 20:22:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:22:03 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 24 Feb 2021 20:22:03 GMT
EXPOSE 8091
# Wed, 24 Feb 2021 20:22:03 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Feb 2021 20:22:03 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:22:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:22:04 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9587daa31955a7d1e8a3f596d61db5ef65bb6338a51db3fba1e5b13a41ce47d`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.4 MB (1430585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1503ebd5b9f3defed1ea4f6999464d888e39b55b9992f5e787863923a02f617a`  
		Last Modified: Wed, 24 Feb 2021 20:24:50 GMT  
		Size: 23.0 MB (23002628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27eec53d6a49e7ed3f980bc2fc84496eeef111e1acb3f05b8bcf1219d04d38`  
		Last Modified: Wed, 24 Feb 2021 20:24:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d1081df1112a2cb60caac77151ac569f4ef70eb2dc3f2f12bb860f83cfa26a`  
		Last Modified: Wed, 24 Feb 2021 20:24:46 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10`

```console
$ docker pull influxdb@sha256:2237aebdede06a162b2a475848aae58b36a3c5616d2895800134d7d15375dd63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7.10` - linux; amd64

```console
$ docker pull influxdb@sha256:d0bab180fd96f4fdb6540ad7643093d8caf21faa7f530b3e814f7fae0434708a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125092813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5616230bf2a9013175f05c816c89d00097b2cf7eb527d3b3fd9c90d70acf2d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:55:55 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 10 Feb 2021 04:56:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Feb 2021 04:56:03 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:56:03 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:56:03 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:03 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:03 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:56:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:04 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f0c925438df84d4762925974fa9b347adb5dce48715acd5b548b9fec6ccff4`  
		Last Modified: Wed, 10 Feb 2021 04:58:08 GMT  
		Size: 64.1 MB (64097822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3495c03e1256c3827908e7c1e30fe4076e2286b9dc1d88b8b5d5bd90d804463b`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0281ac5a9a9620a1c9b83ccaa9823614869d84d631aafcc5fa1e86e6734d426`  
		Last Modified: Wed, 10 Feb 2021 04:57:59 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0891697c6072b912191fa07c825ea350448ac9d6fbf7c60aae7134cef65104c`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:e72ebe3ef14212c7b49a759e52306b341b3a8142e6a21ce583dc966ee92ca7eb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116597301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e61860be06449fa113b1ba45909cbd5ad80d9be82daa7c2f54a7b576156bad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:05:10 GMT
ADD file:36669d020402a086f914d75419118f4daa1cbeeed645c1a77fe62cac0e804b59 in / 
# Fri, 12 Mar 2021 02:05:15 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:40:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 20:09:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 20:09:29 GMT
ENV INFLUXDB_VERSION=1.7.10
# Fri, 12 Mar 2021 20:09:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Fri, 12 Mar 2021 20:09:42 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 12 Mar 2021 20:09:43 GMT
EXPOSE 8086
# Fri, 12 Mar 2021 20:09:43 GMT
VOLUME [/var/lib/influxdb]
# Fri, 12 Mar 2021 20:09:44 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 12 Mar 2021 20:09:45 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 12 Mar 2021 20:09:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 20:09:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:87fcebbbbffa651ca8743935928db6e5acd0bef83a84d1dcc331b6a5dd2dd3a5`  
		Last Modified: Fri, 12 Mar 2021 02:14:09 GMT  
		Size: 42.1 MB (42120188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23db22a6953922b4d37e712f7abfd57e9d0b445d547049f3ae1aff068cd82b05`  
		Last Modified: Fri, 12 Mar 2021 03:50:06 GMT  
		Size: 9.9 MB (9915047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd48c000dbbac1ab4f6cc2b3bbdbd339981893df53383b9f000686f4a1c445b9`  
		Last Modified: Fri, 12 Mar 2021 03:50:04 GMT  
		Size: 3.9 MB (3921108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3176cabfa396c35e5640014ce46bfaa13e9007e5a47f2608a70aab36eb8e`  
		Last Modified: Fri, 12 Mar 2021 20:10:26 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84035ace2e3da053310110cb3181938ac094a0d52935d0c0a62d3d124a813a5`  
		Last Modified: Fri, 12 Mar 2021 20:10:42 GMT  
		Size: 60.6 MB (60636388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa09ea45d4e8cae42a5677ef9312fd14f7095777a92c307a10627e0b048efdc`  
		Last Modified: Fri, 12 Mar 2021 20:10:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b1f453a1cc0eebffbd9fa9260c53189e41a5adb512cbf205d7953ce204c4d3`  
		Last Modified: Fri, 12 Mar 2021 20:10:26 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7042a2b636d6aeff4f7f97ff4b93357ab63f8c1f4243421dfc27e21cd20c429`  
		Last Modified: Fri, 12 Mar 2021 20:10:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:afa19a02206bed160d8ab3a888c07292b42deca2704970505df293f163790a53
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117591382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1f484b197eaa256b21d66461ccb056a820d1a05c1c3908a9d36a193ed7caa7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 22:02:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 22:02:21 GMT
ENV INFLUXDB_VERSION=1.7.10
# Fri, 12 Mar 2021 22:02:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Fri, 12 Mar 2021 22:02:49 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 12 Mar 2021 22:02:51 GMT
EXPOSE 8086
# Fri, 12 Mar 2021 22:02:53 GMT
VOLUME [/var/lib/influxdb]
# Fri, 12 Mar 2021 22:02:54 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 12 Mar 2021 22:02:56 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 12 Mar 2021 22:02:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 22:02:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680b71a7b1637cdab80389ba3468f3abae4d50d7ebe782252d744b21c7ec7d99`  
		Last Modified: Fri, 12 Mar 2021 22:04:46 GMT  
		Size: 2.9 KB (2859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4790b1048e8db5a736643ab714c77a701a3c07206b0cc8687bbf9ac0aafd2f60`  
		Last Modified: Fri, 12 Mar 2021 22:05:03 GMT  
		Size: 60.1 MB (60128621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b00298a38effc46f9de8eb3bea02be8e7c963351626203ce623a6efb185df09`  
		Last Modified: Fri, 12 Mar 2021 22:04:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55726c0e53acd1d10fec203d7d1e4491316036caf74f8024abb04c262e772f6b`  
		Last Modified: Fri, 12 Mar 2021 22:04:46 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293afe590684a128fd6f0c169322550438a0fd704ecab6271a4a69f7a40c1181`  
		Last Modified: Fri, 12 Mar 2021 22:04:46 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-alpine`

```console
$ docker pull influxdb@sha256:910fe461d38ffc4ce8d3b58d251ef57238fa357d2e7b4e630776075bd1860658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e7cebbd98c3e01bfa7235e1fa4062d61afde9b436a1473e841cf03b38e4d6259
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68073050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9902deb5e5d6501a2ce2a4fdbaa97a1c92698ca1be78a67e31f036b4802cf444`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:21:16 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:21:16 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 24 Feb 2021 20:21:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:21:25 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 24 Feb 2021 20:21:25 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:21:25 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Feb 2021 20:21:26 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:21:26 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Feb 2021 20:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:21:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9587daa31955a7d1e8a3f596d61db5ef65bb6338a51db3fba1e5b13a41ce47d`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.4 MB (1430585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b737fe8f89a20d659a5974d6fd2bea9256f6bc7c0e4b83f73b68fe645bd444`  
		Last Modified: Wed, 24 Feb 2021 20:24:19 GMT  
		Size: 63.8 MB (63841107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34844d7466fefaef69070c9de3c4aaa469519b2f43b2d47acd056fda775e647`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc74754a5950d5c197810f90df9e65185df2bc30756e578a1358fa2701b79b1`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2481502c58271f088abe18e7de8045f9f37981de2e0b0b89a6cc0411d869f03f`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-data`

```console
$ docker pull influxdb@sha256:4af280a9420a33eccb8fbcc5ebf6c073759b5fe9309f1fada837860bc32a7872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:a58844cf163a4c4f289134a50d4fbf055806d77d8b101962c15904fcef08060e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148908169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb96bda809ce7fad53c4783719ee9d16e4f4055f19a59e0aad401167ccbd57f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:56:12 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 10 Feb 2021 04:56:22 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:56:22 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:56:22 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:56:23 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:23 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:23 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:56:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7726fa0aee1911fd933abaf235a87e9ffe1b2634ca67cd6816ed91df579ad587`  
		Last Modified: Wed, 10 Feb 2021 04:58:27 GMT  
		Size: 87.9 MB (87913121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4339ee43e029207b966b143a846da54c5c13ff540f26a49a6b33fde7a7f2a`  
		Last Modified: Wed, 10 Feb 2021 04:58:14 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e1aaf6a49d5b0be78daa7e32333521838a3454702e6bbbfacff86075bd911e`  
		Last Modified: Wed, 10 Feb 2021 04:58:14 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3429ae36607fca2ac5eccda45c507332cf32273f7dd66839ef20b3833adf50ed`  
		Last Modified: Wed, 10 Feb 2021 04:58:14 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-data-alpine`

```console
$ docker pull influxdb@sha256:c11a8d9e5486e473be15539f0b4e1e838b417e1d9ec98aaf68e2c76dfff66e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e0052bb0a30daa6fafd1284f58c5b314bbbd46fc71bc3a7ae68160fd37a0b99f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91835615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2548917c38313670d067bb830d3c2e74827084a0b1f77411a43281d6014e23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:21:16 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:21:36 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 24 Feb 2021 20:21:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:21:48 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 24 Feb 2021 20:21:48 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:21:48 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Feb 2021 20:21:48 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:21:49 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Feb 2021 20:21:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:21:49 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9587daa31955a7d1e8a3f596d61db5ef65bb6338a51db3fba1e5b13a41ce47d`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.4 MB (1430585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b674b0db6226660e499a4ee0f904641f0ef9f40003b8c9cae9e4e0f31fa0a8`  
		Last Modified: Wed, 24 Feb 2021 20:24:42 GMT  
		Size: 87.6 MB (87603613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7156423c4742f09db354630e8f0fdd44d0adf904d689afd3fbb23f6ad14c4e`  
		Last Modified: Wed, 24 Feb 2021 20:24:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580b1bc51556d4d6572514a1ad0a73ac207f5076d64c1f1bd9c1bb2d2470f0e`  
		Last Modified: Wed, 24 Feb 2021 20:24:29 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805327c2b8def0883ffb1290fd7b08108db4e1e485b131704a28467a3220ba0e`  
		Last Modified: Wed, 24 Feb 2021 20:24:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-meta`

```console
$ docker pull influxdb@sha256:bd2ade536a4d86c0fbb698e8bd82336be74f991d3aa623a1e83959fbff6df71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:0ef3b034d2c4d595316a40f463e392c906705fed078984b245b3aa6dcdb41f40
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84127444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec9dbe621d18f119a21ce994e923cecfd0608928b8cb8da95cdd9d639fdec97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:56:12 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 10 Feb 2021 04:56:35 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:56:36 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Feb 2021 04:56:36 GMT
EXPOSE 8091
# Wed, 10 Feb 2021 04:56:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:36 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:37 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37485044ae75fc05a5c133877602f1e563f02702daa88e69dbaf6964262eafa7`  
		Last Modified: Wed, 10 Feb 2021 04:58:36 GMT  
		Size: 23.1 MB (23133606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee04e9fe70d35e8397f670bec3673cf5beb018e5952b9b65d9231d4b708462fa`  
		Last Modified: Wed, 10 Feb 2021 04:58:32 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3984387e1cc482d4c47e13155cc6cced0ecd5d4c215de9081209b028d257259a`  
		Last Modified: Wed, 10 Feb 2021 04:58:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-meta-alpine`

```console
$ docker pull influxdb@sha256:2ec9073c1839a53ff3800f0755033932155ef3029dee7731b977db95d0db7809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5a175a321491f3b1c373371d5e559b6927e5ff1c5ad18c0263b4dab9b0f2ea48
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27233429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3207cdcafa6f723ac556403026e44a556235a9debfad2ea620eef98c7ddf44ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:21:16 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:21:36 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 24 Feb 2021 20:22:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:22:03 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 24 Feb 2021 20:22:03 GMT
EXPOSE 8091
# Wed, 24 Feb 2021 20:22:03 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Feb 2021 20:22:03 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:22:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:22:04 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9587daa31955a7d1e8a3f596d61db5ef65bb6338a51db3fba1e5b13a41ce47d`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.4 MB (1430585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1503ebd5b9f3defed1ea4f6999464d888e39b55b9992f5e787863923a02f617a`  
		Last Modified: Wed, 24 Feb 2021 20:24:50 GMT  
		Size: 23.0 MB (23002628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27eec53d6a49e7ed3f980bc2fc84496eeef111e1acb3f05b8bcf1219d04d38`  
		Last Modified: Wed, 24 Feb 2021 20:24:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d1081df1112a2cb60caac77151ac569f4ef70eb2dc3f2f12bb860f83cfa26a`  
		Last Modified: Wed, 24 Feb 2021 20:24:46 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:6417d60baa5a7d45ef78d39871362d6c2d4e38ba5055f3e3f36b07b9fad5720f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:7539edbf76df0498f730904827f859aa4c67e1386cb72601019d72ec3e12ed0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125961499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7870fcea362222d648815a18c6d949e3faae225b97b8c0ee7cc27b74e9d8c45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:56:44 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 10 Feb 2021 04:56:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:56:52 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:56:52 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:53 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0907122426ac6b2c48c0e3da39e10da254ba8f0e10be1600731b210881c4ef`  
		Last Modified: Wed, 10 Feb 2021 04:58:50 GMT  
		Size: 65.0 MB (64966512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d3d7e535c1e62ce9dfa85b05ccb228f0cbf722440cb8958e74580f3de94dd3`  
		Last Modified: Wed, 10 Feb 2021 04:58:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45b611f60bfbba58da3ec97f086ba4c4dfeb487aef823873770166635986f00`  
		Last Modified: Wed, 10 Feb 2021 04:58:40 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7c9bc15cec46afb70a351b3614181ae2cab6e938d478f34bfbfe2cdda2dcd1`  
		Last Modified: Wed, 10 Feb 2021 04:58:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:0e871df7efa1bcdadef1bf9caa16fa62e7df6b14a36bbc8def8f5b41413e0598
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117020861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e988ce200cc5422b31c1b1e2f2712b921c2fb9392450ca3ead6297738bfcfb77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:05:10 GMT
ADD file:36669d020402a086f914d75419118f4daa1cbeeed645c1a77fe62cac0e804b59 in / 
# Fri, 12 Mar 2021 02:05:15 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:40:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 20:09:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 20:09:56 GMT
ENV INFLUXDB_VERSION=1.8.4
# Fri, 12 Mar 2021 20:10:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Fri, 12 Mar 2021 20:10:08 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 12 Mar 2021 20:10:08 GMT
EXPOSE 8086
# Fri, 12 Mar 2021 20:10:09 GMT
VOLUME [/var/lib/influxdb]
# Fri, 12 Mar 2021 20:10:10 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 12 Mar 2021 20:10:11 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 12 Mar 2021 20:10:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 20:10:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:87fcebbbbffa651ca8743935928db6e5acd0bef83a84d1dcc331b6a5dd2dd3a5`  
		Last Modified: Fri, 12 Mar 2021 02:14:09 GMT  
		Size: 42.1 MB (42120188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23db22a6953922b4d37e712f7abfd57e9d0b445d547049f3ae1aff068cd82b05`  
		Last Modified: Fri, 12 Mar 2021 03:50:06 GMT  
		Size: 9.9 MB (9915047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd48c000dbbac1ab4f6cc2b3bbdbd339981893df53383b9f000686f4a1c445b9`  
		Last Modified: Fri, 12 Mar 2021 03:50:04 GMT  
		Size: 3.9 MB (3921108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3176cabfa396c35e5640014ce46bfaa13e9007e5a47f2608a70aab36eb8e`  
		Last Modified: Fri, 12 Mar 2021 20:10:26 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb167310f3a548875e714ddde45998aea4499fce5033d716b5b04ab2cb6b1262`  
		Last Modified: Fri, 12 Mar 2021 20:11:07 GMT  
		Size: 61.1 MB (61059948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608915d3f8617c096894097dd31bda1103758728655cd17f7f0e70f6ef3f6c17`  
		Last Modified: Fri, 12 Mar 2021 20:10:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb6305fa7fdc9e5bc29b757b6959cab3fe33728efcdb43559ecc1bcd08ccf1d`  
		Last Modified: Fri, 12 Mar 2021 20:10:50 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653e39cfb10ae0305d8b9b9faa74a81d47ef2d743ff10757c7f3a66d3f4111c7`  
		Last Modified: Fri, 12 Mar 2021 20:10:50 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c19174cb29b46857b8f18777fc580d9c53779c90cef02e1e096e77803358c610
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118091914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb7c92e03b675b3aac5292a1cc2ff645d60a3ae5fc2953e63c173ba6a4415b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 22:02:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 22:03:12 GMT
ENV INFLUXDB_VERSION=1.8.4
# Fri, 12 Mar 2021 22:03:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Fri, 12 Mar 2021 22:03:25 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 12 Mar 2021 22:03:27 GMT
EXPOSE 8086
# Fri, 12 Mar 2021 22:03:28 GMT
VOLUME [/var/lib/influxdb]
# Fri, 12 Mar 2021 22:03:29 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 12 Mar 2021 22:03:30 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 12 Mar 2021 22:03:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 22:03:32 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680b71a7b1637cdab80389ba3468f3abae4d50d7ebe782252d744b21c7ec7d99`  
		Last Modified: Fri, 12 Mar 2021 22:04:46 GMT  
		Size: 2.9 KB (2859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca129c3a3f09bd2ccb403c9b0bb85a151b6c3a67958703d3e6ff28ce0ca611b`  
		Last Modified: Fri, 12 Mar 2021 22:05:27 GMT  
		Size: 60.6 MB (60629153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66af461b4ff441bff957b3857ba63125defef8afc5c017a07cd9c51ea93818f`  
		Last Modified: Fri, 12 Mar 2021 22:05:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04775a23b021a4c8c9574172b4be5ea4f17fd3d88110a24c9427c7aa83b6451`  
		Last Modified: Fri, 12 Mar 2021 22:05:14 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f691964b980cdeaddf521dee8a227dc0509f6eca0be542aa812081a3158963c`  
		Last Modified: Fri, 12 Mar 2021 22:05:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-alpine`

```console
$ docker pull influxdb@sha256:86a36871313ba3cd0f5f26f8544f60e38b941108b2c612f7772c1033aa67cf60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e116772bd838098506a6f8ca57b455dec36fc9707873772498bad5f4d4747797
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68938617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eae8355b824a04e3ef940b941ae02ff3213e00ff813647deb24502ead2504e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:21:16 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:22:12 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 24 Feb 2021 20:22:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:22:22 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 24 Feb 2021 20:22:22 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:22:23 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Feb 2021 20:22:23 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:22:23 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Feb 2021 20:22:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:22:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9587daa31955a7d1e8a3f596d61db5ef65bb6338a51db3fba1e5b13a41ce47d`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.4 MB (1430585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67573dc4c2905652fbf53bd085e37640f8ad5fa6ed55827c3320ec9cbc983c2e`  
		Last Modified: Wed, 24 Feb 2021 20:25:07 GMT  
		Size: 64.7 MB (64706672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7559d31e6811b2d616d086a16a9a98abe07afecabf63e492e9a1b57a515a197`  
		Last Modified: Wed, 24 Feb 2021 20:24:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a870449cb171fe01938a088101acac4d541fbc12a9b88c57f35a6735ca5cbc8`  
		Last Modified: Wed, 24 Feb 2021 20:24:57 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b16f6af06b8a0e84952ae3798b80dd1643d9ff368deba19676c8b85a4bf6919`  
		Last Modified: Wed, 24 Feb 2021 20:24:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data`

```console
$ docker pull influxdb@sha256:67876cecbc722648d5eaf17c64854ae57beafca233a55416e95fc212de64bd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:9ad29edf6629eeeed7540d003ace92750e12e733055524dc08bc50c682eb8dec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126791523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1586215b740555a75748269f512871688d91312d26491ad08a114601e96719b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:57:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 10 Feb 2021 04:57:10 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:57:10 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:57:10 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:57:10 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:57:11 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:57:11 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:57:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:57:11 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d29e7e8838f6b925c171a67948b5f3bf44fca76a2428583987f3a7474f9e50`  
		Last Modified: Wed, 10 Feb 2021 04:59:10 GMT  
		Size: 65.8 MB (65796478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb80241906ed39ac62840cac80202f837585b84e0224d24571b11c957148879`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d44b9df77d08197aca251c63136878d862be3c48adb4878bace9022c7761a3f`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d904c7edfc7e2abba83d7274f2c25ff792d2688362e3f290b40a35b8f6da`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data-alpine`

```console
$ docker pull influxdb@sha256:1cbf0fd3ca714ebb68d5b889753a3b9f10512cf81a87e7c79c2dc17dab74dfba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f1b67fd4756d1480e361b79ba03dd6a9d777cdefbb2142f041e38c947171bb00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69772703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae14395ed136bd664421fcbfce9681436c1325e66063e1937ae157e9c38cd3ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:21:16 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:22:32 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 24 Feb 2021 20:22:40 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:22:41 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 24 Feb 2021 20:22:41 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:22:41 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Feb 2021 20:22:41 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:22:41 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Feb 2021 20:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:22:42 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9587daa31955a7d1e8a3f596d61db5ef65bb6338a51db3fba1e5b13a41ce47d`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.4 MB (1430585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a215dce6b858821299be01bfcfdad396b1dfaa07b606378d73ad1cbb825460a`  
		Last Modified: Wed, 24 Feb 2021 20:25:28 GMT  
		Size: 65.5 MB (65540698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ec32d8f5562b2cb4c60c59728674cd0923f7bffdeb01b519b9d6f93c3a4077`  
		Last Modified: Wed, 24 Feb 2021 20:25:16 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5782b1dbc21eedfbe9cb042069cdc8517e0d9ce4d46ed7035255ce9bfd2a73`  
		Last Modified: Wed, 24 Feb 2021 20:25:16 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b09b9d2ad4c407fdfacfe363c7285cc8603df8eb96f1e27de544fe1321162ec`  
		Last Modified: Wed, 24 Feb 2021 20:25:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta`

```console
$ docker pull influxdb@sha256:83e2e77f7ef83ceaa7549f44058d12f255301a99fe7ba6cc1a6f4d8a9fe0cb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ffe8c67e7d6a188fe1378ca1541b43740e07f77497f65aacd47103897defe8ae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83859997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d706e62f1b535daeefd18b8bde7816e8310504c1c995ebc1701323883d94d74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:57:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 10 Feb 2021 04:57:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:57:24 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Feb 2021 04:57:24 GMT
EXPOSE 8091
# Wed, 10 Feb 2021 04:57:24 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:57:24 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:57:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:57:25 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ba6effd1841113e069182d033c17f3bdbbd57c3b3e9347abdc2bdecdde2ef`  
		Last Modified: Wed, 10 Feb 2021 04:59:23 GMT  
		Size: 22.9 MB (22866156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b75a883c5a79201ac582bb3980ed32e7f034f2f6ae3ec49667a25f4582463bf`  
		Last Modified: Wed, 10 Feb 2021 04:59:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ebe920089e36547964e057f165cf7102ff2925b478a707d02b94ebd670efe2`  
		Last Modified: Wed, 10 Feb 2021 04:59:17 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta-alpine`

```console
$ docker pull influxdb@sha256:8b4400145dd68d888c52412fe7a515807e73f0f2d4e2729797f40ccecdef0a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4d514f93b2481f610cf691acd8eb2e785724ac8bb5d95584a3e8d035769182b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26966186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30d5df01f013bbc9077d099080c9f7ebb77402f65ba3ea3599eb45fda601f52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:21:16 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:22:32 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 24 Feb 2021 20:22:54 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:22:54 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 24 Feb 2021 20:22:54 GMT
EXPOSE 8091
# Wed, 24 Feb 2021 20:22:55 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Feb 2021 20:22:55 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:22:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:22:55 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9587daa31955a7d1e8a3f596d61db5ef65bb6338a51db3fba1e5b13a41ce47d`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.4 MB (1430585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a1036d493dc4dd595e00e2d074a1f421628cd10b4f493b473ef67cd67a4abf`  
		Last Modified: Wed, 24 Feb 2021 20:25:39 GMT  
		Size: 22.7 MB (22735386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f085f52231d080c77efb876c1979311824caadb20900af4cb7dc0bff59f7089`  
		Last Modified: Wed, 24 Feb 2021 20:25:36 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a97284eb2720d25a6d656c6c0f40165967d5109f2b537d74db9e6b1cb8e1c95`  
		Last Modified: Wed, 24 Feb 2021 20:25:36 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-data`

```console
$ docker pull influxdb@sha256:67876cecbc722648d5eaf17c64854ae57beafca233a55416e95fc212de64bd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data` - linux; amd64

```console
$ docker pull influxdb@sha256:9ad29edf6629eeeed7540d003ace92750e12e733055524dc08bc50c682eb8dec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126791523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1586215b740555a75748269f512871688d91312d26491ad08a114601e96719b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:57:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 10 Feb 2021 04:57:10 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:57:10 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:57:10 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:57:10 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:57:11 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:57:11 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:57:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:57:11 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d29e7e8838f6b925c171a67948b5f3bf44fca76a2428583987f3a7474f9e50`  
		Last Modified: Wed, 10 Feb 2021 04:59:10 GMT  
		Size: 65.8 MB (65796478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb80241906ed39ac62840cac80202f837585b84e0224d24571b11c957148879`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d44b9df77d08197aca251c63136878d862be3c48adb4878bace9022c7761a3f`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d904c7edfc7e2abba83d7274f2c25ff792d2688362e3f290b40a35b8f6da`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-data-alpine`

```console
$ docker pull influxdb@sha256:1cbf0fd3ca714ebb68d5b889753a3b9f10512cf81a87e7c79c2dc17dab74dfba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f1b67fd4756d1480e361b79ba03dd6a9d777cdefbb2142f041e38c947171bb00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69772703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae14395ed136bd664421fcbfce9681436c1325e66063e1937ae157e9c38cd3ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:21:16 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:22:32 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 24 Feb 2021 20:22:40 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:22:41 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 24 Feb 2021 20:22:41 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:22:41 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Feb 2021 20:22:41 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:22:41 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Feb 2021 20:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:22:42 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9587daa31955a7d1e8a3f596d61db5ef65bb6338a51db3fba1e5b13a41ce47d`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.4 MB (1430585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a215dce6b858821299be01bfcfdad396b1dfaa07b606378d73ad1cbb825460a`  
		Last Modified: Wed, 24 Feb 2021 20:25:28 GMT  
		Size: 65.5 MB (65540698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ec32d8f5562b2cb4c60c59728674cd0923f7bffdeb01b519b9d6f93c3a4077`  
		Last Modified: Wed, 24 Feb 2021 20:25:16 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5782b1dbc21eedfbe9cb042069cdc8517e0d9ce4d46ed7035255ce9bfd2a73`  
		Last Modified: Wed, 24 Feb 2021 20:25:16 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b09b9d2ad4c407fdfacfe363c7285cc8603df8eb96f1e27de544fe1321162ec`  
		Last Modified: Wed, 24 Feb 2021 20:25:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-meta`

```console
$ docker pull influxdb@sha256:83e2e77f7ef83ceaa7549f44058d12f255301a99fe7ba6cc1a6f4d8a9fe0cb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ffe8c67e7d6a188fe1378ca1541b43740e07f77497f65aacd47103897defe8ae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83859997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d706e62f1b535daeefd18b8bde7816e8310504c1c995ebc1701323883d94d74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:57:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 10 Feb 2021 04:57:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:57:24 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Feb 2021 04:57:24 GMT
EXPOSE 8091
# Wed, 10 Feb 2021 04:57:24 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:57:24 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:57:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:57:25 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ba6effd1841113e069182d033c17f3bdbbd57c3b3e9347abdc2bdecdde2ef`  
		Last Modified: Wed, 10 Feb 2021 04:59:23 GMT  
		Size: 22.9 MB (22866156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b75a883c5a79201ac582bb3980ed32e7f034f2f6ae3ec49667a25f4582463bf`  
		Last Modified: Wed, 10 Feb 2021 04:59:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ebe920089e36547964e057f165cf7102ff2925b478a707d02b94ebd670efe2`  
		Last Modified: Wed, 10 Feb 2021 04:59:17 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-meta-alpine`

```console
$ docker pull influxdb@sha256:8b4400145dd68d888c52412fe7a515807e73f0f2d4e2729797f40ccecdef0a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4d514f93b2481f610cf691acd8eb2e785724ac8bb5d95584a3e8d035769182b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26966186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30d5df01f013bbc9077d099080c9f7ebb77402f65ba3ea3599eb45fda601f52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:21:16 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:22:32 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 24 Feb 2021 20:22:54 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:22:54 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 24 Feb 2021 20:22:54 GMT
EXPOSE 8091
# Wed, 24 Feb 2021 20:22:55 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Feb 2021 20:22:55 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:22:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:22:55 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9587daa31955a7d1e8a3f596d61db5ef65bb6338a51db3fba1e5b13a41ce47d`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.4 MB (1430585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a1036d493dc4dd595e00e2d074a1f421628cd10b4f493b473ef67cd67a4abf`  
		Last Modified: Wed, 24 Feb 2021 20:25:39 GMT  
		Size: 22.7 MB (22735386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f085f52231d080c77efb876c1979311824caadb20900af4cb7dc0bff59f7089`  
		Last Modified: Wed, 24 Feb 2021 20:25:36 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a97284eb2720d25a6d656c6c0f40165967d5109f2b537d74db9e6b1cb8e1c95`  
		Last Modified: Wed, 24 Feb 2021 20:25:36 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.4`

```console
$ docker pull influxdb@sha256:6417d60baa5a7d45ef78d39871362d6c2d4e38ba5055f3e3f36b07b9fad5720f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.4` - linux; amd64

```console
$ docker pull influxdb@sha256:7539edbf76df0498f730904827f859aa4c67e1386cb72601019d72ec3e12ed0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125961499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7870fcea362222d648815a18c6d949e3faae225b97b8c0ee7cc27b74e9d8c45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:56:44 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 10 Feb 2021 04:56:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:56:52 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:56:52 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:56:52 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:56:53 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0907122426ac6b2c48c0e3da39e10da254ba8f0e10be1600731b210881c4ef`  
		Last Modified: Wed, 10 Feb 2021 04:58:50 GMT  
		Size: 65.0 MB (64966512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d3d7e535c1e62ce9dfa85b05ccb228f0cbf722440cb8958e74580f3de94dd3`  
		Last Modified: Wed, 10 Feb 2021 04:58:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45b611f60bfbba58da3ec97f086ba4c4dfeb487aef823873770166635986f00`  
		Last Modified: Wed, 10 Feb 2021 04:58:40 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7c9bc15cec46afb70a351b3614181ae2cab6e938d478f34bfbfe2cdda2dcd1`  
		Last Modified: Wed, 10 Feb 2021 04:58:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.4` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:0e871df7efa1bcdadef1bf9caa16fa62e7df6b14a36bbc8def8f5b41413e0598
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117020861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e988ce200cc5422b31c1b1e2f2712b921c2fb9392450ca3ead6297738bfcfb77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:05:10 GMT
ADD file:36669d020402a086f914d75419118f4daa1cbeeed645c1a77fe62cac0e804b59 in / 
# Fri, 12 Mar 2021 02:05:15 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:40:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 20:09:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 20:09:56 GMT
ENV INFLUXDB_VERSION=1.8.4
# Fri, 12 Mar 2021 20:10:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Fri, 12 Mar 2021 20:10:08 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 12 Mar 2021 20:10:08 GMT
EXPOSE 8086
# Fri, 12 Mar 2021 20:10:09 GMT
VOLUME [/var/lib/influxdb]
# Fri, 12 Mar 2021 20:10:10 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 12 Mar 2021 20:10:11 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 12 Mar 2021 20:10:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 20:10:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:87fcebbbbffa651ca8743935928db6e5acd0bef83a84d1dcc331b6a5dd2dd3a5`  
		Last Modified: Fri, 12 Mar 2021 02:14:09 GMT  
		Size: 42.1 MB (42120188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23db22a6953922b4d37e712f7abfd57e9d0b445d547049f3ae1aff068cd82b05`  
		Last Modified: Fri, 12 Mar 2021 03:50:06 GMT  
		Size: 9.9 MB (9915047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd48c000dbbac1ab4f6cc2b3bbdbd339981893df53383b9f000686f4a1c445b9`  
		Last Modified: Fri, 12 Mar 2021 03:50:04 GMT  
		Size: 3.9 MB (3921108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3176cabfa396c35e5640014ce46bfaa13e9007e5a47f2608a70aab36eb8e`  
		Last Modified: Fri, 12 Mar 2021 20:10:26 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb167310f3a548875e714ddde45998aea4499fce5033d716b5b04ab2cb6b1262`  
		Last Modified: Fri, 12 Mar 2021 20:11:07 GMT  
		Size: 61.1 MB (61059948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608915d3f8617c096894097dd31bda1103758728655cd17f7f0e70f6ef3f6c17`  
		Last Modified: Fri, 12 Mar 2021 20:10:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb6305fa7fdc9e5bc29b757b6959cab3fe33728efcdb43559ecc1bcd08ccf1d`  
		Last Modified: Fri, 12 Mar 2021 20:10:50 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653e39cfb10ae0305d8b9b9faa74a81d47ef2d743ff10757c7f3a66d3f4111c7`  
		Last Modified: Fri, 12 Mar 2021 20:10:50 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.8.4` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c19174cb29b46857b8f18777fc580d9c53779c90cef02e1e096e77803358c610
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118091914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb7c92e03b675b3aac5292a1cc2ff645d60a3ae5fc2953e63c173ba6a4415b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 22:02:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 22:03:12 GMT
ENV INFLUXDB_VERSION=1.8.4
# Fri, 12 Mar 2021 22:03:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Fri, 12 Mar 2021 22:03:25 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Fri, 12 Mar 2021 22:03:27 GMT
EXPOSE 8086
# Fri, 12 Mar 2021 22:03:28 GMT
VOLUME [/var/lib/influxdb]
# Fri, 12 Mar 2021 22:03:29 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Fri, 12 Mar 2021 22:03:30 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 12 Mar 2021 22:03:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 22:03:32 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680b71a7b1637cdab80389ba3468f3abae4d50d7ebe782252d744b21c7ec7d99`  
		Last Modified: Fri, 12 Mar 2021 22:04:46 GMT  
		Size: 2.9 KB (2859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca129c3a3f09bd2ccb403c9b0bb85a151b6c3a67958703d3e6ff28ce0ca611b`  
		Last Modified: Fri, 12 Mar 2021 22:05:27 GMT  
		Size: 60.6 MB (60629153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66af461b4ff441bff957b3857ba63125defef8afc5c017a07cd9c51ea93818f`  
		Last Modified: Fri, 12 Mar 2021 22:05:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04775a23b021a4c8c9574172b4be5ea4f17fd3d88110a24c9427c7aa83b6451`  
		Last Modified: Fri, 12 Mar 2021 22:05:14 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f691964b980cdeaddf521dee8a227dc0509f6eca0be542aa812081a3158963c`  
		Last Modified: Fri, 12 Mar 2021 22:05:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.4-alpine`

```console
$ docker pull influxdb@sha256:86a36871313ba3cd0f5f26f8544f60e38b941108b2c612f7772c1033aa67cf60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.4-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e116772bd838098506a6f8ca57b455dec36fc9707873772498bad5f4d4747797
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68938617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eae8355b824a04e3ef940b941ae02ff3213e00ff813647deb24502ead2504e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:21:16 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:22:12 GMT
ENV INFLUXDB_VERSION=1.8.4
# Wed, 24 Feb 2021 20:22:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:22:22 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 24 Feb 2021 20:22:22 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:22:23 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Feb 2021 20:22:23 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:22:23 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Feb 2021 20:22:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:22:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9587daa31955a7d1e8a3f596d61db5ef65bb6338a51db3fba1e5b13a41ce47d`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.4 MB (1430585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67573dc4c2905652fbf53bd085e37640f8ad5fa6ed55827c3320ec9cbc983c2e`  
		Last Modified: Wed, 24 Feb 2021 20:25:07 GMT  
		Size: 64.7 MB (64706672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7559d31e6811b2d616d086a16a9a98abe07afecabf63e492e9a1b57a515a197`  
		Last Modified: Wed, 24 Feb 2021 20:24:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a870449cb171fe01938a088101acac4d541fbc12a9b88c57f35a6735ca5cbc8`  
		Last Modified: Wed, 24 Feb 2021 20:24:57 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b16f6af06b8a0e84952ae3798b80dd1643d9ff368deba19676c8b85a4bf6919`  
		Last Modified: Wed, 24 Feb 2021 20:24:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0`

```console
$ docker pull influxdb@sha256:f80a16787d8e03e7d61b9ca23363bbb403c18a8f700204a971ff18de620f781d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0` - linux; amd64

```console
$ docker pull influxdb@sha256:84e443b88e658e0fd37a2491b135eb41b0ebffb0a70d9ac08774fa18e99ee1bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116196025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd69ea12fb632d6434f19ece8946e45304497983459d424d46e666541b0551c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:40 GMT
ADD file:8f75f11b2bd2d50e5912359ae750de06a7b49506df3756c19baf4cc63d900c4f in / 
# Tue, 09 Feb 2021 02:20:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:35:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 24 Feb 2021 20:23:01 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 24 Feb 2021 20:23:01 GMT
ENV GOSU_VER=1.12
# Wed, 24 Feb 2021 20:23:03 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 24 Feb 2021 20:23:03 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 24 Feb 2021 20:23:11 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 24 Feb 2021 20:23:12 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 24 Feb 2021 20:23:12 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Feb 2021 20:23:12 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 24 Feb 2021 20:23:12 GMT
COPY file:aff5e5953d000997c6afdf2d1f612256a94cb61763a6f20cdff8cbd3f5f9096e in /entrypoint.sh 
# Wed, 24 Feb 2021 20:23:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:23:13 GMT
CMD ["influxd"]
# Wed, 24 Feb 2021 20:23:13 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:23:14 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Feb 2021 20:23:14 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:0ecb575e629cd60aa802266a3bc6847dcf4073aa2a6d7d43f717dd61e7b90e0b`  
		Last Modified: Tue, 09 Feb 2021 02:26:22 GMT  
		Size: 50.4 MB (50400198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7467d1831b6947c294d92ee957902c3cd448b17c5ac2103ca5e79d15afb317c3`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 7.8 MB (7830684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feab2c490a3cea21cc051ff29c33cc9857418edfa1be9966124b18abe1d5ae16`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 10.0 MB (9996459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abc6153e13f807194e7e03b7095074b419b6f511ea4fa9fc7d6096c2dcf0418`  
		Last Modified: Wed, 24 Feb 2021 20:25:46 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee48ae9f680e00fc93022b4738498586888ca110cf7e4f3ce5f788b5dd8dc33b`  
		Last Modified: Wed, 24 Feb 2021 20:25:44 GMT  
		Size: 961.0 KB (960987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed0ebfdb96dcd4899bc75a23a2112502f23ae5feb8e4a1954e3714f9151db58`  
		Last Modified: Wed, 24 Feb 2021 20:25:52 GMT  
		Size: 47.0 MB (47001568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3904761f303d622cd12e3e12194b64f3227166a088ee088dd9d130d8d1b40c0`  
		Last Modified: Wed, 24 Feb 2021 20:25:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e1ba2d03a9c970446d278f9f6967f067343f7dfb6dbd5bd1e5e2af8db280dd`  
		Last Modified: Wed, 24 Feb 2021 20:25:44 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f575edf1a03a17c6aa8a6ce21948983dd9e588cff93b8af9d6ab933bbc09f85`  
		Last Modified: Wed, 24 Feb 2021 20:25:45 GMT  
		Size: 3.9 KB (3911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:07d7277af4df9abe844ba4e1ff505838b452b3ed8f70eb9cc170e85ddf2c7497
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112181128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637b2010e5ea28981e5c85cf9fd49d01933156136eb8ffa707446f8531de5b0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:16 GMT
ADD file:b2e2cca51e131b97e6a7e02af893c7f9b1f7a491b3d5fdaafa80409ed248a706 in / 
# Fri, 12 Mar 2021 01:53:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:29:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 22:03:44 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Fri, 12 Mar 2021 22:03:46 GMT
ENV GOSU_VER=1.12
# Fri, 12 Mar 2021 22:03:52 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Fri, 12 Mar 2021 22:03:53 GMT
ENV INFLUXDB_VERSION=2.0.4
# Fri, 12 Mar 2021 22:04:05 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Fri, 12 Mar 2021 22:04:08 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Fri, 12 Mar 2021 22:04:09 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 12 Mar 2021 22:04:10 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Fri, 12 Mar 2021 22:04:13 GMT
COPY file:aff5e5953d000997c6afdf2d1f612256a94cb61763a6f20cdff8cbd3f5f9096e in /entrypoint.sh 
# Fri, 12 Mar 2021 22:04:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 22:04:19 GMT
CMD ["influxd"]
# Fri, 12 Mar 2021 22:04:20 GMT
EXPOSE 8086
# Fri, 12 Mar 2021 22:04:21 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 12 Mar 2021 22:04:22 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:e9742a63e95a88f8685c4f23a73f7dd15e4039ac1862ce5753c53406a5f7c04a`  
		Last Modified: Fri, 12 Mar 2021 02:01:14 GMT  
		Size: 49.2 MB (49195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90273c85fdda8648cee9282aa7b01faf0ec1f45451931985b3504c37cf1ac3e6`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 7.7 MB (7694407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685f873e984153af9a44cf556c7679b430b9c557d901c7d476725134f28754e7`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 10.0 MB (9984339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20896926cd69e8e7eceb8d7459b09a21b50e40799609272022bc969240c79b65`  
		Last Modified: Fri, 12 Mar 2021 22:05:35 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417e6a0f2513081ab6863a9f01d46e3f29e71475b870cb71865f37fa27b149aa`  
		Last Modified: Fri, 12 Mar 2021 22:05:34 GMT  
		Size: 896.4 KB (896378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9896d840c23af2d8e3d23c74a2e0f73fe09a3c3ff1e8e04c7a505912c2503e`  
		Last Modified: Fri, 12 Mar 2021 22:05:45 GMT  
		Size: 44.4 MB (44403985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1b6c919cd48e39334e6cc6851ba291c43af9e44fa178b45aa81dc4a88a227d`  
		Last Modified: Fri, 12 Mar 2021 22:05:34 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a94557b27cd6c85248df1fb4a18c6eba531bf737c9bdb7e05eafc2e3a4ae029`  
		Last Modified: Fri, 12 Mar 2021 22:05:34 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476aa19e8c28d65b349491c738d907327b21aba773bdd05577619bbc65543cea`  
		Last Modified: Fri, 12 Mar 2021 22:05:34 GMT  
		Size: 3.9 KB (3911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0-alpine`

```console
$ docker pull influxdb@sha256:154f2b6995c542a72590a37cd3632583fb1d27f9d8a35bad94870f7a608c7fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:10760b71350a4bf3c2a5af97ae080f3f12f86764453a13559466075a356a22b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60498570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f4559b6bf85c7415a74607caac6124dc334cd321689b9a487cc8ce5f86b629`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 06:58:12 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:23:20 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Wed, 24 Feb 2021 20:23:21 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 24 Feb 2021 20:23:22 GMT
ENV GOSU_VER=1.12
# Wed, 24 Feb 2021 20:23:24 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Feb 2021 20:23:24 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 24 Feb 2021 20:23:30 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 24 Feb 2021 20:23:31 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 24 Feb 2021 20:23:31 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Feb 2021 20:23:31 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 24 Feb 2021 20:23:32 GMT
COPY file:aff5e5953d000997c6afdf2d1f612256a94cb61763a6f20cdff8cbd3f5f9096e in /entrypoint.sh 
# Wed, 24 Feb 2021 20:23:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:23:32 GMT
CMD ["influxd"]
# Wed, 24 Feb 2021 20:23:32 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:23:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Feb 2021 20:23:33 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a566023623516b301d90728ad0e1530d806f4443c0a6991f786c0f6d2c9104`  
		Last Modified: Thu, 18 Feb 2021 06:58:53 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0989adc1cc7bf6af3d45e8719211aae491a59b8fe0029a7cabe464f7747168af`  
		Last Modified: Wed, 24 Feb 2021 20:26:02 GMT  
		Size: 9.7 MB (9718997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a806d7f307b8d2fb7fbf9b1a761895969ab8278b7f012a5db891a2b68edf41fd`  
		Last Modified: Wed, 24 Feb 2021 20:26:01 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191954546f9556ea0fa3cf36bdd81dcb432ea2f0239fef9871d4a344a870d23b`  
		Last Modified: Wed, 24 Feb 2021 20:25:59 GMT  
		Size: 960.6 KB (960620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274ec7667baa873725fba001208aead4b377e4e53c3477cb5b99a8950cf9d705`  
		Last Modified: Wed, 24 Feb 2021 20:26:09 GMT  
		Size: 47.0 MB (47001563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88350c4a12d5663e61cc88613649898e9803f06a27115acf445d3edb96a74cb6`  
		Last Modified: Wed, 24 Feb 2021 20:25:59 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99128313103dc871806282fea18241c440c6e749041dbaa4547ccb1a7699be03`  
		Last Modified: Wed, 24 Feb 2021 20:25:59 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc440e2fed73d1eb94dd9626c50ceba023c27dc938903288b3ef080bf25d8313`  
		Last Modified: Wed, 24 Feb 2021 20:25:59 GMT  
		Size: 3.9 KB (3911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:cfbcdce6fc020f8a7fe0de37a5f5754a7aebbcfa085239ea58a2ba5c9b49b729
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57581262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81b6a01afe437ace6c08fb26a622060e710175058e2fd617ad5e925346ad6dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:41:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:41:56 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Wed, 24 Feb 2021 20:41:58 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 24 Feb 2021 20:41:59 GMT
ENV GOSU_VER=1.12
# Wed, 24 Feb 2021 20:42:02 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Feb 2021 20:42:03 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 24 Feb 2021 20:42:09 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 24 Feb 2021 20:42:12 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 24 Feb 2021 20:42:12 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Feb 2021 20:42:13 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 24 Feb 2021 20:42:14 GMT
COPY file:aff5e5953d000997c6afdf2d1f612256a94cb61763a6f20cdff8cbd3f5f9096e in /entrypoint.sh 
# Wed, 24 Feb 2021 20:42:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:42:15 GMT
CMD ["influxd"]
# Wed, 24 Feb 2021 20:42:16 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:42:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Feb 2021 20:42:17 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e15e59e4d1588f19fb5f25ffa8e496aef33f2e8da76b1a8f7a879869722b9c`  
		Last Modified: Wed, 24 Feb 2021 20:43:00 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd41230647a2c5407c9914def795842841aeb26a63391c9a1179142826614e9e`  
		Last Modified: Wed, 24 Feb 2021 20:43:02 GMT  
		Size: 9.6 MB (9563763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb81695f31cd3efc0d73f8c70ae13c90b62769c90edb4b344e69a93efa2ad3`  
		Last Modified: Wed, 24 Feb 2021 20:43:00 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab5c69196cb98414f56cd0c6d75ffa78bccc2541c6462ae81c12e2249f796f7`  
		Last Modified: Wed, 24 Feb 2021 20:42:59 GMT  
		Size: 896.1 KB (896103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883219e6a21d47dace2080fa1f2acd8d1e1aee2fe78291b81910669d6c992b6e`  
		Last Modified: Wed, 24 Feb 2021 20:43:08 GMT  
		Size: 44.4 MB (44403964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02f7d61d0af8fca81d1dfd14f21d515f0d27055942f373f2bc2683fa9f5ea3`  
		Last Modified: Wed, 24 Feb 2021 20:42:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53fec386ce0de3617258287a25e605aed95b8138778ea1994fb94cf7526dade`  
		Last Modified: Wed, 24 Feb 2021 20:42:58 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c947e1f4cd567b258426c8457dd6e897cad29ef52a79ab2c0ac64b651d2a3d5b`  
		Last Modified: Wed, 24 Feb 2021 20:42:58 GMT  
		Size: 3.9 KB (3911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0.4`

```console
$ docker pull influxdb@sha256:f80a16787d8e03e7d61b9ca23363bbb403c18a8f700204a971ff18de620f781d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0.4` - linux; amd64

```console
$ docker pull influxdb@sha256:84e443b88e658e0fd37a2491b135eb41b0ebffb0a70d9ac08774fa18e99ee1bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116196025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd69ea12fb632d6434f19ece8946e45304497983459d424d46e666541b0551c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:40 GMT
ADD file:8f75f11b2bd2d50e5912359ae750de06a7b49506df3756c19baf4cc63d900c4f in / 
# Tue, 09 Feb 2021 02:20:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:35:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 24 Feb 2021 20:23:01 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 24 Feb 2021 20:23:01 GMT
ENV GOSU_VER=1.12
# Wed, 24 Feb 2021 20:23:03 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 24 Feb 2021 20:23:03 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 24 Feb 2021 20:23:11 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 24 Feb 2021 20:23:12 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 24 Feb 2021 20:23:12 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Feb 2021 20:23:12 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 24 Feb 2021 20:23:12 GMT
COPY file:aff5e5953d000997c6afdf2d1f612256a94cb61763a6f20cdff8cbd3f5f9096e in /entrypoint.sh 
# Wed, 24 Feb 2021 20:23:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:23:13 GMT
CMD ["influxd"]
# Wed, 24 Feb 2021 20:23:13 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:23:14 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Feb 2021 20:23:14 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:0ecb575e629cd60aa802266a3bc6847dcf4073aa2a6d7d43f717dd61e7b90e0b`  
		Last Modified: Tue, 09 Feb 2021 02:26:22 GMT  
		Size: 50.4 MB (50400198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7467d1831b6947c294d92ee957902c3cd448b17c5ac2103ca5e79d15afb317c3`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 7.8 MB (7830684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feab2c490a3cea21cc051ff29c33cc9857418edfa1be9966124b18abe1d5ae16`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 10.0 MB (9996459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abc6153e13f807194e7e03b7095074b419b6f511ea4fa9fc7d6096c2dcf0418`  
		Last Modified: Wed, 24 Feb 2021 20:25:46 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee48ae9f680e00fc93022b4738498586888ca110cf7e4f3ce5f788b5dd8dc33b`  
		Last Modified: Wed, 24 Feb 2021 20:25:44 GMT  
		Size: 961.0 KB (960987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed0ebfdb96dcd4899bc75a23a2112502f23ae5feb8e4a1954e3714f9151db58`  
		Last Modified: Wed, 24 Feb 2021 20:25:52 GMT  
		Size: 47.0 MB (47001568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3904761f303d622cd12e3e12194b64f3227166a088ee088dd9d130d8d1b40c0`  
		Last Modified: Wed, 24 Feb 2021 20:25:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e1ba2d03a9c970446d278f9f6967f067343f7dfb6dbd5bd1e5e2af8db280dd`  
		Last Modified: Wed, 24 Feb 2021 20:25:44 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f575edf1a03a17c6aa8a6ce21948983dd9e588cff93b8af9d6ab933bbc09f85`  
		Last Modified: Wed, 24 Feb 2021 20:25:45 GMT  
		Size: 3.9 KB (3911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0.4` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:07d7277af4df9abe844ba4e1ff505838b452b3ed8f70eb9cc170e85ddf2c7497
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112181128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637b2010e5ea28981e5c85cf9fd49d01933156136eb8ffa707446f8531de5b0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:16 GMT
ADD file:b2e2cca51e131b97e6a7e02af893c7f9b1f7a491b3d5fdaafa80409ed248a706 in / 
# Fri, 12 Mar 2021 01:53:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:29:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 22:03:44 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Fri, 12 Mar 2021 22:03:46 GMT
ENV GOSU_VER=1.12
# Fri, 12 Mar 2021 22:03:52 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Fri, 12 Mar 2021 22:03:53 GMT
ENV INFLUXDB_VERSION=2.0.4
# Fri, 12 Mar 2021 22:04:05 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Fri, 12 Mar 2021 22:04:08 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Fri, 12 Mar 2021 22:04:09 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 12 Mar 2021 22:04:10 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Fri, 12 Mar 2021 22:04:13 GMT
COPY file:aff5e5953d000997c6afdf2d1f612256a94cb61763a6f20cdff8cbd3f5f9096e in /entrypoint.sh 
# Fri, 12 Mar 2021 22:04:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 22:04:19 GMT
CMD ["influxd"]
# Fri, 12 Mar 2021 22:04:20 GMT
EXPOSE 8086
# Fri, 12 Mar 2021 22:04:21 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 12 Mar 2021 22:04:22 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:e9742a63e95a88f8685c4f23a73f7dd15e4039ac1862ce5753c53406a5f7c04a`  
		Last Modified: Fri, 12 Mar 2021 02:01:14 GMT  
		Size: 49.2 MB (49195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90273c85fdda8648cee9282aa7b01faf0ec1f45451931985b3504c37cf1ac3e6`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 7.7 MB (7694407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685f873e984153af9a44cf556c7679b430b9c557d901c7d476725134f28754e7`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 10.0 MB (9984339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20896926cd69e8e7eceb8d7459b09a21b50e40799609272022bc969240c79b65`  
		Last Modified: Fri, 12 Mar 2021 22:05:35 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417e6a0f2513081ab6863a9f01d46e3f29e71475b870cb71865f37fa27b149aa`  
		Last Modified: Fri, 12 Mar 2021 22:05:34 GMT  
		Size: 896.4 KB (896378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9896d840c23af2d8e3d23c74a2e0f73fe09a3c3ff1e8e04c7a505912c2503e`  
		Last Modified: Fri, 12 Mar 2021 22:05:45 GMT  
		Size: 44.4 MB (44403985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1b6c919cd48e39334e6cc6851ba291c43af9e44fa178b45aa81dc4a88a227d`  
		Last Modified: Fri, 12 Mar 2021 22:05:34 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a94557b27cd6c85248df1fb4a18c6eba531bf737c9bdb7e05eafc2e3a4ae029`  
		Last Modified: Fri, 12 Mar 2021 22:05:34 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476aa19e8c28d65b349491c738d907327b21aba773bdd05577619bbc65543cea`  
		Last Modified: Fri, 12 Mar 2021 22:05:34 GMT  
		Size: 3.9 KB (3911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0.4-alpine`

```console
$ docker pull influxdb@sha256:154f2b6995c542a72590a37cd3632583fb1d27f9d8a35bad94870f7a608c7fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0.4-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:10760b71350a4bf3c2a5af97ae080f3f12f86764453a13559466075a356a22b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60498570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f4559b6bf85c7415a74607caac6124dc334cd321689b9a487cc8ce5f86b629`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 06:58:12 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:23:20 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Wed, 24 Feb 2021 20:23:21 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 24 Feb 2021 20:23:22 GMT
ENV GOSU_VER=1.12
# Wed, 24 Feb 2021 20:23:24 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Feb 2021 20:23:24 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 24 Feb 2021 20:23:30 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 24 Feb 2021 20:23:31 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 24 Feb 2021 20:23:31 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Feb 2021 20:23:31 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 24 Feb 2021 20:23:32 GMT
COPY file:aff5e5953d000997c6afdf2d1f612256a94cb61763a6f20cdff8cbd3f5f9096e in /entrypoint.sh 
# Wed, 24 Feb 2021 20:23:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:23:32 GMT
CMD ["influxd"]
# Wed, 24 Feb 2021 20:23:32 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:23:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Feb 2021 20:23:33 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a566023623516b301d90728ad0e1530d806f4443c0a6991f786c0f6d2c9104`  
		Last Modified: Thu, 18 Feb 2021 06:58:53 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0989adc1cc7bf6af3d45e8719211aae491a59b8fe0029a7cabe464f7747168af`  
		Last Modified: Wed, 24 Feb 2021 20:26:02 GMT  
		Size: 9.7 MB (9718997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a806d7f307b8d2fb7fbf9b1a761895969ab8278b7f012a5db891a2b68edf41fd`  
		Last Modified: Wed, 24 Feb 2021 20:26:01 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191954546f9556ea0fa3cf36bdd81dcb432ea2f0239fef9871d4a344a870d23b`  
		Last Modified: Wed, 24 Feb 2021 20:25:59 GMT  
		Size: 960.6 KB (960620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274ec7667baa873725fba001208aead4b377e4e53c3477cb5b99a8950cf9d705`  
		Last Modified: Wed, 24 Feb 2021 20:26:09 GMT  
		Size: 47.0 MB (47001563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88350c4a12d5663e61cc88613649898e9803f06a27115acf445d3edb96a74cb6`  
		Last Modified: Wed, 24 Feb 2021 20:25:59 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99128313103dc871806282fea18241c440c6e749041dbaa4547ccb1a7699be03`  
		Last Modified: Wed, 24 Feb 2021 20:25:59 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc440e2fed73d1eb94dd9626c50ceba023c27dc938903288b3ef080bf25d8313`  
		Last Modified: Wed, 24 Feb 2021 20:25:59 GMT  
		Size: 3.9 KB (3911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0.4-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:cfbcdce6fc020f8a7fe0de37a5f5754a7aebbcfa085239ea58a2ba5c9b49b729
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57581262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81b6a01afe437ace6c08fb26a622060e710175058e2fd617ad5e925346ad6dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:41:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:41:56 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Wed, 24 Feb 2021 20:41:58 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 24 Feb 2021 20:41:59 GMT
ENV GOSU_VER=1.12
# Wed, 24 Feb 2021 20:42:02 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Feb 2021 20:42:03 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 24 Feb 2021 20:42:09 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 24 Feb 2021 20:42:12 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 24 Feb 2021 20:42:12 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Feb 2021 20:42:13 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 24 Feb 2021 20:42:14 GMT
COPY file:aff5e5953d000997c6afdf2d1f612256a94cb61763a6f20cdff8cbd3f5f9096e in /entrypoint.sh 
# Wed, 24 Feb 2021 20:42:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:42:15 GMT
CMD ["influxd"]
# Wed, 24 Feb 2021 20:42:16 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:42:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Feb 2021 20:42:17 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e15e59e4d1588f19fb5f25ffa8e496aef33f2e8da76b1a8f7a879869722b9c`  
		Last Modified: Wed, 24 Feb 2021 20:43:00 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd41230647a2c5407c9914def795842841aeb26a63391c9a1179142826614e9e`  
		Last Modified: Wed, 24 Feb 2021 20:43:02 GMT  
		Size: 9.6 MB (9563763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb81695f31cd3efc0d73f8c70ae13c90b62769c90edb4b344e69a93efa2ad3`  
		Last Modified: Wed, 24 Feb 2021 20:43:00 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab5c69196cb98414f56cd0c6d75ffa78bccc2541c6462ae81c12e2249f796f7`  
		Last Modified: Wed, 24 Feb 2021 20:42:59 GMT  
		Size: 896.1 KB (896103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883219e6a21d47dace2080fa1f2acd8d1e1aee2fe78291b81910669d6c992b6e`  
		Last Modified: Wed, 24 Feb 2021 20:43:08 GMT  
		Size: 44.4 MB (44403964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02f7d61d0af8fca81d1dfd14f21d515f0d27055942f373f2bc2683fa9f5ea3`  
		Last Modified: Wed, 24 Feb 2021 20:42:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53fec386ce0de3617258287a25e605aed95b8138778ea1994fb94cf7526dade`  
		Last Modified: Wed, 24 Feb 2021 20:42:58 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c947e1f4cd567b258426c8457dd6e897cad29ef52a79ab2c0ac64b651d2a3d5b`  
		Last Modified: Wed, 24 Feb 2021 20:42:58 GMT  
		Size: 3.9 KB (3911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:154f2b6995c542a72590a37cd3632583fb1d27f9d8a35bad94870f7a608c7fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:10760b71350a4bf3c2a5af97ae080f3f12f86764453a13559466075a356a22b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60498570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f4559b6bf85c7415a74607caac6124dc334cd321689b9a487cc8ce5f86b629`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 06:58:12 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:23:20 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Wed, 24 Feb 2021 20:23:21 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 24 Feb 2021 20:23:22 GMT
ENV GOSU_VER=1.12
# Wed, 24 Feb 2021 20:23:24 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Feb 2021 20:23:24 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 24 Feb 2021 20:23:30 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 24 Feb 2021 20:23:31 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 24 Feb 2021 20:23:31 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Feb 2021 20:23:31 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 24 Feb 2021 20:23:32 GMT
COPY file:aff5e5953d000997c6afdf2d1f612256a94cb61763a6f20cdff8cbd3f5f9096e in /entrypoint.sh 
# Wed, 24 Feb 2021 20:23:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:23:32 GMT
CMD ["influxd"]
# Wed, 24 Feb 2021 20:23:32 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:23:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Feb 2021 20:23:33 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a566023623516b301d90728ad0e1530d806f4443c0a6991f786c0f6d2c9104`  
		Last Modified: Thu, 18 Feb 2021 06:58:53 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0989adc1cc7bf6af3d45e8719211aae491a59b8fe0029a7cabe464f7747168af`  
		Last Modified: Wed, 24 Feb 2021 20:26:02 GMT  
		Size: 9.7 MB (9718997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a806d7f307b8d2fb7fbf9b1a761895969ab8278b7f012a5db891a2b68edf41fd`  
		Last Modified: Wed, 24 Feb 2021 20:26:01 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191954546f9556ea0fa3cf36bdd81dcb432ea2f0239fef9871d4a344a870d23b`  
		Last Modified: Wed, 24 Feb 2021 20:25:59 GMT  
		Size: 960.6 KB (960620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274ec7667baa873725fba001208aead4b377e4e53c3477cb5b99a8950cf9d705`  
		Last Modified: Wed, 24 Feb 2021 20:26:09 GMT  
		Size: 47.0 MB (47001563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88350c4a12d5663e61cc88613649898e9803f06a27115acf445d3edb96a74cb6`  
		Last Modified: Wed, 24 Feb 2021 20:25:59 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99128313103dc871806282fea18241c440c6e749041dbaa4547ccb1a7699be03`  
		Last Modified: Wed, 24 Feb 2021 20:25:59 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc440e2fed73d1eb94dd9626c50ceba023c27dc938903288b3ef080bf25d8313`  
		Last Modified: Wed, 24 Feb 2021 20:25:59 GMT  
		Size: 3.9 KB (3911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:cfbcdce6fc020f8a7fe0de37a5f5754a7aebbcfa085239ea58a2ba5c9b49b729
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57581262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81b6a01afe437ace6c08fb26a622060e710175058e2fd617ad5e925346ad6dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:41:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:41:56 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Wed, 24 Feb 2021 20:41:58 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 24 Feb 2021 20:41:59 GMT
ENV GOSU_VER=1.12
# Wed, 24 Feb 2021 20:42:02 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Feb 2021 20:42:03 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 24 Feb 2021 20:42:09 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 24 Feb 2021 20:42:12 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 24 Feb 2021 20:42:12 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Feb 2021 20:42:13 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 24 Feb 2021 20:42:14 GMT
COPY file:aff5e5953d000997c6afdf2d1f612256a94cb61763a6f20cdff8cbd3f5f9096e in /entrypoint.sh 
# Wed, 24 Feb 2021 20:42:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:42:15 GMT
CMD ["influxd"]
# Wed, 24 Feb 2021 20:42:16 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:42:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Feb 2021 20:42:17 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e15e59e4d1588f19fb5f25ffa8e496aef33f2e8da76b1a8f7a879869722b9c`  
		Last Modified: Wed, 24 Feb 2021 20:43:00 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd41230647a2c5407c9914def795842841aeb26a63391c9a1179142826614e9e`  
		Last Modified: Wed, 24 Feb 2021 20:43:02 GMT  
		Size: 9.6 MB (9563763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb81695f31cd3efc0d73f8c70ae13c90b62769c90edb4b344e69a93efa2ad3`  
		Last Modified: Wed, 24 Feb 2021 20:43:00 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab5c69196cb98414f56cd0c6d75ffa78bccc2541c6462ae81c12e2249f796f7`  
		Last Modified: Wed, 24 Feb 2021 20:42:59 GMT  
		Size: 896.1 KB (896103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883219e6a21d47dace2080fa1f2acd8d1e1aee2fe78291b81910669d6c992b6e`  
		Last Modified: Wed, 24 Feb 2021 20:43:08 GMT  
		Size: 44.4 MB (44403964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02f7d61d0af8fca81d1dfd14f21d515f0d27055942f373f2bc2683fa9f5ea3`  
		Last Modified: Wed, 24 Feb 2021 20:42:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53fec386ce0de3617258287a25e605aed95b8138778ea1994fb94cf7526dade`  
		Last Modified: Wed, 24 Feb 2021 20:42:58 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c947e1f4cd567b258426c8457dd6e897cad29ef52a79ab2c0ac64b651d2a3d5b`  
		Last Modified: Wed, 24 Feb 2021 20:42:58 GMT  
		Size: 3.9 KB (3911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data`

```console
$ docker pull influxdb@sha256:67876cecbc722648d5eaf17c64854ae57beafca233a55416e95fc212de64bd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:9ad29edf6629eeeed7540d003ace92750e12e733055524dc08bc50c682eb8dec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126791523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1586215b740555a75748269f512871688d91312d26491ad08a114601e96719b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:57:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 10 Feb 2021 04:57:10 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:57:10 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 10 Feb 2021 04:57:10 GMT
EXPOSE 8086
# Wed, 10 Feb 2021 04:57:10 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:57:11 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:57:11 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 10 Feb 2021 04:57:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:57:11 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d29e7e8838f6b925c171a67948b5f3bf44fca76a2428583987f3a7474f9e50`  
		Last Modified: Wed, 10 Feb 2021 04:59:10 GMT  
		Size: 65.8 MB (65796478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb80241906ed39ac62840cac80202f837585b84e0224d24571b11c957148879`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d44b9df77d08197aca251c63136878d862be3c48adb4878bace9022c7761a3f`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a88d904c7edfc7e2abba83d7274f2c25ff792d2688362e3f290b40a35b8f6da`  
		Last Modified: Wed, 10 Feb 2021 04:59:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:1cbf0fd3ca714ebb68d5b889753a3b9f10512cf81a87e7c79c2dc17dab74dfba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f1b67fd4756d1480e361b79ba03dd6a9d777cdefbb2142f041e38c947171bb00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69772703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae14395ed136bd664421fcbfce9681436c1325e66063e1937ae157e9c38cd3ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:21:16 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:22:32 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 24 Feb 2021 20:22:40 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:22:41 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 24 Feb 2021 20:22:41 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:22:41 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Feb 2021 20:22:41 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:22:41 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Feb 2021 20:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:22:42 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9587daa31955a7d1e8a3f596d61db5ef65bb6338a51db3fba1e5b13a41ce47d`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.4 MB (1430585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a215dce6b858821299be01bfcfdad396b1dfaa07b606378d73ad1cbb825460a`  
		Last Modified: Wed, 24 Feb 2021 20:25:28 GMT  
		Size: 65.5 MB (65540698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ec32d8f5562b2cb4c60c59728674cd0923f7bffdeb01b519b9d6f93c3a4077`  
		Last Modified: Wed, 24 Feb 2021 20:25:16 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5782b1dbc21eedfbe9cb042069cdc8517e0d9ce4d46ed7035255ce9bfd2a73`  
		Last Modified: Wed, 24 Feb 2021 20:25:16 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b09b9d2ad4c407fdfacfe363c7285cc8603df8eb96f1e27de544fe1321162ec`  
		Last Modified: Wed, 24 Feb 2021 20:25:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:f80a16787d8e03e7d61b9ca23363bbb403c18a8f700204a971ff18de620f781d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:84e443b88e658e0fd37a2491b135eb41b0ebffb0a70d9ac08774fa18e99ee1bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116196025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd69ea12fb632d6434f19ece8946e45304497983459d424d46e666541b0551c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:40 GMT
ADD file:8f75f11b2bd2d50e5912359ae750de06a7b49506df3756c19baf4cc63d900c4f in / 
# Tue, 09 Feb 2021 02:20:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:35:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 24 Feb 2021 20:23:01 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 24 Feb 2021 20:23:01 GMT
ENV GOSU_VER=1.12
# Wed, 24 Feb 2021 20:23:03 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 24 Feb 2021 20:23:03 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 24 Feb 2021 20:23:11 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 24 Feb 2021 20:23:12 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 24 Feb 2021 20:23:12 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Feb 2021 20:23:12 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 24 Feb 2021 20:23:12 GMT
COPY file:aff5e5953d000997c6afdf2d1f612256a94cb61763a6f20cdff8cbd3f5f9096e in /entrypoint.sh 
# Wed, 24 Feb 2021 20:23:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:23:13 GMT
CMD ["influxd"]
# Wed, 24 Feb 2021 20:23:13 GMT
EXPOSE 8086
# Wed, 24 Feb 2021 20:23:14 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Feb 2021 20:23:14 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:0ecb575e629cd60aa802266a3bc6847dcf4073aa2a6d7d43f717dd61e7b90e0b`  
		Last Modified: Tue, 09 Feb 2021 02:26:22 GMT  
		Size: 50.4 MB (50400198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7467d1831b6947c294d92ee957902c3cd448b17c5ac2103ca5e79d15afb317c3`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 7.8 MB (7830684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feab2c490a3cea21cc051ff29c33cc9857418edfa1be9966124b18abe1d5ae16`  
		Last Modified: Tue, 09 Feb 2021 04:46:00 GMT  
		Size: 10.0 MB (9996459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abc6153e13f807194e7e03b7095074b419b6f511ea4fa9fc7d6096c2dcf0418`  
		Last Modified: Wed, 24 Feb 2021 20:25:46 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee48ae9f680e00fc93022b4738498586888ca110cf7e4f3ce5f788b5dd8dc33b`  
		Last Modified: Wed, 24 Feb 2021 20:25:44 GMT  
		Size: 961.0 KB (960987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed0ebfdb96dcd4899bc75a23a2112502f23ae5feb8e4a1954e3714f9151db58`  
		Last Modified: Wed, 24 Feb 2021 20:25:52 GMT  
		Size: 47.0 MB (47001568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3904761f303d622cd12e3e12194b64f3227166a088ee088dd9d130d8d1b40c0`  
		Last Modified: Wed, 24 Feb 2021 20:25:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e1ba2d03a9c970446d278f9f6967f067343f7dfb6dbd5bd1e5e2af8db280dd`  
		Last Modified: Wed, 24 Feb 2021 20:25:44 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f575edf1a03a17c6aa8a6ce21948983dd9e588cff93b8af9d6ab933bbc09f85`  
		Last Modified: Wed, 24 Feb 2021 20:25:45 GMT  
		Size: 3.9 KB (3911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:07d7277af4df9abe844ba4e1ff505838b452b3ed8f70eb9cc170e85ddf2c7497
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112181128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637b2010e5ea28981e5c85cf9fd49d01933156136eb8ffa707446f8531de5b0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:16 GMT
ADD file:b2e2cca51e131b97e6a7e02af893c7f9b1f7a491b3d5fdaafa80409ed248a706 in / 
# Fri, 12 Mar 2021 01:53:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:29:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:29:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 22:03:44 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Fri, 12 Mar 2021 22:03:46 GMT
ENV GOSU_VER=1.12
# Fri, 12 Mar 2021 22:03:52 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Fri, 12 Mar 2021 22:03:53 GMT
ENV INFLUXDB_VERSION=2.0.4
# Fri, 12 Mar 2021 22:04:05 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Fri, 12 Mar 2021 22:04:08 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Fri, 12 Mar 2021 22:04:09 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 12 Mar 2021 22:04:10 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Fri, 12 Mar 2021 22:04:13 GMT
COPY file:aff5e5953d000997c6afdf2d1f612256a94cb61763a6f20cdff8cbd3f5f9096e in /entrypoint.sh 
# Fri, 12 Mar 2021 22:04:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 22:04:19 GMT
CMD ["influxd"]
# Fri, 12 Mar 2021 22:04:20 GMT
EXPOSE 8086
# Fri, 12 Mar 2021 22:04:21 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 12 Mar 2021 22:04:22 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:e9742a63e95a88f8685c4f23a73f7dd15e4039ac1862ce5753c53406a5f7c04a`  
		Last Modified: Fri, 12 Mar 2021 02:01:14 GMT  
		Size: 49.2 MB (49195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90273c85fdda8648cee9282aa7b01faf0ec1f45451931985b3504c37cf1ac3e6`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 7.7 MB (7694407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685f873e984153af9a44cf556c7679b430b9c557d901c7d476725134f28754e7`  
		Last Modified: Fri, 12 Mar 2021 02:43:30 GMT  
		Size: 10.0 MB (9984339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20896926cd69e8e7eceb8d7459b09a21b50e40799609272022bc969240c79b65`  
		Last Modified: Fri, 12 Mar 2021 22:05:35 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417e6a0f2513081ab6863a9f01d46e3f29e71475b870cb71865f37fa27b149aa`  
		Last Modified: Fri, 12 Mar 2021 22:05:34 GMT  
		Size: 896.4 KB (896378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9896d840c23af2d8e3d23c74a2e0f73fe09a3c3ff1e8e04c7a505912c2503e`  
		Last Modified: Fri, 12 Mar 2021 22:05:45 GMT  
		Size: 44.4 MB (44403985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1b6c919cd48e39334e6cc6851ba291c43af9e44fa178b45aa81dc4a88a227d`  
		Last Modified: Fri, 12 Mar 2021 22:05:34 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a94557b27cd6c85248df1fb4a18c6eba531bf737c9bdb7e05eafc2e3a4ae029`  
		Last Modified: Fri, 12 Mar 2021 22:05:34 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476aa19e8c28d65b349491c738d907327b21aba773bdd05577619bbc65543cea`  
		Last Modified: Fri, 12 Mar 2021 22:05:34 GMT  
		Size: 3.9 KB (3911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:83e2e77f7ef83ceaa7549f44058d12f255301a99fe7ba6cc1a6f4d8a9fe0cb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ffe8c67e7d6a188fe1378ca1541b43740e07f77497f65aacd47103897defe8ae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83859997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d706e62f1b535daeefd18b8bde7816e8310504c1c995ebc1701323883d94d74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:55:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:57:02 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 10 Feb 2021 04:57:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 10 Feb 2021 04:57:24 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 10 Feb 2021 04:57:24 GMT
EXPOSE 8091
# Wed, 10 Feb 2021 04:57:24 GMT
VOLUME [/var/lib/influxdb]
# Wed, 10 Feb 2021 04:57:24 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 10 Feb 2021 04:57:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:57:25 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0485a89d8e9c67bdd94e4042a819881d93674b78e0ec3daabcb42766d2c324`  
		Last Modified: Wed, 10 Feb 2021 04:57:58 GMT  
		Size: 2.8 KB (2828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ba6effd1841113e069182d033c17f3bdbbd57c3b3e9347abdc2bdecdde2ef`  
		Last Modified: Wed, 10 Feb 2021 04:59:23 GMT  
		Size: 22.9 MB (22866156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b75a883c5a79201ac582bb3980ed32e7f034f2f6ae3ec49667a25f4582463bf`  
		Last Modified: Wed, 10 Feb 2021 04:59:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ebe920089e36547964e057f165cf7102ff2925b478a707d02b94ebd670efe2`  
		Last Modified: Wed, 10 Feb 2021 04:59:17 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:8b4400145dd68d888c52412fe7a515807e73f0f2d4e2729797f40ccecdef0a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4d514f93b2481f610cf691acd8eb2e785724ac8bb5d95584a3e8d035769182b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26966186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30d5df01f013bbc9077d099080c9f7ebb77402f65ba3ea3599eb45fda601f52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:21:16 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 20:22:32 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 24 Feb 2021 20:22:54 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 20:22:54 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 24 Feb 2021 20:22:54 GMT
EXPOSE 8091
# Wed, 24 Feb 2021 20:22:55 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Feb 2021 20:22:55 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 24 Feb 2021 20:22:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 20:22:55 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9587daa31955a7d1e8a3f596d61db5ef65bb6338a51db3fba1e5b13a41ce47d`  
		Last Modified: Wed, 24 Feb 2021 20:24:09 GMT  
		Size: 1.4 MB (1430585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a1036d493dc4dd595e00e2d074a1f421628cd10b4f493b473ef67cd67a4abf`  
		Last Modified: Wed, 24 Feb 2021 20:25:39 GMT  
		Size: 22.7 MB (22735386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f085f52231d080c77efb876c1979311824caadb20900af4cb7dc0bff59f7089`  
		Last Modified: Wed, 24 Feb 2021 20:25:36 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a97284eb2720d25a6d656c6c0f40165967d5109f2b537d74db9e6b1cb8e1c95`  
		Last Modified: Wed, 24 Feb 2021 20:25:36 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
