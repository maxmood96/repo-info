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
$ docker pull influxdb@sha256:9f85bcf46611bd5fc74ffb7a5fc6bd397e9902c2ae232aa8ec56fae02ff2d244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7` - linux; amd64

```console
$ docker pull influxdb@sha256:09b8d5c2c84676af55406ee78b987561f7a682b8f28bbc2eae4aaaacfcc9d886
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122283134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f227ace566f880bfcb21784475d8a27b189e0b733b4ba153cddb0426d36c50d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:07:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 24 Mar 2021 01:30:00 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 24 Mar 2021 01:30:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 24 Mar 2021 01:30:06 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 24 Mar 2021 01:30:06 GMT
EXPOSE 8086
# Wed, 24 Mar 2021 01:30:06 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 01:30:06 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 24 Mar 2021 01:30:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Mar 2021 01:30:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 01:30:07 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25737831bed10fe0362ba56031883977ad22903ddcb50b82c3f74982b1179565`  
		Last Modified: Sat, 13 Mar 2021 10:10:50 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c6b5ee302d0b765dd927ff46fad53ac46d2538403b54e197c0920b66e8918a`  
		Last Modified: Wed, 24 Mar 2021 01:32:24 GMT  
		Size: 61.3 MB (61285145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c50e0f36eb3c7e305c17748895f2d805a3606d40aa3cbace06649204da83133`  
		Last Modified: Wed, 24 Mar 2021 01:32:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90955cf00d21f72f9debbbf4a346772b81aca04d8061f5c5fed1d66aa5761ed6`  
		Last Modified: Wed, 24 Mar 2021 01:32:16 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6173304749b81c581b212a21e6478be74a1836a571b2ac07a574b97473fdbc`  
		Last Modified: Wed, 24 Mar 2021 01:32:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:9d12a904a590ac77ea9aff372401d09dce532054e8ca98805892d7661524df8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113429877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd474d1cd6e40ce751873cbe25df33b31ae574a21a45b495b1101018d1fbe3a`
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
# Wed, 24 Mar 2021 02:35:39 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 24 Mar 2021 02:35:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 24 Mar 2021 02:35:52 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 24 Mar 2021 02:35:53 GMT
EXPOSE 8086
# Wed, 24 Mar 2021 02:35:54 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 02:35:55 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 24 Mar 2021 02:35:55 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Mar 2021 02:35:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 02:35:57 GMT
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
	-	`sha256:45a5aa0bd5f13a7c6efcd98dae37269b67118b79ca8beb52a4d944ff6d9c8366`  
		Last Modified: Wed, 24 Mar 2021 02:36:32 GMT  
		Size: 57.5 MB (57468966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64942160a06f4e69d143e8905c337a610d169558a693a75c84a86b30f4559ddd`  
		Last Modified: Wed, 24 Mar 2021 02:36:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93bc4ded709c5bd7b887b2db812e82a073c1eae3231a921f4a1c423b6ead95e`  
		Last Modified: Wed, 24 Mar 2021 02:36:16 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bf72d1c1d3073a3ca14c292891e6dd5cad50fcbd03b930b9a87a4c2d00a460`  
		Last Modified: Wed, 24 Mar 2021 02:36:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:96336d27a6d79b497491e523664756b49e0a92692bd764651326e2cf70df0e7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114667029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c1f9af0b4a4b7fe7a9baa4ce7f86646e8fbd4eaad48958a8d02f4928755e87`
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
# Wed, 24 Mar 2021 02:13:34 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 24 Mar 2021 02:13:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 24 Mar 2021 02:13:47 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 24 Mar 2021 02:13:48 GMT
EXPOSE 8086
# Wed, 24 Mar 2021 02:13:50 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 02:13:51 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 24 Mar 2021 02:13:52 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Mar 2021 02:13:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 02:13:54 GMT
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
	-	`sha256:ce3d87689f270352166c61950862bba2239a40174b6c88440d903316fecc374c`  
		Last Modified: Wed, 24 Mar 2021 02:14:43 GMT  
		Size: 57.2 MB (57204270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c2cb69a4b40ba3146f9a5183316861f39259f233cc9a8d8b47fb1120de48ca`  
		Last Modified: Wed, 24 Mar 2021 02:14:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34916d339747e2b5e1ef02a57e9435f05b61c84458b7be287dd8e02af4b15419`  
		Last Modified: Wed, 24 Mar 2021 02:14:30 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eae025e582613bbbc98d1db3cc2fc41d1e4c197b080bd191d3b2a1d6ef1bf65`  
		Last Modified: Wed, 24 Mar 2021 02:14:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-alpine`

```console
$ docker pull influxdb@sha256:d4e6f2a369b19c91485931780bf87059b4d2916da9e841078c62cefb7d847858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:19247443733bb8b14cb6cf4e7a2e73e69d187f6aa3e448626735d021652e03d0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65266965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d3cbf9ee782c9ebec7612dbe95244e61694d87350ea469c20a199c3b863331`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:07:34 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Mar 2021 01:30:10 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 24 Mar 2021 01:30:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Mar 2021 01:30:24 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 24 Mar 2021 01:30:25 GMT
EXPOSE 8086
# Wed, 24 Mar 2021 01:30:25 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 01:30:25 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 24 Mar 2021 01:30:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Mar 2021 01:30:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 01:30:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b572d48a3184c0ad742e4c1b3b72687a6f896767590493e8b39cc19f843924`  
		Last Modified: Sat, 13 Mar 2021 10:11:15 GMT  
		Size: 1.4 MB (1430764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d74b7173d11ee9bb3b930caec4c47eef3da13548c0aede3bfb9ca6f4f3d9969`  
		Last Modified: Wed, 24 Mar 2021 01:32:43 GMT  
		Size: 61.0 MB (61034813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a10649c235fa87894ff5b0401db7c13d0d8af180fa329a7430a8930d230569`  
		Last Modified: Wed, 24 Mar 2021 01:32:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857e08e010aed50d817087341fab129dda67b7023f8cae61cc58007c57e4ab74`  
		Last Modified: Wed, 24 Mar 2021 01:32:36 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99dfdcf45de31bde8003512911d561332ce81d4157f7f0334029f39550005b03`  
		Last Modified: Wed, 24 Mar 2021 01:32:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data`

```console
$ docker pull influxdb@sha256:4d019ac729f0134a9bac6271ae001544864875576fe95cd239c14934370b496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:50d970c553462ddd9ac26c5971eccd19aa87d037820210446fb90e036a3fc157
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148947067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5a3328195beac6f2a7fc9e35718237b6f536792371f96ca06b998fb531983a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:07:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 24 Mar 2021 01:30:29 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 24 Mar 2021 01:30:34 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 24 Mar 2021 01:30:34 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 24 Mar 2021 01:30:35 GMT
EXPOSE 8086
# Wed, 24 Mar 2021 01:30:35 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 01:30:35 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 24 Mar 2021 01:30:35 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Mar 2021 01:30:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 01:30:36 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25737831bed10fe0362ba56031883977ad22903ddcb50b82c3f74982b1179565`  
		Last Modified: Sat, 13 Mar 2021 10:10:50 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75c67676994072e49d009e8f194a6963c018cb8bc348e639a5d7204d96ccd94`  
		Last Modified: Wed, 24 Mar 2021 01:33:08 GMT  
		Size: 87.9 MB (87949019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcd9af98ab39fb848124f5af0d1be90af83229802117198680371f07226aa35`  
		Last Modified: Wed, 24 Mar 2021 01:32:56 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7447714bed6e0959b3e2e68ebd3ca68efc92506d1402f0bf00e600dda7aa710b`  
		Last Modified: Wed, 24 Mar 2021 01:32:56 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71b16143e711cf1e8b1860e176727a0a388f55154b141b05ac41d105aad93de`  
		Last Modified: Wed, 24 Mar 2021 01:32:56 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data-alpine`

```console
$ docker pull influxdb@sha256:0f6f162b2f945d91948e9fc9e69a4fd294683a13af1930587bfa16f1eae12414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4ab689adc88a941f91d966e9d8191d5cffa0ff66c2377863a556e107f3728683
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91871040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f9073a5ea6eacf46e6e07bbd14afa41102a21db1cde47759b4cf0d15a99b5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:07:34 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Mar 2021 01:30:39 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 24 Mar 2021 01:30:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Mar 2021 01:30:50 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 24 Mar 2021 01:30:50 GMT
EXPOSE 8086
# Wed, 24 Mar 2021 01:30:50 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 01:30:51 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 24 Mar 2021 01:30:51 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Mar 2021 01:30:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 01:30:51 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b572d48a3184c0ad742e4c1b3b72687a6f896767590493e8b39cc19f843924`  
		Last Modified: Sat, 13 Mar 2021 10:11:15 GMT  
		Size: 1.4 MB (1430764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231d3fdca176701889c539522c70862c369a5fdec8e3ac7fbfe5313312ac2344`  
		Last Modified: Wed, 24 Mar 2021 01:33:32 GMT  
		Size: 87.6 MB (87638830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2902514c5e62dfe508c134c83a5421cd5308c46cb40284306784d259b1c3409e`  
		Last Modified: Wed, 24 Mar 2021 01:33:19 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5700e8a9b66cdb66fb953eecdb7b787a8b011f9126a4a2ffe87823e4577e43`  
		Last Modified: Wed, 24 Mar 2021 01:33:20 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57beab644e5e4f7a98dba21cee981f4922c77c78b06fe1c0939d8c41318c147`  
		Last Modified: Wed, 24 Mar 2021 01:33:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta`

```console
$ docker pull influxdb@sha256:5ba16254a52939d162d7ca6181df96e2b380466a78003358dff9fac38ae48b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:cafd7791b75d9a57bd9b184b3cb30a40f12f10019c3d61758746aa84a77775f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84130472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5078e9777698312956c49382c5b7bd8abbc340c7ac0f6e2a21a6e96491acdb14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:07:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 24 Mar 2021 01:30:29 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 24 Mar 2021 01:30:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 24 Mar 2021 01:30:59 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 24 Mar 2021 01:30:59 GMT
EXPOSE 8091
# Wed, 24 Mar 2021 01:30:59 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 01:30:59 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 24 Mar 2021 01:30:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 01:31:00 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25737831bed10fe0362ba56031883977ad22903ddcb50b82c3f74982b1179565`  
		Last Modified: Sat, 13 Mar 2021 10:10:50 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3680cde6f7c327fdbab072f04ee9195451dad55a4b2b99e7b3020f9927eca0`  
		Last Modified: Wed, 24 Mar 2021 01:33:46 GMT  
		Size: 23.1 MB (23133628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26506064d1d72b45cfb4b348ca5a3b7151d982e3aa4d2ac97f2105cb2e2be00`  
		Last Modified: Wed, 24 Mar 2021 01:33:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e6da2e537c79c5a96da4222b799ed56bba50ef3f775891a4df302962129ee9`  
		Last Modified: Wed, 24 Mar 2021 01:33:46 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta-alpine`

```console
$ docker pull influxdb@sha256:2bd5868aa3d7c79df9f63ed2b3cd1a3d23fd90e1efa0dd2db3da45c8aef0b5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:25f86ce366fbe3d7c12ce3ceb6f218642d64218708b3d6f7d5ecd6cb04f27cdf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27233971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9275fc4f171620576a3ad7540021fd18f55df26c2e87ac328574bce1de003`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:07:34 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Mar 2021 01:30:39 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 24 Mar 2021 01:31:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Mar 2021 01:31:12 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 24 Mar 2021 01:31:12 GMT
EXPOSE 8091
# Wed, 24 Mar 2021 01:31:12 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 01:31:12 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 24 Mar 2021 01:31:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 01:31:13 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b572d48a3184c0ad742e4c1b3b72687a6f896767590493e8b39cc19f843924`  
		Last Modified: Sat, 13 Mar 2021 10:11:15 GMT  
		Size: 1.4 MB (1430764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a52761cca69fb1ae7e8327ba6e9f4bbf4aa45c2ffa66fac284576a3e987c373`  
		Last Modified: Wed, 24 Mar 2021 01:34:00 GMT  
		Size: 23.0 MB (23002963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4509e4a5931257b54778a24b914dbf721a2838c648b3afbfb967ee9f26f0c5b`  
		Last Modified: Wed, 24 Mar 2021 01:33:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f594ab67c2b94563720d8000d4bd8fd73da82a546b07e197ca964ee46cfeb12`  
		Last Modified: Wed, 24 Mar 2021 01:33:57 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11`

```console
$ docker pull influxdb@sha256:9f85bcf46611bd5fc74ffb7a5fc6bd397e9902c2ae232aa8ec56fae02ff2d244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7.11` - linux; amd64

```console
$ docker pull influxdb@sha256:09b8d5c2c84676af55406ee78b987561f7a682b8f28bbc2eae4aaaacfcc9d886
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122283134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f227ace566f880bfcb21784475d8a27b189e0b733b4ba153cddb0426d36c50d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:07:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 24 Mar 2021 01:30:00 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 24 Mar 2021 01:30:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 24 Mar 2021 01:30:06 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 24 Mar 2021 01:30:06 GMT
EXPOSE 8086
# Wed, 24 Mar 2021 01:30:06 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 01:30:06 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 24 Mar 2021 01:30:06 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Mar 2021 01:30:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 01:30:07 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25737831bed10fe0362ba56031883977ad22903ddcb50b82c3f74982b1179565`  
		Last Modified: Sat, 13 Mar 2021 10:10:50 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c6b5ee302d0b765dd927ff46fad53ac46d2538403b54e197c0920b66e8918a`  
		Last Modified: Wed, 24 Mar 2021 01:32:24 GMT  
		Size: 61.3 MB (61285145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c50e0f36eb3c7e305c17748895f2d805a3606d40aa3cbace06649204da83133`  
		Last Modified: Wed, 24 Mar 2021 01:32:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90955cf00d21f72f9debbbf4a346772b81aca04d8061f5c5fed1d66aa5761ed6`  
		Last Modified: Wed, 24 Mar 2021 01:32:16 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6173304749b81c581b212a21e6478be74a1836a571b2ac07a574b97473fdbc`  
		Last Modified: Wed, 24 Mar 2021 01:32:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.11` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:9d12a904a590ac77ea9aff372401d09dce532054e8ca98805892d7661524df8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113429877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd474d1cd6e40ce751873cbe25df33b31ae574a21a45b495b1101018d1fbe3a`
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
# Wed, 24 Mar 2021 02:35:39 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 24 Mar 2021 02:35:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 24 Mar 2021 02:35:52 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 24 Mar 2021 02:35:53 GMT
EXPOSE 8086
# Wed, 24 Mar 2021 02:35:54 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 02:35:55 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 24 Mar 2021 02:35:55 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Mar 2021 02:35:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 02:35:57 GMT
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
	-	`sha256:45a5aa0bd5f13a7c6efcd98dae37269b67118b79ca8beb52a4d944ff6d9c8366`  
		Last Modified: Wed, 24 Mar 2021 02:36:32 GMT  
		Size: 57.5 MB (57468966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64942160a06f4e69d143e8905c337a610d169558a693a75c84a86b30f4559ddd`  
		Last Modified: Wed, 24 Mar 2021 02:36:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93bc4ded709c5bd7b887b2db812e82a073c1eae3231a921f4a1c423b6ead95e`  
		Last Modified: Wed, 24 Mar 2021 02:36:16 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bf72d1c1d3073a3ca14c292891e6dd5cad50fcbd03b930b9a87a4c2d00a460`  
		Last Modified: Wed, 24 Mar 2021 02:36:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:96336d27a6d79b497491e523664756b49e0a92692bd764651326e2cf70df0e7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114667029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c1f9af0b4a4b7fe7a9baa4ce7f86646e8fbd4eaad48958a8d02f4928755e87`
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
# Wed, 24 Mar 2021 02:13:34 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 24 Mar 2021 02:13:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 24 Mar 2021 02:13:47 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 24 Mar 2021 02:13:48 GMT
EXPOSE 8086
# Wed, 24 Mar 2021 02:13:50 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 02:13:51 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 24 Mar 2021 02:13:52 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Mar 2021 02:13:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 02:13:54 GMT
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
	-	`sha256:ce3d87689f270352166c61950862bba2239a40174b6c88440d903316fecc374c`  
		Last Modified: Wed, 24 Mar 2021 02:14:43 GMT  
		Size: 57.2 MB (57204270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c2cb69a4b40ba3146f9a5183316861f39259f233cc9a8d8b47fb1120de48ca`  
		Last Modified: Wed, 24 Mar 2021 02:14:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34916d339747e2b5e1ef02a57e9435f05b61c84458b7be287dd8e02af4b15419`  
		Last Modified: Wed, 24 Mar 2021 02:14:30 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eae025e582613bbbc98d1db3cc2fc41d1e4c197b080bd191d3b2a1d6ef1bf65`  
		Last Modified: Wed, 24 Mar 2021 02:14:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-alpine`

```console
$ docker pull influxdb@sha256:d4e6f2a369b19c91485931780bf87059b4d2916da9e841078c62cefb7d847858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:19247443733bb8b14cb6cf4e7a2e73e69d187f6aa3e448626735d021652e03d0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65266965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d3cbf9ee782c9ebec7612dbe95244e61694d87350ea469c20a199c3b863331`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:07:34 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Mar 2021 01:30:10 GMT
ENV INFLUXDB_VERSION=1.7.11
# Wed, 24 Mar 2021 01:30:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Mar 2021 01:30:24 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 24 Mar 2021 01:30:25 GMT
EXPOSE 8086
# Wed, 24 Mar 2021 01:30:25 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 01:30:25 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 24 Mar 2021 01:30:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Mar 2021 01:30:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 01:30:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b572d48a3184c0ad742e4c1b3b72687a6f896767590493e8b39cc19f843924`  
		Last Modified: Sat, 13 Mar 2021 10:11:15 GMT  
		Size: 1.4 MB (1430764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d74b7173d11ee9bb3b930caec4c47eef3da13548c0aede3bfb9ca6f4f3d9969`  
		Last Modified: Wed, 24 Mar 2021 01:32:43 GMT  
		Size: 61.0 MB (61034813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a10649c235fa87894ff5b0401db7c13d0d8af180fa329a7430a8930d230569`  
		Last Modified: Wed, 24 Mar 2021 01:32:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857e08e010aed50d817087341fab129dda67b7023f8cae61cc58007c57e4ab74`  
		Last Modified: Wed, 24 Mar 2021 01:32:36 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99dfdcf45de31bde8003512911d561332ce81d4157f7f0334029f39550005b03`  
		Last Modified: Wed, 24 Mar 2021 01:32:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-data`

```console
$ docker pull influxdb@sha256:4d019ac729f0134a9bac6271ae001544864875576fe95cd239c14934370b496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:50d970c553462ddd9ac26c5971eccd19aa87d037820210446fb90e036a3fc157
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148947067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5a3328195beac6f2a7fc9e35718237b6f536792371f96ca06b998fb531983a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:07:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 24 Mar 2021 01:30:29 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 24 Mar 2021 01:30:34 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 24 Mar 2021 01:30:34 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 24 Mar 2021 01:30:35 GMT
EXPOSE 8086
# Wed, 24 Mar 2021 01:30:35 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 01:30:35 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 24 Mar 2021 01:30:35 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Mar 2021 01:30:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 01:30:36 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25737831bed10fe0362ba56031883977ad22903ddcb50b82c3f74982b1179565`  
		Last Modified: Sat, 13 Mar 2021 10:10:50 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75c67676994072e49d009e8f194a6963c018cb8bc348e639a5d7204d96ccd94`  
		Last Modified: Wed, 24 Mar 2021 01:33:08 GMT  
		Size: 87.9 MB (87949019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcd9af98ab39fb848124f5af0d1be90af83229802117198680371f07226aa35`  
		Last Modified: Wed, 24 Mar 2021 01:32:56 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7447714bed6e0959b3e2e68ebd3ca68efc92506d1402f0bf00e600dda7aa710b`  
		Last Modified: Wed, 24 Mar 2021 01:32:56 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71b16143e711cf1e8b1860e176727a0a388f55154b141b05ac41d105aad93de`  
		Last Modified: Wed, 24 Mar 2021 01:32:56 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-data-alpine`

```console
$ docker pull influxdb@sha256:0f6f162b2f945d91948e9fc9e69a4fd294683a13af1930587bfa16f1eae12414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4ab689adc88a941f91d966e9d8191d5cffa0ff66c2377863a556e107f3728683
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91871040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f9073a5ea6eacf46e6e07bbd14afa41102a21db1cde47759b4cf0d15a99b5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:07:34 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Mar 2021 01:30:39 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 24 Mar 2021 01:30:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Mar 2021 01:30:50 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 24 Mar 2021 01:30:50 GMT
EXPOSE 8086
# Wed, 24 Mar 2021 01:30:50 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 01:30:51 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 24 Mar 2021 01:30:51 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 24 Mar 2021 01:30:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 01:30:51 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b572d48a3184c0ad742e4c1b3b72687a6f896767590493e8b39cc19f843924`  
		Last Modified: Sat, 13 Mar 2021 10:11:15 GMT  
		Size: 1.4 MB (1430764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231d3fdca176701889c539522c70862c369a5fdec8e3ac7fbfe5313312ac2344`  
		Last Modified: Wed, 24 Mar 2021 01:33:32 GMT  
		Size: 87.6 MB (87638830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2902514c5e62dfe508c134c83a5421cd5308c46cb40284306784d259b1c3409e`  
		Last Modified: Wed, 24 Mar 2021 01:33:19 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5700e8a9b66cdb66fb953eecdb7b787a8b011f9126a4a2ffe87823e4577e43`  
		Last Modified: Wed, 24 Mar 2021 01:33:20 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57beab644e5e4f7a98dba21cee981f4922c77c78b06fe1c0939d8c41318c147`  
		Last Modified: Wed, 24 Mar 2021 01:33:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-meta`

```console
$ docker pull influxdb@sha256:5ba16254a52939d162d7ca6181df96e2b380466a78003358dff9fac38ae48b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:cafd7791b75d9a57bd9b184b3cb30a40f12f10019c3d61758746aa84a77775f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84130472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5078e9777698312956c49382c5b7bd8abbc340c7ac0f6e2a21a6e96491acdb14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:07:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 24 Mar 2021 01:30:29 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 24 Mar 2021 01:30:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 24 Mar 2021 01:30:59 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 24 Mar 2021 01:30:59 GMT
EXPOSE 8091
# Wed, 24 Mar 2021 01:30:59 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 01:30:59 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 24 Mar 2021 01:30:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 01:31:00 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25737831bed10fe0362ba56031883977ad22903ddcb50b82c3f74982b1179565`  
		Last Modified: Sat, 13 Mar 2021 10:10:50 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3680cde6f7c327fdbab072f04ee9195451dad55a4b2b99e7b3020f9927eca0`  
		Last Modified: Wed, 24 Mar 2021 01:33:46 GMT  
		Size: 23.1 MB (23133628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26506064d1d72b45cfb4b348ca5a3b7151d982e3aa4d2ac97f2105cb2e2be00`  
		Last Modified: Wed, 24 Mar 2021 01:33:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e6da2e537c79c5a96da4222b799ed56bba50ef3f775891a4df302962129ee9`  
		Last Modified: Wed, 24 Mar 2021 01:33:46 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.11-meta-alpine`

```console
$ docker pull influxdb@sha256:2bd5868aa3d7c79df9f63ed2b3cd1a3d23fd90e1efa0dd2db3da45c8aef0b5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:25f86ce366fbe3d7c12ce3ceb6f218642d64218708b3d6f7d5ecd6cb04f27cdf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27233971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9275fc4f171620576a3ad7540021fd18f55df26c2e87ac328574bce1de003`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:07:34 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 24 Mar 2021 01:30:39 GMT
ENV INFLUXDB_VERSION=1.7.11-c1.7.11
# Wed, 24 Mar 2021 01:31:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Mar 2021 01:31:12 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 24 Mar 2021 01:31:12 GMT
EXPOSE 8091
# Wed, 24 Mar 2021 01:31:12 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Mar 2021 01:31:12 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 24 Mar 2021 01:31:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Mar 2021 01:31:13 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b572d48a3184c0ad742e4c1b3b72687a6f896767590493e8b39cc19f843924`  
		Last Modified: Sat, 13 Mar 2021 10:11:15 GMT  
		Size: 1.4 MB (1430764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a52761cca69fb1ae7e8327ba6e9f4bbf4aa45c2ffa66fac284576a3e987c373`  
		Last Modified: Wed, 24 Mar 2021 01:34:00 GMT  
		Size: 23.0 MB (23002963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4509e4a5931257b54778a24b914dbf721a2838c648b3afbfb967ee9f26f0c5b`  
		Last Modified: Wed, 24 Mar 2021 01:33:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f594ab67c2b94563720d8000d4bd8fd73da82a546b07e197ca964ee46cfeb12`  
		Last Modified: Wed, 24 Mar 2021 01:33:57 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8`

```console
$ docker pull influxdb@sha256:9e548c65c144cf461d47f565d337379b2d48b3119660d1e5f8667cbb7af76e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8` - linux; amd64

```console
$ docker pull influxdb@sha256:b730caa46ce7c24abe98db26138ef53b3edc3005c5e1a9cce2be8a570fe26b45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125964733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2862e581f93c3e3bd2259ab1dd5c854e709cd4ff190aeb00574505a639ee2ffe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:07:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 13 Mar 2021 10:08:37 GMT
ENV INFLUXDB_VERSION=1.8.4
# Sat, 13 Mar 2021 10:08:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sat, 13 Mar 2021 10:08:44 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 13 Mar 2021 10:08:44 GMT
EXPOSE 8086
# Sat, 13 Mar 2021 10:08:44 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:08:44 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:08:45 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 13 Mar 2021 10:08:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:08:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25737831bed10fe0362ba56031883977ad22903ddcb50b82c3f74982b1179565`  
		Last Modified: Sat, 13 Mar 2021 10:10:50 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb2cc840df9cab16628be5c124fef4254629549021e424958e0ccc5611df75a`  
		Last Modified: Sat, 13 Mar 2021 10:13:09 GMT  
		Size: 65.0 MB (64966742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc38168907bdee3cf7eb67a49531ffd58bc50e6149f8e199677f3792d0c3cc`  
		Last Modified: Sat, 13 Mar 2021 10:13:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641ddd68a92a1ece1ebf215d2088de75bf689f607f705b0ebab3be9558a72acb`  
		Last Modified: Sat, 13 Mar 2021 10:13:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f82b1e82ba21d2242a790e569b4b5828426bf39d3ecd20110742ab171f88628`  
		Last Modified: Sat, 13 Mar 2021 10:13:01 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull influxdb@sha256:15109d72c00890f6d6a9e71c2851e0b1a82626d71551427557e99f75ad9d4e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f4d6133a9e38c511e3176a83ce233a8ff672fe0c52f35d51f75f29e120406500
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68938796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aad43c31bcf530a7c4cb9210551739b41b1652cb8704429e8dd95a171fdd4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:07:34 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 13 Mar 2021 10:08:48 GMT
ENV INFLUXDB_VERSION=1.8.4
# Sat, 13 Mar 2021 10:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 13 Mar 2021 10:08:54 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 13 Mar 2021 10:08:55 GMT
EXPOSE 8086
# Sat, 13 Mar 2021 10:08:55 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:08:55 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:08:55 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 13 Mar 2021 10:08:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:08:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b572d48a3184c0ad742e4c1b3b72687a6f896767590493e8b39cc19f843924`  
		Last Modified: Sat, 13 Mar 2021 10:11:15 GMT  
		Size: 1.4 MB (1430764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f519c1164f6024a249b425c7977363d0078768a7d3571481a1f0a0d67b2897`  
		Last Modified: Sat, 13 Mar 2021 10:13:34 GMT  
		Size: 64.7 MB (64706646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a286293fe407d8ee31bb91a778a15c47b8219dcf4258ae3ab4a564d40751a961`  
		Last Modified: Sat, 13 Mar 2021 10:13:20 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22689a6aee5944cddfeb418dbb85e19584f17a2cf25e5847b33254e8cb27606b`  
		Last Modified: Sat, 13 Mar 2021 10:13:19 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdb16557381e4ba91ef5dec2b57b4e1a757b3219ec95b3dfb55565ad0492c57`  
		Last Modified: Sat, 13 Mar 2021 10:13:19 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data`

```console
$ docker pull influxdb@sha256:1a848bd4ee1a8a12220886b2213e8f41f8518a8005e53508c8c4827a2d190978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data` - linux; amd64

```console
$ docker pull influxdb@sha256:ecc951feb2a2c357b9a3460c6a8dc8eeaaf38e6ecc4a60c194a150aec92b82fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126794466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ff7f6acf2095904719d11c3f266f95c1b1fc1ada6cfa5ec251e6bea6e89999`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:07:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 13 Mar 2021 10:09:00 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 13 Mar 2021 10:09:06 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 13 Mar 2021 10:09:07 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 13 Mar 2021 10:09:07 GMT
EXPOSE 8086
# Sat, 13 Mar 2021 10:09:07 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:09:07 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:09:07 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 13 Mar 2021 10:09:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:09:08 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25737831bed10fe0362ba56031883977ad22903ddcb50b82c3f74982b1179565`  
		Last Modified: Sat, 13 Mar 2021 10:10:50 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18576c011e4fba451270d363e409c97b372b9fdf2fd235ce41bc78e9a817535d`  
		Last Modified: Sat, 13 Mar 2021 10:13:54 GMT  
		Size: 65.8 MB (65796421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141c9c3bb5a126ba7762bf6e8490158429fced829fae9e8e8474e4d13ae50a57`  
		Last Modified: Sat, 13 Mar 2021 10:13:45 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7e88aff98fdcb49c6eb4d996f4a69041cd2591c7503d317aeaf2a44e8404cd`  
		Last Modified: Sat, 13 Mar 2021 10:13:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5267ed226902fef8eb8572d171b1efcda36c633f8bfe60c498a27afe764013`  
		Last Modified: Sat, 13 Mar 2021 10:13:45 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-data-alpine`

```console
$ docker pull influxdb@sha256:72201ba79e44315cac8944621549d40e8ba8350b6b00917eea49b8f88e7e3dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:33519de466913e487be9e1f02af9e6e849e05849e2137cb7d09d7ebcf016839a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69772902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e662be1d19d8a9bd697d6438b0908a800d0a310d4bd04165e68ec05ffd0691a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:07:34 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 13 Mar 2021 10:09:11 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 13 Mar 2021 10:09:19 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 13 Mar 2021 10:09:19 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 13 Mar 2021 10:09:20 GMT
EXPOSE 8086
# Sat, 13 Mar 2021 10:09:20 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:09:20 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:09:20 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 13 Mar 2021 10:09:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:09:21 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b572d48a3184c0ad742e4c1b3b72687a6f896767590493e8b39cc19f843924`  
		Last Modified: Sat, 13 Mar 2021 10:11:15 GMT  
		Size: 1.4 MB (1430764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef23fd2718fb492806f24481d4bbef97011a461dc36cd3657567662996c35a5`  
		Last Modified: Sat, 13 Mar 2021 10:14:17 GMT  
		Size: 65.5 MB (65540696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d750db74011b4bd6cdadca668da48e27a2316e6218fd046f57d3c30fa7308ba6`  
		Last Modified: Sat, 13 Mar 2021 10:14:08 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46ffac5dbd2cc362451f8274fb25f20aa672e9668a4e09e3fe9d7c799fad126`  
		Last Modified: Sat, 13 Mar 2021 10:14:08 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8683186eb48f43e6644290a19d3c83098a730a4ba1a1b3119af598dc30cfd8`  
		Last Modified: Sat, 13 Mar 2021 10:14:08 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta`

```console
$ docker pull influxdb@sha256:e8f7332ae9bf4935cd55651cb66df86c458e640f7d31a4f693c2addf64a77336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c34a2ae90ea1ad09e67c0b70494356874af68d53553073f4eb24e95aecdb24fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83863091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911cfe59b714c4ed06169ca6b8c633eeb32f8b84c995046a15896abc7b9ecbd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:07:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 13 Mar 2021 10:09:00 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 13 Mar 2021 10:09:28 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 13 Mar 2021 10:09:28 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 13 Mar 2021 10:09:29 GMT
EXPOSE 8091
# Sat, 13 Mar 2021 10:09:29 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:09:29 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:09:29 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25737831bed10fe0362ba56031883977ad22903ddcb50b82c3f74982b1179565`  
		Last Modified: Sat, 13 Mar 2021 10:10:50 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca679c2c6e2a4ce57f63ba3dcb941dde4764c229295240ac47383c0ab2d58d53`  
		Last Modified: Sat, 13 Mar 2021 10:14:39 GMT  
		Size: 22.9 MB (22866247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce7a1017fc271c11da61ca509b5dac1881c8032f0bf0b7d5e2c3b57ac32201e`  
		Last Modified: Sat, 13 Mar 2021 10:14:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cebe14b4929afdae376a7ce1883ea97e600d4e9d35aa0c347602e0eefc8305`  
		Last Modified: Sat, 13 Mar 2021 10:14:35 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8-meta-alpine`

```console
$ docker pull influxdb@sha256:f5e194de56745fc72bb1bb460ed88f59023c65005403117c4b0694f6531c89ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:87dd9e771b3d8b514f0970ce5d82f84edf65d681d5482983b3598f58de3d4c5a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26966388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acafa701406a7367f7215f4368a8730c24d0c048cd2bbfcbfdfa134548ef7c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:07:34 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 13 Mar 2021 10:09:11 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 13 Mar 2021 10:09:37 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 13 Mar 2021 10:09:37 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 13 Mar 2021 10:09:37 GMT
EXPOSE 8091
# Sat, 13 Mar 2021 10:09:37 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:09:38 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:09:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:09:38 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b572d48a3184c0ad742e4c1b3b72687a6f896767590493e8b39cc19f843924`  
		Last Modified: Sat, 13 Mar 2021 10:11:15 GMT  
		Size: 1.4 MB (1430764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d519f7d0d8e6ebd6e8856db8a34338ab36f21a9f7750c061f728f3f7faf4b`  
		Last Modified: Sat, 13 Mar 2021 10:14:56 GMT  
		Size: 22.7 MB (22735383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820d21cf4e4c41228969e4da796d51abb8f7bf7379ce56380ae57f321336700f`  
		Last Modified: Sat, 13 Mar 2021 10:14:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3eafd806e9fb49033f42ce9dd548448f5fb429b0e7070c800b0cb5539273d4`  
		Last Modified: Sat, 13 Mar 2021 10:14:53 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-data`

```console
$ docker pull influxdb@sha256:1a848bd4ee1a8a12220886b2213e8f41f8518a8005e53508c8c4827a2d190978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data` - linux; amd64

```console
$ docker pull influxdb@sha256:ecc951feb2a2c357b9a3460c6a8dc8eeaaf38e6ecc4a60c194a150aec92b82fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126794466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ff7f6acf2095904719d11c3f266f95c1b1fc1ada6cfa5ec251e6bea6e89999`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:07:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 13 Mar 2021 10:09:00 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 13 Mar 2021 10:09:06 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 13 Mar 2021 10:09:07 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 13 Mar 2021 10:09:07 GMT
EXPOSE 8086
# Sat, 13 Mar 2021 10:09:07 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:09:07 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:09:07 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 13 Mar 2021 10:09:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:09:08 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25737831bed10fe0362ba56031883977ad22903ddcb50b82c3f74982b1179565`  
		Last Modified: Sat, 13 Mar 2021 10:10:50 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18576c011e4fba451270d363e409c97b372b9fdf2fd235ce41bc78e9a817535d`  
		Last Modified: Sat, 13 Mar 2021 10:13:54 GMT  
		Size: 65.8 MB (65796421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141c9c3bb5a126ba7762bf6e8490158429fced829fae9e8e8474e4d13ae50a57`  
		Last Modified: Sat, 13 Mar 2021 10:13:45 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7e88aff98fdcb49c6eb4d996f4a69041cd2591c7503d317aeaf2a44e8404cd`  
		Last Modified: Sat, 13 Mar 2021 10:13:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5267ed226902fef8eb8572d171b1efcda36c633f8bfe60c498a27afe764013`  
		Last Modified: Sat, 13 Mar 2021 10:13:45 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-data-alpine`

```console
$ docker pull influxdb@sha256:72201ba79e44315cac8944621549d40e8ba8350b6b00917eea49b8f88e7e3dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:33519de466913e487be9e1f02af9e6e849e05849e2137cb7d09d7ebcf016839a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69772902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e662be1d19d8a9bd697d6438b0908a800d0a310d4bd04165e68ec05ffd0691a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:07:34 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 13 Mar 2021 10:09:11 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 13 Mar 2021 10:09:19 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 13 Mar 2021 10:09:19 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 13 Mar 2021 10:09:20 GMT
EXPOSE 8086
# Sat, 13 Mar 2021 10:09:20 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:09:20 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:09:20 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 13 Mar 2021 10:09:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:09:21 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b572d48a3184c0ad742e4c1b3b72687a6f896767590493e8b39cc19f843924`  
		Last Modified: Sat, 13 Mar 2021 10:11:15 GMT  
		Size: 1.4 MB (1430764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef23fd2718fb492806f24481d4bbef97011a461dc36cd3657567662996c35a5`  
		Last Modified: Sat, 13 Mar 2021 10:14:17 GMT  
		Size: 65.5 MB (65540696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d750db74011b4bd6cdadca668da48e27a2316e6218fd046f57d3c30fa7308ba6`  
		Last Modified: Sat, 13 Mar 2021 10:14:08 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46ffac5dbd2cc362451f8274fb25f20aa672e9668a4e09e3fe9d7c799fad126`  
		Last Modified: Sat, 13 Mar 2021 10:14:08 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8683186eb48f43e6644290a19d3c83098a730a4ba1a1b3119af598dc30cfd8`  
		Last Modified: Sat, 13 Mar 2021 10:14:08 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-meta`

```console
$ docker pull influxdb@sha256:e8f7332ae9bf4935cd55651cb66df86c458e640f7d31a4f693c2addf64a77336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c34a2ae90ea1ad09e67c0b70494356874af68d53553073f4eb24e95aecdb24fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83863091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911cfe59b714c4ed06169ca6b8c633eeb32f8b84c995046a15896abc7b9ecbd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:07:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 13 Mar 2021 10:09:00 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 13 Mar 2021 10:09:28 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 13 Mar 2021 10:09:28 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 13 Mar 2021 10:09:29 GMT
EXPOSE 8091
# Sat, 13 Mar 2021 10:09:29 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:09:29 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:09:29 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25737831bed10fe0362ba56031883977ad22903ddcb50b82c3f74982b1179565`  
		Last Modified: Sat, 13 Mar 2021 10:10:50 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca679c2c6e2a4ce57f63ba3dcb941dde4764c229295240ac47383c0ab2d58d53`  
		Last Modified: Sat, 13 Mar 2021 10:14:39 GMT  
		Size: 22.9 MB (22866247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce7a1017fc271c11da61ca509b5dac1881c8032f0bf0b7d5e2c3b57ac32201e`  
		Last Modified: Sat, 13 Mar 2021 10:14:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cebe14b4929afdae376a7ce1883ea97e600d4e9d35aa0c347602e0eefc8305`  
		Last Modified: Sat, 13 Mar 2021 10:14:35 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.3-meta-alpine`

```console
$ docker pull influxdb@sha256:f5e194de56745fc72bb1bb460ed88f59023c65005403117c4b0694f6531c89ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.3-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:87dd9e771b3d8b514f0970ce5d82f84edf65d681d5482983b3598f58de3d4c5a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26966388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acafa701406a7367f7215f4368a8730c24d0c048cd2bbfcbfdfa134548ef7c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:07:34 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 13 Mar 2021 10:09:11 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 13 Mar 2021 10:09:37 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 13 Mar 2021 10:09:37 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 13 Mar 2021 10:09:37 GMT
EXPOSE 8091
# Sat, 13 Mar 2021 10:09:37 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:09:38 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:09:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:09:38 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b572d48a3184c0ad742e4c1b3b72687a6f896767590493e8b39cc19f843924`  
		Last Modified: Sat, 13 Mar 2021 10:11:15 GMT  
		Size: 1.4 MB (1430764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d519f7d0d8e6ebd6e8856db8a34338ab36f21a9f7750c061f728f3f7faf4b`  
		Last Modified: Sat, 13 Mar 2021 10:14:56 GMT  
		Size: 22.7 MB (22735383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820d21cf4e4c41228969e4da796d51abb8f7bf7379ce56380ae57f321336700f`  
		Last Modified: Sat, 13 Mar 2021 10:14:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3eafd806e9fb49033f42ce9dd548448f5fb429b0e7070c800b0cb5539273d4`  
		Last Modified: Sat, 13 Mar 2021 10:14:53 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.8.4`

```console
$ docker pull influxdb@sha256:9e548c65c144cf461d47f565d337379b2d48b3119660d1e5f8667cbb7af76e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.8.4` - linux; amd64

```console
$ docker pull influxdb@sha256:b730caa46ce7c24abe98db26138ef53b3edc3005c5e1a9cce2be8a570fe26b45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125964733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2862e581f93c3e3bd2259ab1dd5c854e709cd4ff190aeb00574505a639ee2ffe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:07:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 13 Mar 2021 10:08:37 GMT
ENV INFLUXDB_VERSION=1.8.4
# Sat, 13 Mar 2021 10:08:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sat, 13 Mar 2021 10:08:44 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 13 Mar 2021 10:08:44 GMT
EXPOSE 8086
# Sat, 13 Mar 2021 10:08:44 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:08:44 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:08:45 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 13 Mar 2021 10:08:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:08:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25737831bed10fe0362ba56031883977ad22903ddcb50b82c3f74982b1179565`  
		Last Modified: Sat, 13 Mar 2021 10:10:50 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb2cc840df9cab16628be5c124fef4254629549021e424958e0ccc5611df75a`  
		Last Modified: Sat, 13 Mar 2021 10:13:09 GMT  
		Size: 65.0 MB (64966742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc38168907bdee3cf7eb67a49531ffd58bc50e6149f8e199677f3792d0c3cc`  
		Last Modified: Sat, 13 Mar 2021 10:13:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641ddd68a92a1ece1ebf215d2088de75bf689f607f705b0ebab3be9558a72acb`  
		Last Modified: Sat, 13 Mar 2021 10:13:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f82b1e82ba21d2242a790e569b4b5828426bf39d3ecd20110742ab171f88628`  
		Last Modified: Sat, 13 Mar 2021 10:13:01 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull influxdb@sha256:15109d72c00890f6d6a9e71c2851e0b1a82626d71551427557e99f75ad9d4e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.8.4-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f4d6133a9e38c511e3176a83ce233a8ff672fe0c52f35d51f75f29e120406500
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68938796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aad43c31bcf530a7c4cb9210551739b41b1652cb8704429e8dd95a171fdd4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:07:34 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 13 Mar 2021 10:08:48 GMT
ENV INFLUXDB_VERSION=1.8.4
# Sat, 13 Mar 2021 10:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 13 Mar 2021 10:08:54 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 13 Mar 2021 10:08:55 GMT
EXPOSE 8086
# Sat, 13 Mar 2021 10:08:55 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:08:55 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:08:55 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 13 Mar 2021 10:08:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:08:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b572d48a3184c0ad742e4c1b3b72687a6f896767590493e8b39cc19f843924`  
		Last Modified: Sat, 13 Mar 2021 10:11:15 GMT  
		Size: 1.4 MB (1430764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f519c1164f6024a249b425c7977363d0078768a7d3571481a1f0a0d67b2897`  
		Last Modified: Sat, 13 Mar 2021 10:13:34 GMT  
		Size: 64.7 MB (64706646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a286293fe407d8ee31bb91a778a15c47b8219dcf4258ae3ab4a564d40751a961`  
		Last Modified: Sat, 13 Mar 2021 10:13:20 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22689a6aee5944cddfeb418dbb85e19584f17a2cf25e5847b33254e8cb27606b`  
		Last Modified: Sat, 13 Mar 2021 10:13:19 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdb16557381e4ba91ef5dec2b57b4e1a757b3219ec95b3dfb55565ad0492c57`  
		Last Modified: Sat, 13 Mar 2021 10:13:19 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0`

```console
$ docker pull influxdb@sha256:f84d9dc486e5933fdca12c66dc945101b21e356c2f5838e4ac42b355c41813ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0` - linux; amd64

```console
$ docker pull influxdb@sha256:3d8220100eebbe8163daa1ec3112ea85352916e4e61e4eed3d3c3f54b54e567e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116198808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f9150a5e7f1ab4d6149ac0622fbe536a0a1dedae2bfd88b9dd2680ebeebbc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:27 GMT
ADD file:575bf0d00d72810609a4118728923f11625b43de536352fe69a341086e4ebfd1 in / 
# Fri, 12 Mar 2021 02:20:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:49:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:49:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:09:42 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 13 Mar 2021 10:09:42 GMT
ENV GOSU_VER=1.12
# Sat, 13 Mar 2021 10:09:46 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Sat, 13 Mar 2021 10:09:46 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 17 Mar 2021 18:23:06 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 17 Mar 2021 18:23:08 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 17 Mar 2021 18:23:08 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 17 Mar 2021 18:23:08 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 17 Mar 2021 18:23:08 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 17 Mar 2021 18:23:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Mar 2021 18:23:09 GMT
CMD ["influxd"]
# Wed, 17 Mar 2021 18:23:09 GMT
EXPOSE 8086
# Wed, 17 Mar 2021 18:23:09 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 17 Mar 2021 18:23:09 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:e22122b926a1a853d61887fa35c3fe53e05ee7dc0f2f488936dc9838bd0e230d`  
		Last Modified: Fri, 12 Mar 2021 02:25:38 GMT  
		Size: 50.4 MB (50400353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e09ae83733d697508e34827538cc0129b8719b85db943041c5d37287bcb81`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 7.8 MB (7832474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e319e3daef68c36099bf3b534377a78d373f67bde3d156119c2463f5fe133ac5`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 10.0 MB (9997147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b330fcd093c9f406b78dbb3eb30ba647453e21a6f98248db555edbc9b4b05c14`  
		Last Modified: Sat, 13 Mar 2021 10:15:13 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5fbd072b21506c45c169f90c463ab8dc87270ade79660a625bae429508fe4b`  
		Last Modified: Sat, 13 Mar 2021 10:15:10 GMT  
		Size: 961.0 KB (960992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a11e9877203e1cb0d2d341484c3dd53093bbe1c47563ca5e9b209eaefe60640`  
		Last Modified: Wed, 17 Mar 2021 18:24:29 GMT  
		Size: 47.0 MB (47001580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ebd202fc31a7821bf65c6b05f8e83afa333314c353343142be1e9f9be2dd91`  
		Last Modified: Wed, 17 Mar 2021 18:24:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3679fc97953d82c23817aeb72bd0c1ae75ead527692a8b4921a9d2382e7322`  
		Last Modified: Wed, 17 Mar 2021 18:24:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3e9aa12abff71c52d71f001a63c1e8608a1f76d61bdd778ce58f1fd86f6f4c`  
		Last Modified: Wed, 17 Mar 2021 18:24:22 GMT  
		Size: 3.9 KB (3922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:52fe997276608db793e9e9616e1548eb9815dff6539cbc3e8bda79f88449a3c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112181150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e0140e11122b7680b0f65178b63cced4f963497d66b1a953be99045f8ffe9b`
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
# Wed, 17 Mar 2021 17:41:18 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 17 Mar 2021 17:41:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 17 Mar 2021 17:41:21 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 17 Mar 2021 17:41:22 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 17 Mar 2021 17:41:23 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 17 Mar 2021 17:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Mar 2021 17:41:25 GMT
CMD ["influxd"]
# Wed, 17 Mar 2021 17:41:25 GMT
EXPOSE 8086
# Wed, 17 Mar 2021 17:41:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 17 Mar 2021 17:41:27 GMT
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
	-	`sha256:e6bd2f6270db099d4e06c87835dcd290765c59381fbc9523ec7f2038ab5328a0`  
		Last Modified: Wed, 17 Mar 2021 17:42:28 GMT  
		Size: 44.4 MB (44403990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde6be645ea4f12c5bf48eced01d7eff45d3b9807dc0ccc11c6218e7b25fd607`  
		Last Modified: Wed, 17 Mar 2021 17:42:19 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa62b33c5c36df63a4c674a8dcd0864a4deda5d635e72958d2ca7b7ba64c293`  
		Last Modified: Wed, 17 Mar 2021 17:42:19 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a084e7539f63b191fd5fb9c5f0d21f1038f1216cac7c9a967cefd0ce783eb00`  
		Last Modified: Wed, 17 Mar 2021 17:42:19 GMT  
		Size: 3.9 KB (3926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0-alpine`

```console
$ docker pull influxdb@sha256:140cff530782b7f380a02d55bc9325c61b19f887824d54248c86a449393aa2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:55e9c2a38b9013fae5faec4e97f5d4c4b54380285ab84f3a8862ee62e3dec63e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60480698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3279de7243f7292ca2a9ebd4fabbf53720ae84442f28b4d9bd25fa3b29ed685f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 13 Mar 2021 04:22:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:09:59 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Sat, 13 Mar 2021 10:10:00 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 13 Mar 2021 10:10:00 GMT
ENV GOSU_VER=1.12
# Wed, 17 Mar 2021 18:23:16 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Mar 2021 18:23:16 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 17 Mar 2021 18:23:22 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 17 Mar 2021 18:23:23 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 17 Mar 2021 18:23:23 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 17 Mar 2021 18:23:24 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 17 Mar 2021 18:23:24 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 17 Mar 2021 18:23:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Mar 2021 18:23:24 GMT
CMD ["influxd"]
# Wed, 17 Mar 2021 18:23:24 GMT
EXPOSE 8086
# Wed, 17 Mar 2021 18:23:25 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 17 Mar 2021 18:23:25 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf3a7b369ab361149a2966cf437a5fd4730d81746d4aa29dd71ecbed71765da`  
		Last Modified: Sat, 13 Mar 2021 04:23:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81573d157ce7aceb135335ef386f0405887d0bdd187e4fee5287cf82de3b32`  
		Last Modified: Sat, 13 Mar 2021 10:15:35 GMT  
		Size: 9.7 MB (9700963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4832d1f6325f85d19c79a40d3d1b880fa86fdf04dea68d5e718abc3d53fa2c5`  
		Last Modified: Sat, 13 Mar 2021 10:15:33 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce58b7cf68cf881fec31d70740252c1d2d7ddb55db6461bd6e0c1d4cd654351`  
		Last Modified: Wed, 17 Mar 2021 18:24:44 GMT  
		Size: 960.6 KB (960620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f44e70b13ed0efcbfd808ae158fa6b6c4af768a66a456a9cbaba1496d21f9d`  
		Last Modified: Wed, 17 Mar 2021 18:24:55 GMT  
		Size: 47.0 MB (47001589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3013020617680ac7db9d3f556a52622fbe98169ac8f3bc7cb1e265c6a94ddb`  
		Last Modified: Wed, 17 Mar 2021 18:24:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c6abad0f4c4ef8f57cefc7a7bf1b5a7b442e4b54a44a41722635e173aa6281`  
		Last Modified: Wed, 17 Mar 2021 18:24:44 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3098e77a5afcff1082201f8a4c0a252125e13806cbe5b16bb32429e03b9cce1d`  
		Last Modified: Wed, 17 Mar 2021 18:24:44 GMT  
		Size: 3.9 KB (3922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:9840d194969f764a892cc2c7eef7e8c66214264ec17d96f7b21fdb5b1c803765
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57581280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0e75edb4cddfe0f916bd39f98f76cc2ed89c4cb1c1c9e44cd2f7630587634c`
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
# Wed, 17 Mar 2021 17:41:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Mar 2021 17:41:40 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 17 Mar 2021 17:41:47 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 17 Mar 2021 17:41:50 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 17 Mar 2021 17:41:51 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 17 Mar 2021 17:41:51 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 17 Mar 2021 17:41:52 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 17 Mar 2021 17:41:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Mar 2021 17:41:54 GMT
CMD ["influxd"]
# Wed, 17 Mar 2021 17:41:55 GMT
EXPOSE 8086
# Wed, 17 Mar 2021 17:41:55 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 17 Mar 2021 17:41:56 GMT
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
	-	`sha256:1325cab6b18db58aa541a042a9f2102d32982b143413f30dc21bd4ed44cc5ba2`  
		Last Modified: Wed, 17 Mar 2021 17:42:40 GMT  
		Size: 896.1 KB (896107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51da687a3bd52f0d68ec78f8c5c318a689185b99324238c51675cd338182a40d`  
		Last Modified: Wed, 17 Mar 2021 17:42:49 GMT  
		Size: 44.4 MB (44403964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09c1a0be5ba0b717afcba312309eb8cc9e7683b4cc96acb344b5e0e482c1d4f`  
		Last Modified: Wed, 17 Mar 2021 17:42:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a57191351b89117a69551902d75fb475bb9399726bc40373792716096b9287c`  
		Last Modified: Wed, 17 Mar 2021 17:42:40 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b291ff54275c708e972945d8d7114c9fa8fa877cb39a04a59e809c2927974767`  
		Last Modified: Wed, 17 Mar 2021 17:42:40 GMT  
		Size: 3.9 KB (3927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0.4`

```console
$ docker pull influxdb@sha256:f84d9dc486e5933fdca12c66dc945101b21e356c2f5838e4ac42b355c41813ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0.4` - linux; amd64

```console
$ docker pull influxdb@sha256:3d8220100eebbe8163daa1ec3112ea85352916e4e61e4eed3d3c3f54b54e567e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116198808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f9150a5e7f1ab4d6149ac0622fbe536a0a1dedae2bfd88b9dd2680ebeebbc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:27 GMT
ADD file:575bf0d00d72810609a4118728923f11625b43de536352fe69a341086e4ebfd1 in / 
# Fri, 12 Mar 2021 02:20:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:49:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:49:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:09:42 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 13 Mar 2021 10:09:42 GMT
ENV GOSU_VER=1.12
# Sat, 13 Mar 2021 10:09:46 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Sat, 13 Mar 2021 10:09:46 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 17 Mar 2021 18:23:06 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 17 Mar 2021 18:23:08 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 17 Mar 2021 18:23:08 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 17 Mar 2021 18:23:08 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 17 Mar 2021 18:23:08 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 17 Mar 2021 18:23:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Mar 2021 18:23:09 GMT
CMD ["influxd"]
# Wed, 17 Mar 2021 18:23:09 GMT
EXPOSE 8086
# Wed, 17 Mar 2021 18:23:09 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 17 Mar 2021 18:23:09 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:e22122b926a1a853d61887fa35c3fe53e05ee7dc0f2f488936dc9838bd0e230d`  
		Last Modified: Fri, 12 Mar 2021 02:25:38 GMT  
		Size: 50.4 MB (50400353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e09ae83733d697508e34827538cc0129b8719b85db943041c5d37287bcb81`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 7.8 MB (7832474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e319e3daef68c36099bf3b534377a78d373f67bde3d156119c2463f5fe133ac5`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 10.0 MB (9997147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b330fcd093c9f406b78dbb3eb30ba647453e21a6f98248db555edbc9b4b05c14`  
		Last Modified: Sat, 13 Mar 2021 10:15:13 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5fbd072b21506c45c169f90c463ab8dc87270ade79660a625bae429508fe4b`  
		Last Modified: Sat, 13 Mar 2021 10:15:10 GMT  
		Size: 961.0 KB (960992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a11e9877203e1cb0d2d341484c3dd53093bbe1c47563ca5e9b209eaefe60640`  
		Last Modified: Wed, 17 Mar 2021 18:24:29 GMT  
		Size: 47.0 MB (47001580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ebd202fc31a7821bf65c6b05f8e83afa333314c353343142be1e9f9be2dd91`  
		Last Modified: Wed, 17 Mar 2021 18:24:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3679fc97953d82c23817aeb72bd0c1ae75ead527692a8b4921a9d2382e7322`  
		Last Modified: Wed, 17 Mar 2021 18:24:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3e9aa12abff71c52d71f001a63c1e8608a1f76d61bdd778ce58f1fd86f6f4c`  
		Last Modified: Wed, 17 Mar 2021 18:24:22 GMT  
		Size: 3.9 KB (3922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0.4` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:52fe997276608db793e9e9616e1548eb9815dff6539cbc3e8bda79f88449a3c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112181150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e0140e11122b7680b0f65178b63cced4f963497d66b1a953be99045f8ffe9b`
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
# Wed, 17 Mar 2021 17:41:18 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 17 Mar 2021 17:41:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 17 Mar 2021 17:41:21 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 17 Mar 2021 17:41:22 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 17 Mar 2021 17:41:23 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 17 Mar 2021 17:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Mar 2021 17:41:25 GMT
CMD ["influxd"]
# Wed, 17 Mar 2021 17:41:25 GMT
EXPOSE 8086
# Wed, 17 Mar 2021 17:41:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 17 Mar 2021 17:41:27 GMT
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
	-	`sha256:e6bd2f6270db099d4e06c87835dcd290765c59381fbc9523ec7f2038ab5328a0`  
		Last Modified: Wed, 17 Mar 2021 17:42:28 GMT  
		Size: 44.4 MB (44403990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde6be645ea4f12c5bf48eced01d7eff45d3b9807dc0ccc11c6218e7b25fd607`  
		Last Modified: Wed, 17 Mar 2021 17:42:19 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa62b33c5c36df63a4c674a8dcd0864a4deda5d635e72958d2ca7b7ba64c293`  
		Last Modified: Wed, 17 Mar 2021 17:42:19 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a084e7539f63b191fd5fb9c5f0d21f1038f1216cac7c9a967cefd0ce783eb00`  
		Last Modified: Wed, 17 Mar 2021 17:42:19 GMT  
		Size: 3.9 KB (3926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:2.0.4-alpine`

```console
$ docker pull influxdb@sha256:140cff530782b7f380a02d55bc9325c61b19f887824d54248c86a449393aa2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:2.0.4-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:55e9c2a38b9013fae5faec4e97f5d4c4b54380285ab84f3a8862ee62e3dec63e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60480698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3279de7243f7292ca2a9ebd4fabbf53720ae84442f28b4d9bd25fa3b29ed685f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 13 Mar 2021 04:22:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:09:59 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Sat, 13 Mar 2021 10:10:00 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 13 Mar 2021 10:10:00 GMT
ENV GOSU_VER=1.12
# Wed, 17 Mar 2021 18:23:16 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Mar 2021 18:23:16 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 17 Mar 2021 18:23:22 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 17 Mar 2021 18:23:23 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 17 Mar 2021 18:23:23 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 17 Mar 2021 18:23:24 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 17 Mar 2021 18:23:24 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 17 Mar 2021 18:23:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Mar 2021 18:23:24 GMT
CMD ["influxd"]
# Wed, 17 Mar 2021 18:23:24 GMT
EXPOSE 8086
# Wed, 17 Mar 2021 18:23:25 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 17 Mar 2021 18:23:25 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf3a7b369ab361149a2966cf437a5fd4730d81746d4aa29dd71ecbed71765da`  
		Last Modified: Sat, 13 Mar 2021 04:23:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81573d157ce7aceb135335ef386f0405887d0bdd187e4fee5287cf82de3b32`  
		Last Modified: Sat, 13 Mar 2021 10:15:35 GMT  
		Size: 9.7 MB (9700963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4832d1f6325f85d19c79a40d3d1b880fa86fdf04dea68d5e718abc3d53fa2c5`  
		Last Modified: Sat, 13 Mar 2021 10:15:33 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce58b7cf68cf881fec31d70740252c1d2d7ddb55db6461bd6e0c1d4cd654351`  
		Last Modified: Wed, 17 Mar 2021 18:24:44 GMT  
		Size: 960.6 KB (960620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f44e70b13ed0efcbfd808ae158fa6b6c4af768a66a456a9cbaba1496d21f9d`  
		Last Modified: Wed, 17 Mar 2021 18:24:55 GMT  
		Size: 47.0 MB (47001589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3013020617680ac7db9d3f556a52622fbe98169ac8f3bc7cb1e265c6a94ddb`  
		Last Modified: Wed, 17 Mar 2021 18:24:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c6abad0f4c4ef8f57cefc7a7bf1b5a7b442e4b54a44a41722635e173aa6281`  
		Last Modified: Wed, 17 Mar 2021 18:24:44 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3098e77a5afcff1082201f8a4c0a252125e13806cbe5b16bb32429e03b9cce1d`  
		Last Modified: Wed, 17 Mar 2021 18:24:44 GMT  
		Size: 3.9 KB (3922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:2.0.4-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:9840d194969f764a892cc2c7eef7e8c66214264ec17d96f7b21fdb5b1c803765
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57581280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0e75edb4cddfe0f916bd39f98f76cc2ed89c4cb1c1c9e44cd2f7630587634c`
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
# Wed, 17 Mar 2021 17:41:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Mar 2021 17:41:40 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 17 Mar 2021 17:41:47 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 17 Mar 2021 17:41:50 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 17 Mar 2021 17:41:51 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 17 Mar 2021 17:41:51 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 17 Mar 2021 17:41:52 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 17 Mar 2021 17:41:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Mar 2021 17:41:54 GMT
CMD ["influxd"]
# Wed, 17 Mar 2021 17:41:55 GMT
EXPOSE 8086
# Wed, 17 Mar 2021 17:41:55 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 17 Mar 2021 17:41:56 GMT
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
	-	`sha256:1325cab6b18db58aa541a042a9f2102d32982b143413f30dc21bd4ed44cc5ba2`  
		Last Modified: Wed, 17 Mar 2021 17:42:40 GMT  
		Size: 896.1 KB (896107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51da687a3bd52f0d68ec78f8c5c318a689185b99324238c51675cd338182a40d`  
		Last Modified: Wed, 17 Mar 2021 17:42:49 GMT  
		Size: 44.4 MB (44403964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09c1a0be5ba0b717afcba312309eb8cc9e7683b4cc96acb344b5e0e482c1d4f`  
		Last Modified: Wed, 17 Mar 2021 17:42:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a57191351b89117a69551902d75fb475bb9399726bc40373792716096b9287c`  
		Last Modified: Wed, 17 Mar 2021 17:42:40 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b291ff54275c708e972945d8d7114c9fa8fa877cb39a04a59e809c2927974767`  
		Last Modified: Wed, 17 Mar 2021 17:42:40 GMT  
		Size: 3.9 KB (3927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:140cff530782b7f380a02d55bc9325c61b19f887824d54248c86a449393aa2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:55e9c2a38b9013fae5faec4e97f5d4c4b54380285ab84f3a8862ee62e3dec63e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60480698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3279de7243f7292ca2a9ebd4fabbf53720ae84442f28b4d9bd25fa3b29ed685f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Sat, 13 Mar 2021 04:22:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:09:59 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Sat, 13 Mar 2021 10:10:00 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 13 Mar 2021 10:10:00 GMT
ENV GOSU_VER=1.12
# Wed, 17 Mar 2021 18:23:16 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Mar 2021 18:23:16 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 17 Mar 2021 18:23:22 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 17 Mar 2021 18:23:23 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 17 Mar 2021 18:23:23 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 17 Mar 2021 18:23:24 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 17 Mar 2021 18:23:24 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 17 Mar 2021 18:23:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Mar 2021 18:23:24 GMT
CMD ["influxd"]
# Wed, 17 Mar 2021 18:23:24 GMT
EXPOSE 8086
# Wed, 17 Mar 2021 18:23:25 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 17 Mar 2021 18:23:25 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf3a7b369ab361149a2966cf437a5fd4730d81746d4aa29dd71ecbed71765da`  
		Last Modified: Sat, 13 Mar 2021 04:23:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81573d157ce7aceb135335ef386f0405887d0bdd187e4fee5287cf82de3b32`  
		Last Modified: Sat, 13 Mar 2021 10:15:35 GMT  
		Size: 9.7 MB (9700963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4832d1f6325f85d19c79a40d3d1b880fa86fdf04dea68d5e718abc3d53fa2c5`  
		Last Modified: Sat, 13 Mar 2021 10:15:33 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce58b7cf68cf881fec31d70740252c1d2d7ddb55db6461bd6e0c1d4cd654351`  
		Last Modified: Wed, 17 Mar 2021 18:24:44 GMT  
		Size: 960.6 KB (960620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f44e70b13ed0efcbfd808ae158fa6b6c4af768a66a456a9cbaba1496d21f9d`  
		Last Modified: Wed, 17 Mar 2021 18:24:55 GMT  
		Size: 47.0 MB (47001589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3013020617680ac7db9d3f556a52622fbe98169ac8f3bc7cb1e265c6a94ddb`  
		Last Modified: Wed, 17 Mar 2021 18:24:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c6abad0f4c4ef8f57cefc7a7bf1b5a7b442e4b54a44a41722635e173aa6281`  
		Last Modified: Wed, 17 Mar 2021 18:24:44 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3098e77a5afcff1082201f8a4c0a252125e13806cbe5b16bb32429e03b9cce1d`  
		Last Modified: Wed, 17 Mar 2021 18:24:44 GMT  
		Size: 3.9 KB (3922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:9840d194969f764a892cc2c7eef7e8c66214264ec17d96f7b21fdb5b1c803765
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57581280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0e75edb4cddfe0f916bd39f98f76cc2ed89c4cb1c1c9e44cd2f7630587634c`
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
# Wed, 17 Mar 2021 17:41:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Mar 2021 17:41:40 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 17 Mar 2021 17:41:47 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 17 Mar 2021 17:41:50 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 17 Mar 2021 17:41:51 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 17 Mar 2021 17:41:51 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 17 Mar 2021 17:41:52 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 17 Mar 2021 17:41:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Mar 2021 17:41:54 GMT
CMD ["influxd"]
# Wed, 17 Mar 2021 17:41:55 GMT
EXPOSE 8086
# Wed, 17 Mar 2021 17:41:55 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 17 Mar 2021 17:41:56 GMT
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
	-	`sha256:1325cab6b18db58aa541a042a9f2102d32982b143413f30dc21bd4ed44cc5ba2`  
		Last Modified: Wed, 17 Mar 2021 17:42:40 GMT  
		Size: 896.1 KB (896107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51da687a3bd52f0d68ec78f8c5c318a689185b99324238c51675cd338182a40d`  
		Last Modified: Wed, 17 Mar 2021 17:42:49 GMT  
		Size: 44.4 MB (44403964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09c1a0be5ba0b717afcba312309eb8cc9e7683b4cc96acb344b5e0e482c1d4f`  
		Last Modified: Wed, 17 Mar 2021 17:42:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a57191351b89117a69551902d75fb475bb9399726bc40373792716096b9287c`  
		Last Modified: Wed, 17 Mar 2021 17:42:40 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b291ff54275c708e972945d8d7114c9fa8fa877cb39a04a59e809c2927974767`  
		Last Modified: Wed, 17 Mar 2021 17:42:40 GMT  
		Size: 3.9 KB (3927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data`

```console
$ docker pull influxdb@sha256:1a848bd4ee1a8a12220886b2213e8f41f8518a8005e53508c8c4827a2d190978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:ecc951feb2a2c357b9a3460c6a8dc8eeaaf38e6ecc4a60c194a150aec92b82fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126794466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ff7f6acf2095904719d11c3f266f95c1b1fc1ada6cfa5ec251e6bea6e89999`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:07:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 13 Mar 2021 10:09:00 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 13 Mar 2021 10:09:06 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 13 Mar 2021 10:09:07 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 13 Mar 2021 10:09:07 GMT
EXPOSE 8086
# Sat, 13 Mar 2021 10:09:07 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:09:07 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:09:07 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 13 Mar 2021 10:09:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:09:08 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25737831bed10fe0362ba56031883977ad22903ddcb50b82c3f74982b1179565`  
		Last Modified: Sat, 13 Mar 2021 10:10:50 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18576c011e4fba451270d363e409c97b372b9fdf2fd235ce41bc78e9a817535d`  
		Last Modified: Sat, 13 Mar 2021 10:13:54 GMT  
		Size: 65.8 MB (65796421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141c9c3bb5a126ba7762bf6e8490158429fced829fae9e8e8474e4d13ae50a57`  
		Last Modified: Sat, 13 Mar 2021 10:13:45 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7e88aff98fdcb49c6eb4d996f4a69041cd2591c7503d317aeaf2a44e8404cd`  
		Last Modified: Sat, 13 Mar 2021 10:13:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5267ed226902fef8eb8572d171b1efcda36c633f8bfe60c498a27afe764013`  
		Last Modified: Sat, 13 Mar 2021 10:13:45 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:72201ba79e44315cac8944621549d40e8ba8350b6b00917eea49b8f88e7e3dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:33519de466913e487be9e1f02af9e6e849e05849e2137cb7d09d7ebcf016839a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69772902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e662be1d19d8a9bd697d6438b0908a800d0a310d4bd04165e68ec05ffd0691a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:07:34 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 13 Mar 2021 10:09:11 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 13 Mar 2021 10:09:19 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 13 Mar 2021 10:09:19 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sat, 13 Mar 2021 10:09:20 GMT
EXPOSE 8086
# Sat, 13 Mar 2021 10:09:20 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:09:20 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:09:20 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 13 Mar 2021 10:09:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:09:21 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b572d48a3184c0ad742e4c1b3b72687a6f896767590493e8b39cc19f843924`  
		Last Modified: Sat, 13 Mar 2021 10:11:15 GMT  
		Size: 1.4 MB (1430764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef23fd2718fb492806f24481d4bbef97011a461dc36cd3657567662996c35a5`  
		Last Modified: Sat, 13 Mar 2021 10:14:17 GMT  
		Size: 65.5 MB (65540696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d750db74011b4bd6cdadca668da48e27a2316e6218fd046f57d3c30fa7308ba6`  
		Last Modified: Sat, 13 Mar 2021 10:14:08 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46ffac5dbd2cc362451f8274fb25f20aa672e9668a4e09e3fe9d7c799fad126`  
		Last Modified: Sat, 13 Mar 2021 10:14:08 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8683186eb48f43e6644290a19d3c83098a730a4ba1a1b3119af598dc30cfd8`  
		Last Modified: Sat, 13 Mar 2021 10:14:08 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:f84d9dc486e5933fdca12c66dc945101b21e356c2f5838e4ac42b355c41813ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:3d8220100eebbe8163daa1ec3112ea85352916e4e61e4eed3d3c3f54b54e567e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116198808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f9150a5e7f1ab4d6149ac0622fbe536a0a1dedae2bfd88b9dd2680ebeebbc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:27 GMT
ADD file:575bf0d00d72810609a4118728923f11625b43de536352fe69a341086e4ebfd1 in / 
# Fri, 12 Mar 2021 02:20:28 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:49:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:49:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:09:42 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 13 Mar 2021 10:09:42 GMT
ENV GOSU_VER=1.12
# Sat, 13 Mar 2021 10:09:46 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Sat, 13 Mar 2021 10:09:46 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 17 Mar 2021 18:23:06 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 17 Mar 2021 18:23:08 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 17 Mar 2021 18:23:08 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 17 Mar 2021 18:23:08 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 17 Mar 2021 18:23:08 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 17 Mar 2021 18:23:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Mar 2021 18:23:09 GMT
CMD ["influxd"]
# Wed, 17 Mar 2021 18:23:09 GMT
EXPOSE 8086
# Wed, 17 Mar 2021 18:23:09 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 17 Mar 2021 18:23:09 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:e22122b926a1a853d61887fa35c3fe53e05ee7dc0f2f488936dc9838bd0e230d`  
		Last Modified: Fri, 12 Mar 2021 02:25:38 GMT  
		Size: 50.4 MB (50400353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e09ae83733d697508e34827538cc0129b8719b85db943041c5d37287bcb81`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 7.8 MB (7832474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e319e3daef68c36099bf3b534377a78d373f67bde3d156119c2463f5fe133ac5`  
		Last Modified: Fri, 12 Mar 2021 03:19:09 GMT  
		Size: 10.0 MB (9997147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b330fcd093c9f406b78dbb3eb30ba647453e21a6f98248db555edbc9b4b05c14`  
		Last Modified: Sat, 13 Mar 2021 10:15:13 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5fbd072b21506c45c169f90c463ab8dc87270ade79660a625bae429508fe4b`  
		Last Modified: Sat, 13 Mar 2021 10:15:10 GMT  
		Size: 961.0 KB (960992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a11e9877203e1cb0d2d341484c3dd53093bbe1c47563ca5e9b209eaefe60640`  
		Last Modified: Wed, 17 Mar 2021 18:24:29 GMT  
		Size: 47.0 MB (47001580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ebd202fc31a7821bf65c6b05f8e83afa333314c353343142be1e9f9be2dd91`  
		Last Modified: Wed, 17 Mar 2021 18:24:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3679fc97953d82c23817aeb72bd0c1ae75ead527692a8b4921a9d2382e7322`  
		Last Modified: Wed, 17 Mar 2021 18:24:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3e9aa12abff71c52d71f001a63c1e8608a1f76d61bdd778ce58f1fd86f6f4c`  
		Last Modified: Wed, 17 Mar 2021 18:24:22 GMT  
		Size: 3.9 KB (3922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:52fe997276608db793e9e9616e1548eb9815dff6539cbc3e8bda79f88449a3c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112181150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e0140e11122b7680b0f65178b63cced4f963497d66b1a953be99045f8ffe9b`
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
# Wed, 17 Mar 2021 17:41:18 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 17 Mar 2021 17:41:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 17 Mar 2021 17:41:21 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 17 Mar 2021 17:41:22 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 17 Mar 2021 17:41:23 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 17 Mar 2021 17:41:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Mar 2021 17:41:25 GMT
CMD ["influxd"]
# Wed, 17 Mar 2021 17:41:25 GMT
EXPOSE 8086
# Wed, 17 Mar 2021 17:41:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 17 Mar 2021 17:41:27 GMT
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
	-	`sha256:e6bd2f6270db099d4e06c87835dcd290765c59381fbc9523ec7f2038ab5328a0`  
		Last Modified: Wed, 17 Mar 2021 17:42:28 GMT  
		Size: 44.4 MB (44403990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde6be645ea4f12c5bf48eced01d7eff45d3b9807dc0ccc11c6218e7b25fd607`  
		Last Modified: Wed, 17 Mar 2021 17:42:19 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa62b33c5c36df63a4c674a8dcd0864a4deda5d635e72958d2ca7b7ba64c293`  
		Last Modified: Wed, 17 Mar 2021 17:42:19 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a084e7539f63b191fd5fb9c5f0d21f1038f1216cac7c9a967cefd0ce783eb00`  
		Last Modified: Wed, 17 Mar 2021 17:42:19 GMT  
		Size: 3.9 KB (3926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:e8f7332ae9bf4935cd55651cb66df86c458e640f7d31a4f693c2addf64a77336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c34a2ae90ea1ad09e67c0b70494356874af68d53553073f4eb24e95aecdb24fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83863091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911cfe59b714c4ed06169ca6b8c633eeb32f8b84c995046a15896abc7b9ecbd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:36 GMT
ADD file:5f8ab4280b54d91475c84e497163ec05aabb5a9f9b9de687d38fda535ddc29b2 in / 
# Fri, 12 Mar 2021 02:22:36 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 13 Mar 2021 10:07:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 13 Mar 2021 10:09:00 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 13 Mar 2021 10:09:28 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sat, 13 Mar 2021 10:09:28 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 13 Mar 2021 10:09:29 GMT
EXPOSE 8091
# Sat, 13 Mar 2021 10:09:29 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:09:29 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:09:29 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:16cf3fa6cb1190b4dfd82a5319faa13e2eb6e69b7b4828d4d98ba1c0b216e446`  
		Last Modified: Fri, 12 Mar 2021 02:29:57 GMT  
		Size: 45.4 MB (45380216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd031622b35dad4be68eec6ac0787b0394f37b3dbb600a04e8b2363297b8d7`  
		Last Modified: Fri, 12 Mar 2021 03:22:18 GMT  
		Size: 11.3 MB (11270857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3fcab77df556f3a56ec3d2a5b5cc304f4c4d4341b6f8423dd86ebe5ddaebb`  
		Last Modified: Fri, 12 Mar 2021 03:22:16 GMT  
		Size: 4.3 MB (4342349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25737831bed10fe0362ba56031883977ad22903ddcb50b82c3f74982b1179565`  
		Last Modified: Sat, 13 Mar 2021 10:10:50 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca679c2c6e2a4ce57f63ba3dcb941dde4764c229295240ac47383c0ab2d58d53`  
		Last Modified: Sat, 13 Mar 2021 10:14:39 GMT  
		Size: 22.9 MB (22866247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce7a1017fc271c11da61ca509b5dac1881c8032f0bf0b7d5e2c3b57ac32201e`  
		Last Modified: Sat, 13 Mar 2021 10:14:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cebe14b4929afdae376a7ce1883ea97e600d4e9d35aa0c347602e0eefc8305`  
		Last Modified: Sat, 13 Mar 2021 10:14:35 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:f5e194de56745fc72bb1bb460ed88f59023c65005403117c4b0694f6531c89ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:87dd9e771b3d8b514f0970ce5d82f84edf65d681d5482983b3598f58de3d4c5a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26966388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acafa701406a7367f7215f4368a8730c24d0c048cd2bbfcbfdfa134548ef7c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 03:37:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Mar 2021 10:07:34 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 13 Mar 2021 10:09:11 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Sat, 13 Mar 2021 10:09:37 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 13 Mar 2021 10:09:37 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sat, 13 Mar 2021 10:09:37 GMT
EXPOSE 8091
# Sat, 13 Mar 2021 10:09:37 GMT
VOLUME [/var/lib/influxdb]
# Sat, 13 Mar 2021 10:09:38 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sat, 13 Mar 2021 10:09:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 13 Mar 2021 10:09:38 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab45d475695400229b7b704d7c3a4a6f326f0eb1299894f67d202fbaf5a331`  
		Last Modified: Fri, 12 Mar 2021 03:39:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b572d48a3184c0ad742e4c1b3b72687a6f896767590493e8b39cc19f843924`  
		Last Modified: Sat, 13 Mar 2021 10:11:15 GMT  
		Size: 1.4 MB (1430764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d519f7d0d8e6ebd6e8856db8a34338ab36f21a9f7750c061f728f3f7faf4b`  
		Last Modified: Sat, 13 Mar 2021 10:14:56 GMT  
		Size: 22.7 MB (22735383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820d21cf4e4c41228969e4da796d51abb8f7bf7379ce56380ae57f321336700f`  
		Last Modified: Sat, 13 Mar 2021 10:14:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3eafd806e9fb49033f42ce9dd548448f5fb429b0e7070c800b0cb5539273d4`  
		Last Modified: Sat, 13 Mar 2021 10:14:53 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
