<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.5`](#influxdb15)
-	[`influxdb:1.5.4`](#influxdb154)
-	[`influxdb:1.5.4-alpine`](#influxdb154-alpine)
-	[`influxdb:1.5.4-data`](#influxdb154-data)
-	[`influxdb:1.5.4-data-alpine`](#influxdb154-data-alpine)
-	[`influxdb:1.5.4-meta`](#influxdb154-meta)
-	[`influxdb:1.5.4-meta-alpine`](#influxdb154-meta-alpine)
-	[`influxdb:1.5-alpine`](#influxdb15-alpine)
-	[`influxdb:1.5-data`](#influxdb15-data)
-	[`influxdb:1.5-data-alpine`](#influxdb15-data-alpine)
-	[`influxdb:1.5-meta`](#influxdb15-meta)
-	[`influxdb:1.5-meta-alpine`](#influxdb15-meta-alpine)
-	[`influxdb:1.6`](#influxdb16)
-	[`influxdb:1.6.6`](#influxdb166)
-	[`influxdb:1.6.6-alpine`](#influxdb166-alpine)
-	[`influxdb:1.6.6-data`](#influxdb166-data)
-	[`influxdb:1.6.6-data-alpine`](#influxdb166-data-alpine)
-	[`influxdb:1.6.6-meta`](#influxdb166-meta)
-	[`influxdb:1.6.6-meta-alpine`](#influxdb166-meta-alpine)
-	[`influxdb:1.6-alpine`](#influxdb16-alpine)
-	[`influxdb:1.6-data`](#influxdb16-data)
-	[`influxdb:1.6-data-alpine`](#influxdb16-data-alpine)
-	[`influxdb:1.6-meta`](#influxdb16-meta)
-	[`influxdb:1.6-meta-alpine`](#influxdb16-meta-alpine)
-	[`influxdb:1.7`](#influxdb17)
-	[`influxdb:1.7.10`](#influxdb1710)
-	[`influxdb:1.7.10-alpine`](#influxdb1710-alpine)
-	[`influxdb:1.7.10-data`](#influxdb1710-data)
-	[`influxdb:1.7.10-data-alpine`](#influxdb1710-data-alpine)
-	[`influxdb:1.7.10-meta`](#influxdb1710-meta)
-	[`influxdb:1.7.10-meta-alpine`](#influxdb1710-meta-alpine)
-	[`influxdb:1.7-alpine`](#influxdb17-alpine)
-	[`influxdb:1.7-data`](#influxdb17-data)
-	[`influxdb:1.7-data-alpine`](#influxdb17-data-alpine)
-	[`influxdb:1.7-meta`](#influxdb17-meta)
-	[`influxdb:1.7-meta-alpine`](#influxdb17-meta-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:data`](#influxdbdata)
-	[`influxdb:data-alpine`](#influxdbdata-alpine)
-	[`influxdb:latest`](#influxdblatest)
-	[`influxdb:meta`](#influxdbmeta)
-	[`influxdb:meta-alpine`](#influxdbmeta-alpine)

## `influxdb:1.5`

```console
$ docker pull influxdb@sha256:288509621df042aae118027f56348ace846ee50cc2f274427e3340416a97dd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.5` - linux; amd64

```console
$ docker pull influxdb@sha256:9ef2a28d7274e656b6445abac2e9dcbfda8d5edf751eddb91b3f0bd7bb5620a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83546877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515fe44f08152285d6397c0fb49e72ce47d97a0844d2b3e68814e9ab7626884a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:54:16 GMT
ENV INFLUXDB_VERSION=1.5.4
# Wed, 01 Apr 2020 01:54:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 01 Apr 2020 01:54:20 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 01 Apr 2020 01:54:20 GMT
EXPOSE 8086
# Wed, 01 Apr 2020 01:54:20 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:54:21 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:54:21 GMT
COPY file:9d63e46d6e9bed7502af5cddf053b5ea832d65716b7e457a74a61af74587483a in /init-influxdb.sh 
# Wed, 01 Apr 2020 01:54:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:54:21 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b720d56ef94f09db4b7fe8e4a44443bae5de71d263e74aea74076aa16cbb5f3d`  
		Last Modified: Wed, 01 Apr 2020 01:57:33 GMT  
		Size: 23.0 MB (23029013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f08ee46430a160b32608d90674830eef640a4c45706b239191172ab5ed1edf`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1adb4a8f236d83d3eb7acdc4f329babf8848110f657d0413960016b8cb5a7b`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b185e00b122d5b5134cbacb433e08c0adf00403def4d18c8f579fccf6360806c`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.5` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:894349b507c15ad7b3f952b68a660abbe299129033a6e26ebb5d54c7d2c15aeb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77180643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c57c0af2ccf059b27532edd31deb7d4417f76b8181dc3293fd0c451347e1f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:24 GMT
ADD file:b047b0c4dbfbcc048385195e807283b9386c4aac13a4841112cb3f76cd932b06 in / 
# Tue, 31 Mar 2020 01:52:26 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:53:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 23:27:41 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 23:27:42 GMT
ENV INFLUXDB_VERSION=1.5.4
# Tue, 31 Mar 2020 23:27:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 23:27:56 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 31 Mar 2020 23:27:57 GMT
EXPOSE 8086
# Tue, 31 Mar 2020 23:27:58 GMT
VOLUME [/var/lib/influxdb]
# Tue, 31 Mar 2020 23:27:59 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 31 Mar 2020 23:28:00 GMT
COPY file:9d63e46d6e9bed7502af5cddf053b5ea832d65716b7e457a74a61af74587483a in /init-influxdb.sh 
# Tue, 31 Mar 2020 23:28:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 23:28:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:eb3768893937e6b455f98cd8db65949a6aa5c54ebd94fca3039af9833187ce10`  
		Last Modified: Tue, 31 Mar 2020 01:59:52 GMT  
		Size: 42.1 MB (42100090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb68590923b075c8f49c4470341451f9d874afc84c5fc916278815a1064243`  
		Last Modified: Tue, 31 Mar 2020 04:04:43 GMT  
		Size: 9.5 MB (9498284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743981b4cf60d4ed8ddd6610e4d1d75256ddb63a7d83d540a96e1faf8ba8a315`  
		Last Modified: Tue, 31 Mar 2020 04:04:42 GMT  
		Size: 3.9 MB (3918805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39848df21e0940ce448bbc5a30bb53f1ae2d3a23b774be8add8462388496176d`  
		Last Modified: Tue, 31 Mar 2020 23:29:03 GMT  
		Size: 2.8 KB (2805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfe5e926036bb4d10845efb0c0e7d2be6d10b220949d30f49a256f350fd2eb8`  
		Last Modified: Tue, 31 Mar 2020 23:29:11 GMT  
		Size: 21.7 MB (21658943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9880f4d6b37345bd12222b535bd89fe6dba532fec2d41b81f128dfb94026ac4`  
		Last Modified: Tue, 31 Mar 2020 23:29:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a305b3675657b73f086d7c9658d1702886e1be8680411ec24bc84f0020a1164`  
		Last Modified: Tue, 31 Mar 2020 23:29:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e44bb7a824ba04168af270e2c3698fce357e37a6d52a59a8ed2fff72dbbcf59`  
		Last Modified: Tue, 31 Mar 2020 23:29:02 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.5` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:63f0c018d055f23503c24614b8987b5527c76f5cfe16f6a3de32f60084160d9f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78015968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14388c7d4157506a5907cd23ff3f41c7beb325830cd33a961d2c9909a44643d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:21:37 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 21:21:38 GMT
ENV INFLUXDB_VERSION=1.5.4
# Tue, 31 Mar 2020 21:21:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 21:21:44 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 31 Mar 2020 21:21:45 GMT
EXPOSE 8086
# Tue, 31 Mar 2020 21:21:45 GMT
VOLUME [/var/lib/influxdb]
# Tue, 31 Mar 2020 21:21:46 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 31 Mar 2020 21:21:47 GMT
COPY file:9d63e46d6e9bed7502af5cddf053b5ea832d65716b7e457a74a61af74587483a in /init-influxdb.sh 
# Tue, 31 Mar 2020 21:21:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 21:21:48 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4b0dbd0d8c4ebbcb0bd21245e7f3bfa3f1dcaa045d058597cb38fd62aa3c95`  
		Last Modified: Tue, 31 Mar 2020 21:22:36 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a63ae22ed78cf7ef5e0a3ab9ec8142586762b1775d340c9f8bcdcd4cf75d593`  
		Last Modified: Tue, 31 Mar 2020 21:22:43 GMT  
		Size: 21.0 MB (21010473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c045e79c1dd83e61922b48352824534d3d7bd2d68dfa82bfd7497cbb2515e861`  
		Last Modified: Tue, 31 Mar 2020 21:22:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ec0608bf3aebe642fed219524433eea77c3e70b49be7b0847b619c610f8a1a`  
		Last Modified: Tue, 31 Mar 2020 21:22:35 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960db156b4a4885140f4d33548df3054ce26ba4290efc98ee575c3f3daa844d5`  
		Last Modified: Tue, 31 Mar 2020 21:22:36 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5.4`

```console
$ docker pull influxdb@sha256:288509621df042aae118027f56348ace846ee50cc2f274427e3340416a97dd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.5.4` - linux; amd64

```console
$ docker pull influxdb@sha256:9ef2a28d7274e656b6445abac2e9dcbfda8d5edf751eddb91b3f0bd7bb5620a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83546877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515fe44f08152285d6397c0fb49e72ce47d97a0844d2b3e68814e9ab7626884a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:54:16 GMT
ENV INFLUXDB_VERSION=1.5.4
# Wed, 01 Apr 2020 01:54:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 01 Apr 2020 01:54:20 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 01 Apr 2020 01:54:20 GMT
EXPOSE 8086
# Wed, 01 Apr 2020 01:54:20 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:54:21 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:54:21 GMT
COPY file:9d63e46d6e9bed7502af5cddf053b5ea832d65716b7e457a74a61af74587483a in /init-influxdb.sh 
# Wed, 01 Apr 2020 01:54:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:54:21 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b720d56ef94f09db4b7fe8e4a44443bae5de71d263e74aea74076aa16cbb5f3d`  
		Last Modified: Wed, 01 Apr 2020 01:57:33 GMT  
		Size: 23.0 MB (23029013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f08ee46430a160b32608d90674830eef640a4c45706b239191172ab5ed1edf`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1adb4a8f236d83d3eb7acdc4f329babf8848110f657d0413960016b8cb5a7b`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b185e00b122d5b5134cbacb433e08c0adf00403def4d18c8f579fccf6360806c`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.5.4` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:894349b507c15ad7b3f952b68a660abbe299129033a6e26ebb5d54c7d2c15aeb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77180643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c57c0af2ccf059b27532edd31deb7d4417f76b8181dc3293fd0c451347e1f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:24 GMT
ADD file:b047b0c4dbfbcc048385195e807283b9386c4aac13a4841112cb3f76cd932b06 in / 
# Tue, 31 Mar 2020 01:52:26 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:53:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 23:27:41 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 23:27:42 GMT
ENV INFLUXDB_VERSION=1.5.4
# Tue, 31 Mar 2020 23:27:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 23:27:56 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 31 Mar 2020 23:27:57 GMT
EXPOSE 8086
# Tue, 31 Mar 2020 23:27:58 GMT
VOLUME [/var/lib/influxdb]
# Tue, 31 Mar 2020 23:27:59 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 31 Mar 2020 23:28:00 GMT
COPY file:9d63e46d6e9bed7502af5cddf053b5ea832d65716b7e457a74a61af74587483a in /init-influxdb.sh 
# Tue, 31 Mar 2020 23:28:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 23:28:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:eb3768893937e6b455f98cd8db65949a6aa5c54ebd94fca3039af9833187ce10`  
		Last Modified: Tue, 31 Mar 2020 01:59:52 GMT  
		Size: 42.1 MB (42100090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb68590923b075c8f49c4470341451f9d874afc84c5fc916278815a1064243`  
		Last Modified: Tue, 31 Mar 2020 04:04:43 GMT  
		Size: 9.5 MB (9498284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743981b4cf60d4ed8ddd6610e4d1d75256ddb63a7d83d540a96e1faf8ba8a315`  
		Last Modified: Tue, 31 Mar 2020 04:04:42 GMT  
		Size: 3.9 MB (3918805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39848df21e0940ce448bbc5a30bb53f1ae2d3a23b774be8add8462388496176d`  
		Last Modified: Tue, 31 Mar 2020 23:29:03 GMT  
		Size: 2.8 KB (2805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfe5e926036bb4d10845efb0c0e7d2be6d10b220949d30f49a256f350fd2eb8`  
		Last Modified: Tue, 31 Mar 2020 23:29:11 GMT  
		Size: 21.7 MB (21658943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9880f4d6b37345bd12222b535bd89fe6dba532fec2d41b81f128dfb94026ac4`  
		Last Modified: Tue, 31 Mar 2020 23:29:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a305b3675657b73f086d7c9658d1702886e1be8680411ec24bc84f0020a1164`  
		Last Modified: Tue, 31 Mar 2020 23:29:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e44bb7a824ba04168af270e2c3698fce357e37a6d52a59a8ed2fff72dbbcf59`  
		Last Modified: Tue, 31 Mar 2020 23:29:02 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.5.4` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:63f0c018d055f23503c24614b8987b5527c76f5cfe16f6a3de32f60084160d9f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78015968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14388c7d4157506a5907cd23ff3f41c7beb325830cd33a961d2c9909a44643d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:21:37 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 21:21:38 GMT
ENV INFLUXDB_VERSION=1.5.4
# Tue, 31 Mar 2020 21:21:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 21:21:44 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 31 Mar 2020 21:21:45 GMT
EXPOSE 8086
# Tue, 31 Mar 2020 21:21:45 GMT
VOLUME [/var/lib/influxdb]
# Tue, 31 Mar 2020 21:21:46 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 31 Mar 2020 21:21:47 GMT
COPY file:9d63e46d6e9bed7502af5cddf053b5ea832d65716b7e457a74a61af74587483a in /init-influxdb.sh 
# Tue, 31 Mar 2020 21:21:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 21:21:48 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4b0dbd0d8c4ebbcb0bd21245e7f3bfa3f1dcaa045d058597cb38fd62aa3c95`  
		Last Modified: Tue, 31 Mar 2020 21:22:36 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a63ae22ed78cf7ef5e0a3ab9ec8142586762b1775d340c9f8bcdcd4cf75d593`  
		Last Modified: Tue, 31 Mar 2020 21:22:43 GMT  
		Size: 21.0 MB (21010473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c045e79c1dd83e61922b48352824534d3d7bd2d68dfa82bfd7497cbb2515e861`  
		Last Modified: Tue, 31 Mar 2020 21:22:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ec0608bf3aebe642fed219524433eea77c3e70b49be7b0847b619c610f8a1a`  
		Last Modified: Tue, 31 Mar 2020 21:22:35 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960db156b4a4885140f4d33548df3054ce26ba4290efc98ee575c3f3daa844d5`  
		Last Modified: Tue, 31 Mar 2020 21:22:36 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5.4-alpine`

```console
$ docker pull influxdb@sha256:8e4c6fd4173ab8788c7bbecf0f4e3fc46c380bd73795692284077fa57ec06957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5.4-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4ba2e4fffadbd511077577335f2602948f9986bd9be37283efb1b50e641576f8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27546568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6f252a585b5bba79a0e4ff0dbe6fd81f1fa6a69047a4ff83ccab54abc1c619`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:03:48 GMT
ENV INFLUXDB_VERSION=1.5.4
# Thu, 23 Jan 2020 19:03:53 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:03:53 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:03:53 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:03:53 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:03:53 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:03:54 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:03:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:03:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88394c2854089d5054b091622be66c81f76b1aa57aaab8a1e4fb260e6f2a4cbb`  
		Last Modified: Thu, 23 Jan 2020 19:07:10 GMT  
		Size: 22.9 MB (22916851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fc9971237ebca6230d5800910c605aa425f88e336456c4f952d3785f22236d`  
		Last Modified: Thu, 23 Jan 2020 19:07:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b417c45244d8df449455879226f05faf43924b084fffb3de3430975f03917f56`  
		Last Modified: Thu, 23 Jan 2020 19:07:01 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7397ad8bd2bc035e91075df8d70d674df7aa57e1d230556dff6a93b9d7ec370e`  
		Last Modified: Thu, 23 Jan 2020 19:07:01 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5.4-data`

```console
$ docker pull influxdb@sha256:29fe413cc1e5e6177d59ec4129856038fd0f43d05077b60dbea4ff4fa4330271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5.4-data` - linux; amd64

```console
$ docker pull influxdb@sha256:4e78aa7939730adf99ed443ef725c775f1b0a76defdbe665f4ade81865484dc7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84300643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e778cbbf40e90ade27a5fe232b3fff89c3d57283743503d17eb86d3c814848`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:54:29 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Wed, 01 Apr 2020 01:54:35 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 01 Apr 2020 01:54:35 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 01 Apr 2020 01:54:35 GMT
EXPOSE 8086
# Wed, 01 Apr 2020 01:54:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:54:36 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:54:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 01 Apr 2020 01:54:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:54:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4bcc5089cfc4abd26d43bae2d2c33c09c6d28e4a17dd077dce04fea28ca336`  
		Last Modified: Wed, 01 Apr 2020 01:57:44 GMT  
		Size: 23.8 MB (23782721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c11e336a1b7f341621263386d698569b0ee7da3bf80644ffcf1c23604feb1aa`  
		Last Modified: Wed, 01 Apr 2020 01:57:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00427487b4d66de06a2814199e5a1d6df166deae45cdcdb8c7f33530bb072adf`  
		Last Modified: Wed, 01 Apr 2020 01:57:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302518573ca30d38a5b5d0ebb2d033cd556e139146a31b338ae63d6928a30c76`  
		Last Modified: Wed, 01 Apr 2020 01:57:37 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5.4-data-alpine`

```console
$ docker pull influxdb@sha256:de7ead51d90b0ea4853ef4d603cc9cc17b386d33d0d5273decaefeab25d0d86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5.4-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:0a8e496ac00fb556392e252a47b047843e176c5f38a40160f86489ceb30825c8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28299789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe04106d38b3f3d171c1ce7f48100da80cc6d63d6ee14b0820f1a70f346f1eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:02 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Thu, 23 Jan 2020 19:04:07 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:07 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:04:07 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:04:07 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:07 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:07 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:04:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:08 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5636523728be94f8e3e0040b406697262e4b48fde6334e9ffe248d9082401`  
		Last Modified: Thu, 23 Jan 2020 19:07:30 GMT  
		Size: 23.7 MB (23670013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb8d0867f6a6f6d4a9d64a95b07f9cd2e1e8c961ec8b75c387a1967c89ec7ec`  
		Last Modified: Thu, 23 Jan 2020 19:07:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54826124424838ea73c4731f23548a42ad0693312df4b0399d1368d51c44562c`  
		Last Modified: Thu, 23 Jan 2020 19:07:15 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19b6aff30df100fd8085bb178fee7e62e0cc282b763decf56cecfe747642eed`  
		Last Modified: Thu, 23 Jan 2020 19:07:15 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5.4-meta`

```console
$ docker pull influxdb@sha256:5bfd60bbc406c6643e50ddfb55968622c5544c8628691836b3b11aa54fe9a6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5.4-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:027adb9d4a762d0d725b0f85c36b56be106107232b535bac6632276093c19b0e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71710844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0c5b801dc9eaec676ab8d69e91a0be67cf9d71afe7bb01441b4867e8b9c6db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:54:29 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Wed, 01 Apr 2020 01:54:50 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 01 Apr 2020 01:54:50 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 01 Apr 2020 01:54:51 GMT
EXPOSE 8091
# Wed, 01 Apr 2020 01:54:51 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:54:51 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:54:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:54:52 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0654d384a3eaad7d7da44dff8a811ee19972a2a5eff023aa5e38472104c5b32`  
		Last Modified: Wed, 01 Apr 2020 01:57:52 GMT  
		Size: 11.2 MB (11194126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50519f5c2fce761a2758fd77bc990843edd93481b234cd4c969dfeaaca9e00b6`  
		Last Modified: Wed, 01 Apr 2020 01:57:49 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab1a71222e0e4e005972758a858e68a43d661c24d4407d0f5ba18fc7fe130e5`  
		Last Modified: Wed, 01 Apr 2020 01:57:49 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5.4-meta-alpine`

```console
$ docker pull influxdb@sha256:6f84ba5ba10c833d9cc14b9c36541ab9657d68f1a46303784a08b691fc381154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5.4-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:77e862d69197c3b486eabc8170c199fa18dce5f81fc703d66f2fedba0d19eaf0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15779821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64e168fcf407e757b2ad9c3f9e73710a026bbe05be46a21f91d4aae930dcfa3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:02 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Thu, 23 Jan 2020 19:04:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:19 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 23 Jan 2020 19:04:19 GMT
EXPOSE 8091
# Thu, 23 Jan 2020 19:04:19 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:19 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:19 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0e87069833ff629f85d2e8945f09b6a5af9aacf30af70ff537adcb22b09772`  
		Last Modified: Thu, 23 Jan 2020 19:07:43 GMT  
		Size: 11.2 MB (11151245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab027e28e6d75a43518ff2cfe15764266fc70ff97d429bcaaa8fe936585e30f5`  
		Last Modified: Thu, 23 Jan 2020 19:07:35 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2836d507107845041948aa147917bdbd6177563dee7f77b1552983df73acc37`  
		Last Modified: Thu, 23 Jan 2020 19:07:35 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5-alpine`

```console
$ docker pull influxdb@sha256:8e4c6fd4173ab8788c7bbecf0f4e3fc46c380bd73795692284077fa57ec06957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4ba2e4fffadbd511077577335f2602948f9986bd9be37283efb1b50e641576f8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27546568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6f252a585b5bba79a0e4ff0dbe6fd81f1fa6a69047a4ff83ccab54abc1c619`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:03:48 GMT
ENV INFLUXDB_VERSION=1.5.4
# Thu, 23 Jan 2020 19:03:53 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:03:53 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:03:53 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:03:53 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:03:53 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:03:54 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:03:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:03:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88394c2854089d5054b091622be66c81f76b1aa57aaab8a1e4fb260e6f2a4cbb`  
		Last Modified: Thu, 23 Jan 2020 19:07:10 GMT  
		Size: 22.9 MB (22916851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fc9971237ebca6230d5800910c605aa425f88e336456c4f952d3785f22236d`  
		Last Modified: Thu, 23 Jan 2020 19:07:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b417c45244d8df449455879226f05faf43924b084fffb3de3430975f03917f56`  
		Last Modified: Thu, 23 Jan 2020 19:07:01 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7397ad8bd2bc035e91075df8d70d674df7aa57e1d230556dff6a93b9d7ec370e`  
		Last Modified: Thu, 23 Jan 2020 19:07:01 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5-data`

```console
$ docker pull influxdb@sha256:29fe413cc1e5e6177d59ec4129856038fd0f43d05077b60dbea4ff4fa4330271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5-data` - linux; amd64

```console
$ docker pull influxdb@sha256:4e78aa7939730adf99ed443ef725c775f1b0a76defdbe665f4ade81865484dc7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84300643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e778cbbf40e90ade27a5fe232b3fff89c3d57283743503d17eb86d3c814848`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:54:29 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Wed, 01 Apr 2020 01:54:35 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 01 Apr 2020 01:54:35 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 01 Apr 2020 01:54:35 GMT
EXPOSE 8086
# Wed, 01 Apr 2020 01:54:36 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:54:36 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:54:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 01 Apr 2020 01:54:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:54:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4bcc5089cfc4abd26d43bae2d2c33c09c6d28e4a17dd077dce04fea28ca336`  
		Last Modified: Wed, 01 Apr 2020 01:57:44 GMT  
		Size: 23.8 MB (23782721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c11e336a1b7f341621263386d698569b0ee7da3bf80644ffcf1c23604feb1aa`  
		Last Modified: Wed, 01 Apr 2020 01:57:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00427487b4d66de06a2814199e5a1d6df166deae45cdcdb8c7f33530bb072adf`  
		Last Modified: Wed, 01 Apr 2020 01:57:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302518573ca30d38a5b5d0ebb2d033cd556e139146a31b338ae63d6928a30c76`  
		Last Modified: Wed, 01 Apr 2020 01:57:37 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5-data-alpine`

```console
$ docker pull influxdb@sha256:de7ead51d90b0ea4853ef4d603cc9cc17b386d33d0d5273decaefeab25d0d86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:0a8e496ac00fb556392e252a47b047843e176c5f38a40160f86489ceb30825c8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28299789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe04106d38b3f3d171c1ce7f48100da80cc6d63d6ee14b0820f1a70f346f1eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:02 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Thu, 23 Jan 2020 19:04:07 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:07 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:04:07 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:04:07 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:07 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:07 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:04:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:08 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5636523728be94f8e3e0040b406697262e4b48fde6334e9ffe248d9082401`  
		Last Modified: Thu, 23 Jan 2020 19:07:30 GMT  
		Size: 23.7 MB (23670013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb8d0867f6a6f6d4a9d64a95b07f9cd2e1e8c961ec8b75c387a1967c89ec7ec`  
		Last Modified: Thu, 23 Jan 2020 19:07:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54826124424838ea73c4731f23548a42ad0693312df4b0399d1368d51c44562c`  
		Last Modified: Thu, 23 Jan 2020 19:07:15 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19b6aff30df100fd8085bb178fee7e62e0cc282b763decf56cecfe747642eed`  
		Last Modified: Thu, 23 Jan 2020 19:07:15 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5-meta`

```console
$ docker pull influxdb@sha256:5bfd60bbc406c6643e50ddfb55968622c5544c8628691836b3b11aa54fe9a6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:027adb9d4a762d0d725b0f85c36b56be106107232b535bac6632276093c19b0e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71710844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0c5b801dc9eaec676ab8d69e91a0be67cf9d71afe7bb01441b4867e8b9c6db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:54:29 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Wed, 01 Apr 2020 01:54:50 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 01 Apr 2020 01:54:50 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 01 Apr 2020 01:54:51 GMT
EXPOSE 8091
# Wed, 01 Apr 2020 01:54:51 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:54:51 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:54:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:54:52 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0654d384a3eaad7d7da44dff8a811ee19972a2a5eff023aa5e38472104c5b32`  
		Last Modified: Wed, 01 Apr 2020 01:57:52 GMT  
		Size: 11.2 MB (11194126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50519f5c2fce761a2758fd77bc990843edd93481b234cd4c969dfeaaca9e00b6`  
		Last Modified: Wed, 01 Apr 2020 01:57:49 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab1a71222e0e4e005972758a858e68a43d661c24d4407d0f5ba18fc7fe130e5`  
		Last Modified: Wed, 01 Apr 2020 01:57:49 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5-meta-alpine`

```console
$ docker pull influxdb@sha256:6f84ba5ba10c833d9cc14b9c36541ab9657d68f1a46303784a08b691fc381154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:77e862d69197c3b486eabc8170c199fa18dce5f81fc703d66f2fedba0d19eaf0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15779821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64e168fcf407e757b2ad9c3f9e73710a026bbe05be46a21f91d4aae930dcfa3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:02 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Thu, 23 Jan 2020 19:04:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:19 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 23 Jan 2020 19:04:19 GMT
EXPOSE 8091
# Thu, 23 Jan 2020 19:04:19 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:19 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:19 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0e87069833ff629f85d2e8945f09b6a5af9aacf30af70ff537adcb22b09772`  
		Last Modified: Thu, 23 Jan 2020 19:07:43 GMT  
		Size: 11.2 MB (11151245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab027e28e6d75a43518ff2cfe15764266fc70ff97d429bcaaa8fe936585e30f5`  
		Last Modified: Thu, 23 Jan 2020 19:07:35 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2836d507107845041948aa147917bdbd6177563dee7f77b1552983df73acc37`  
		Last Modified: Thu, 23 Jan 2020 19:07:35 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6`

```console
$ docker pull influxdb@sha256:fa24eaf1046345b9973500ecc6f2363f82876cd3e3617e6610544454dddcdd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.6` - linux; amd64

```console
$ docker pull influxdb@sha256:712cdf0f367b2dc2641b323acf10fde9497b437dfb94ddf3e7860adca31e0aef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85827193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126e586f79679027059922d0914ff62ec5c754cb75ced5c90880049c6bd6488d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:55:02 GMT
ENV INFLUXDB_VERSION=1.6.6
# Wed, 01 Apr 2020 01:55:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 01 Apr 2020 01:55:09 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 01 Apr 2020 01:55:09 GMT
EXPOSE 8086
# Wed, 01 Apr 2020 01:55:10 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:55:10 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:55:11 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 01 Apr 2020 01:55:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:55:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc788f9b26ac2c01fa1de681f450920a1ca8fae1e449f9860a2db1c4bfda5165`  
		Last Modified: Wed, 01 Apr 2020 01:58:05 GMT  
		Size: 25.3 MB (25309330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81375ed6922d5a570af9be243b2bae076cef06f3dc19183e9dbf176e4158f41`  
		Last Modified: Wed, 01 Apr 2020 01:57:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f2c22607e0ae9e279571c2b71c6f1290e422a43a44ca4cd972ba061cea1ffb`  
		Last Modified: Wed, 01 Apr 2020 01:57:57 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b0fb98e078b7d0e44a16c7a993c072cbb80aae155c6e735498545268565a0f`  
		Last Modified: Wed, 01 Apr 2020 01:57:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.6` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:9ab3c133791cbf6f759e2c4dc11f838059f2f32153257d2251ae2c5607d07c37
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79869354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1812f810717070dd50e1f276d38dcdf7b2025a4c83ad1783a30921e27f17b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:24 GMT
ADD file:b047b0c4dbfbcc048385195e807283b9386c4aac13a4841112cb3f76cd932b06 in / 
# Tue, 31 Mar 2020 01:52:26 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:53:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 23:27:41 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 23:28:10 GMT
ENV INFLUXDB_VERSION=1.6.6
# Tue, 31 Mar 2020 23:28:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 23:28:18 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 31 Mar 2020 23:28:19 GMT
EXPOSE 8086
# Tue, 31 Mar 2020 23:28:20 GMT
VOLUME [/var/lib/influxdb]
# Tue, 31 Mar 2020 23:28:21 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 31 Mar 2020 23:28:22 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 31 Mar 2020 23:28:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 23:28:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:eb3768893937e6b455f98cd8db65949a6aa5c54ebd94fca3039af9833187ce10`  
		Last Modified: Tue, 31 Mar 2020 01:59:52 GMT  
		Size: 42.1 MB (42100090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb68590923b075c8f49c4470341451f9d874afc84c5fc916278815a1064243`  
		Last Modified: Tue, 31 Mar 2020 04:04:43 GMT  
		Size: 9.5 MB (9498284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743981b4cf60d4ed8ddd6610e4d1d75256ddb63a7d83d540a96e1faf8ba8a315`  
		Last Modified: Tue, 31 Mar 2020 04:04:42 GMT  
		Size: 3.9 MB (3918805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39848df21e0940ce448bbc5a30bb53f1ae2d3a23b774be8add8462388496176d`  
		Last Modified: Tue, 31 Mar 2020 23:29:03 GMT  
		Size: 2.8 KB (2805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4280e1fc10fa476b320d4db5f411e54a45fe770f6e8ec935202d88dffa5f1ee`  
		Last Modified: Tue, 31 Mar 2020 23:29:25 GMT  
		Size: 24.3 MB (24347656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b999bfda899e1b5084f389b1709a0f23516a8687fa2e12ae4a208e2023216988`  
		Last Modified: Tue, 31 Mar 2020 23:29:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d1cce137c72a0806234b5b0373262776ace8334165e9848b2205d305429c9a`  
		Last Modified: Tue, 31 Mar 2020 23:29:18 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f72b3eca89b1dbcd7d5a2cf80d6d7087ba3be24cc1a5e52a085b2309fd7868`  
		Last Modified: Tue, 31 Mar 2020 23:29:17 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.6` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b50a77b1f84092aa359034e32993462ee05fb94656eb982bbd51a4d2c1e768fe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80670478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8031e809e7e45cfc429d7a175dca28f81a0dea83688f92a4d2702aceb444a93a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:21:37 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 21:21:54 GMT
ENV INFLUXDB_VERSION=1.6.6
# Tue, 31 Mar 2020 21:22:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 21:22:03 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 31 Mar 2020 21:22:03 GMT
EXPOSE 8086
# Tue, 31 Mar 2020 21:22:04 GMT
VOLUME [/var/lib/influxdb]
# Tue, 31 Mar 2020 21:22:04 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 31 Mar 2020 21:22:05 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 31 Mar 2020 21:22:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 21:22:06 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4b0dbd0d8c4ebbcb0bd21245e7f3bfa3f1dcaa045d058597cb38fd62aa3c95`  
		Last Modified: Tue, 31 Mar 2020 21:22:36 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475ce4d1ac35d8785f620e5b66167382bb8c8f7546427f54c97e6ff0211a5fb`  
		Last Modified: Tue, 31 Mar 2020 21:22:56 GMT  
		Size: 23.7 MB (23664987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8166bc522049f0e3a213fcae27fee94f6f67f606f82bea60d1ec8dbe9e5675`  
		Last Modified: Tue, 31 Mar 2020 21:22:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efebdc1f3cf9006dd1470abfa7712c2fad22dc75c7b59e92a9856c47c61adfd2`  
		Last Modified: Tue, 31 Mar 2020 21:22:48 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609bf9b695dd5f96868282c99574d029d659e3fbade1d07909decc6ea0ff398f`  
		Last Modified: Tue, 31 Mar 2020 21:22:48 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6.6`

```console
$ docker pull influxdb@sha256:fa24eaf1046345b9973500ecc6f2363f82876cd3e3617e6610544454dddcdd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.6.6` - linux; amd64

```console
$ docker pull influxdb@sha256:712cdf0f367b2dc2641b323acf10fde9497b437dfb94ddf3e7860adca31e0aef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85827193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126e586f79679027059922d0914ff62ec5c754cb75ced5c90880049c6bd6488d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:55:02 GMT
ENV INFLUXDB_VERSION=1.6.6
# Wed, 01 Apr 2020 01:55:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 01 Apr 2020 01:55:09 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 01 Apr 2020 01:55:09 GMT
EXPOSE 8086
# Wed, 01 Apr 2020 01:55:10 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:55:10 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:55:11 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 01 Apr 2020 01:55:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:55:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc788f9b26ac2c01fa1de681f450920a1ca8fae1e449f9860a2db1c4bfda5165`  
		Last Modified: Wed, 01 Apr 2020 01:58:05 GMT  
		Size: 25.3 MB (25309330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81375ed6922d5a570af9be243b2bae076cef06f3dc19183e9dbf176e4158f41`  
		Last Modified: Wed, 01 Apr 2020 01:57:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f2c22607e0ae9e279571c2b71c6f1290e422a43a44ca4cd972ba061cea1ffb`  
		Last Modified: Wed, 01 Apr 2020 01:57:57 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b0fb98e078b7d0e44a16c7a993c072cbb80aae155c6e735498545268565a0f`  
		Last Modified: Wed, 01 Apr 2020 01:57:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.6.6` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:9ab3c133791cbf6f759e2c4dc11f838059f2f32153257d2251ae2c5607d07c37
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79869354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1812f810717070dd50e1f276d38dcdf7b2025a4c83ad1783a30921e27f17b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:24 GMT
ADD file:b047b0c4dbfbcc048385195e807283b9386c4aac13a4841112cb3f76cd932b06 in / 
# Tue, 31 Mar 2020 01:52:26 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:53:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 23:27:41 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 23:28:10 GMT
ENV INFLUXDB_VERSION=1.6.6
# Tue, 31 Mar 2020 23:28:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 23:28:18 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 31 Mar 2020 23:28:19 GMT
EXPOSE 8086
# Tue, 31 Mar 2020 23:28:20 GMT
VOLUME [/var/lib/influxdb]
# Tue, 31 Mar 2020 23:28:21 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 31 Mar 2020 23:28:22 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 31 Mar 2020 23:28:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 23:28:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:eb3768893937e6b455f98cd8db65949a6aa5c54ebd94fca3039af9833187ce10`  
		Last Modified: Tue, 31 Mar 2020 01:59:52 GMT  
		Size: 42.1 MB (42100090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb68590923b075c8f49c4470341451f9d874afc84c5fc916278815a1064243`  
		Last Modified: Tue, 31 Mar 2020 04:04:43 GMT  
		Size: 9.5 MB (9498284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743981b4cf60d4ed8ddd6610e4d1d75256ddb63a7d83d540a96e1faf8ba8a315`  
		Last Modified: Tue, 31 Mar 2020 04:04:42 GMT  
		Size: 3.9 MB (3918805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39848df21e0940ce448bbc5a30bb53f1ae2d3a23b774be8add8462388496176d`  
		Last Modified: Tue, 31 Mar 2020 23:29:03 GMT  
		Size: 2.8 KB (2805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4280e1fc10fa476b320d4db5f411e54a45fe770f6e8ec935202d88dffa5f1ee`  
		Last Modified: Tue, 31 Mar 2020 23:29:25 GMT  
		Size: 24.3 MB (24347656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b999bfda899e1b5084f389b1709a0f23516a8687fa2e12ae4a208e2023216988`  
		Last Modified: Tue, 31 Mar 2020 23:29:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d1cce137c72a0806234b5b0373262776ace8334165e9848b2205d305429c9a`  
		Last Modified: Tue, 31 Mar 2020 23:29:18 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f72b3eca89b1dbcd7d5a2cf80d6d7087ba3be24cc1a5e52a085b2309fd7868`  
		Last Modified: Tue, 31 Mar 2020 23:29:17 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.6.6` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b50a77b1f84092aa359034e32993462ee05fb94656eb982bbd51a4d2c1e768fe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80670478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8031e809e7e45cfc429d7a175dca28f81a0dea83688f92a4d2702aceb444a93a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:21:37 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 21:21:54 GMT
ENV INFLUXDB_VERSION=1.6.6
# Tue, 31 Mar 2020 21:22:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 21:22:03 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 31 Mar 2020 21:22:03 GMT
EXPOSE 8086
# Tue, 31 Mar 2020 21:22:04 GMT
VOLUME [/var/lib/influxdb]
# Tue, 31 Mar 2020 21:22:04 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 31 Mar 2020 21:22:05 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 31 Mar 2020 21:22:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 21:22:06 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4b0dbd0d8c4ebbcb0bd21245e7f3bfa3f1dcaa045d058597cb38fd62aa3c95`  
		Last Modified: Tue, 31 Mar 2020 21:22:36 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475ce4d1ac35d8785f620e5b66167382bb8c8f7546427f54c97e6ff0211a5fb`  
		Last Modified: Tue, 31 Mar 2020 21:22:56 GMT  
		Size: 23.7 MB (23664987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8166bc522049f0e3a213fcae27fee94f6f67f606f82bea60d1ec8dbe9e5675`  
		Last Modified: Tue, 31 Mar 2020 21:22:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efebdc1f3cf9006dd1470abfa7712c2fad22dc75c7b59e92a9856c47c61adfd2`  
		Last Modified: Tue, 31 Mar 2020 21:22:48 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609bf9b695dd5f96868282c99574d029d659e3fbade1d07909decc6ea0ff398f`  
		Last Modified: Tue, 31 Mar 2020 21:22:48 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6.6-alpine`

```console
$ docker pull influxdb@sha256:e60ab84cd8ec29d78b5d521599d8b301412c786688a6fe20b220af841ac7e39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6.6-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5e4e97a593880e8a87bb23aa3639f9f670e09e9b7a270a2506b7e0a060a2fb90
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29819765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895b69188094ed510263d77a311bbf4ddafabbb163e03b87fcfd530b74259420`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:28 GMT
ENV INFLUXDB_VERSION=1.6.6
# Thu, 23 Jan 2020 19:04:34 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:35 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:04:35 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:04:35 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:36 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:04:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:36 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a151a3c263ad506526e5130f4a8bbc2235448102aa0718108b3ccb238f11a5`  
		Last Modified: Thu, 23 Jan 2020 19:08:04 GMT  
		Size: 25.2 MB (25190045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a05f89f09d0ed1cfaf52247a8db617df8e97f3741004b646cf0208f7b469f5c`  
		Last Modified: Thu, 23 Jan 2020 19:07:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d98e03916bb6aad744b9c054a966c996532b8a1c962c1a891b143fe2fb3a4cd`  
		Last Modified: Thu, 23 Jan 2020 19:07:49 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744cc3d6ebb5f7879f04721c401125f0f4ec928e5c6b9f040add9cde29397359`  
		Last Modified: Thu, 23 Jan 2020 19:07:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6.6-data`

```console
$ docker pull influxdb@sha256:bd89e17b6862654717bd929f9e6e3ab9447ff11fed644da0d2246c859dd4cb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6.6-data` - linux; amd64

```console
$ docker pull influxdb@sha256:96392345e2d465657d3940863c78533644411cf985fac5d95ce6b27cf0ad618d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87090007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c079006a436ea341b5099a1b79b5a25b2069636f7f2d33348938b716ac02b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:55:23 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Wed, 01 Apr 2020 01:55:28 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 01 Apr 2020 01:55:29 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 01 Apr 2020 01:55:29 GMT
EXPOSE 8086
# Wed, 01 Apr 2020 01:55:30 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:55:30 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:55:30 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 01 Apr 2020 01:55:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:55:31 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c7c721dcc5de6530d0f909a28d1a52524f90eb47343cb5c1fd843b2c82f2b`  
		Last Modified: Wed, 01 Apr 2020 01:58:17 GMT  
		Size: 26.6 MB (26572086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f168b45b74f200ce321daa878dd49c8711c924165d7b44d6457ba1349deede`  
		Last Modified: Wed, 01 Apr 2020 01:58:10 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c41e29406af0345d4c36f5f76fe1ac1b83db5b35ce761227a349bd5674d17c2`  
		Last Modified: Wed, 01 Apr 2020 01:58:10 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10502195f0e6b257f828ca176ce39d6a87c11a63ae379b72acd97110448ccf1c`  
		Last Modified: Wed, 01 Apr 2020 01:58:10 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6.6-data-alpine`

```console
$ docker pull influxdb@sha256:f51fc6d7713bdc8f2c15aab1d51be52000e011625035b8ee98855070f3b1c49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6.6-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2de0016b2ef4b8b3aae9e18bbbd0c69ce264fa1c040d664c84f148ebca5e5c5b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31082210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b7416db022c81033acdb0769f087d71797e95be591ae5221e065852079f4cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:45 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Thu, 23 Jan 2020 19:04:52 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:52 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:04:52 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:04:53 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:53 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:53 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:04:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee5a3c7ffbad06c5f2dc9cbdfe7d7f7e2dfb86669ad668682a7b447f26482a6`  
		Last Modified: Thu, 23 Jan 2020 19:08:18 GMT  
		Size: 26.5 MB (26452432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3809d3ef5db1ec9ee254ae86da4919cd2106320ad70c4079ec13e747bcf4e9d0`  
		Last Modified: Thu, 23 Jan 2020 19:08:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68df561574e02cac655e37af87f36eec1442e47592ec23533456764749f6b08c`  
		Last Modified: Thu, 23 Jan 2020 19:08:10 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c80f847536ae5085e3e2437ca2d567776548c98d908624546cb808d76967bc`  
		Last Modified: Thu, 23 Jan 2020 19:08:10 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6.6-meta`

```console
$ docker pull influxdb@sha256:6c7d37c9cddeb269da9cf0cbb3c243608cd4502b7e7d0a25f682ad0f59190f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6.6-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:f01dc5990e4bc7b291a140d5ce68bd4d840371fea8135c5518f621b9f5f9c2ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73065871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3382645d3b799bfb231ec21fa24a97683b2e906566970cc5cec356c447a13a99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:55:23 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Wed, 01 Apr 2020 01:55:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 01 Apr 2020 01:55:45 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 01 Apr 2020 01:55:46 GMT
EXPOSE 8091
# Wed, 01 Apr 2020 01:55:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:55:47 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:55:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:55:47 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255fead21f054f94e3eb4f552c9bb8c242d79a849a786fd732c61612624a8526`  
		Last Modified: Wed, 01 Apr 2020 01:58:26 GMT  
		Size: 12.5 MB (12549153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6183626a6903e3e322142d44b191818868f355fe4a8bc80bae9472dfd1437e`  
		Last Modified: Wed, 01 Apr 2020 01:58:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237c836b032f5c6d4e2f3eb72733e53a4ae345791a5f62d1f916f29eb82abe03`  
		Last Modified: Wed, 01 Apr 2020 01:58:23 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6.6-meta-alpine`

```console
$ docker pull influxdb@sha256:f61c44d51eaa6cb19ce9e9d843ea7af742638550865de9c520bfe2830a4843c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6.6-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:df5bfa4f8a27751e5982ad0204f65a2890e507185996dd5910501655429d84e0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17133215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636882454a88a2ac32cb337b9cea0a68e6213fea058dadd5e2594b1859f76e19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:45 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Thu, 23 Jan 2020 19:05:07 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:05:07 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 23 Jan 2020 19:05:08 GMT
EXPOSE 8091
# Thu, 23 Jan 2020 19:05:08 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:05:08 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:05:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:05:09 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1444ac986dfc2da3021e80d7f77108c243e6dd5fdc69f2fb00c7db43659f982b`  
		Last Modified: Thu, 23 Jan 2020 19:08:32 GMT  
		Size: 12.5 MB (12504639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d95a63d52ff0d2fd2bcff5cdd2bd5d68cf7aa680a6d1f465a4bb7041ff7b0`  
		Last Modified: Thu, 23 Jan 2020 19:08:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefc3206ef8d05db423379f56204ab63424a340f63f75fa7864d04550fa15922`  
		Last Modified: Thu, 23 Jan 2020 19:08:24 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6-alpine`

```console
$ docker pull influxdb@sha256:e60ab84cd8ec29d78b5d521599d8b301412c786688a6fe20b220af841ac7e39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5e4e97a593880e8a87bb23aa3639f9f670e09e9b7a270a2506b7e0a060a2fb90
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29819765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895b69188094ed510263d77a311bbf4ddafabbb163e03b87fcfd530b74259420`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:28 GMT
ENV INFLUXDB_VERSION=1.6.6
# Thu, 23 Jan 2020 19:04:34 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:35 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:04:35 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:04:35 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:36 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:04:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:36 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a151a3c263ad506526e5130f4a8bbc2235448102aa0718108b3ccb238f11a5`  
		Last Modified: Thu, 23 Jan 2020 19:08:04 GMT  
		Size: 25.2 MB (25190045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a05f89f09d0ed1cfaf52247a8db617df8e97f3741004b646cf0208f7b469f5c`  
		Last Modified: Thu, 23 Jan 2020 19:07:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d98e03916bb6aad744b9c054a966c996532b8a1c962c1a891b143fe2fb3a4cd`  
		Last Modified: Thu, 23 Jan 2020 19:07:49 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744cc3d6ebb5f7879f04721c401125f0f4ec928e5c6b9f040add9cde29397359`  
		Last Modified: Thu, 23 Jan 2020 19:07:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6-data`

```console
$ docker pull influxdb@sha256:bd89e17b6862654717bd929f9e6e3ab9447ff11fed644da0d2246c859dd4cb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6-data` - linux; amd64

```console
$ docker pull influxdb@sha256:96392345e2d465657d3940863c78533644411cf985fac5d95ce6b27cf0ad618d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87090007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c079006a436ea341b5099a1b79b5a25b2069636f7f2d33348938b716ac02b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:55:23 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Wed, 01 Apr 2020 01:55:28 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 01 Apr 2020 01:55:29 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 01 Apr 2020 01:55:29 GMT
EXPOSE 8086
# Wed, 01 Apr 2020 01:55:30 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:55:30 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:55:30 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 01 Apr 2020 01:55:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:55:31 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061c7c721dcc5de6530d0f909a28d1a52524f90eb47343cb5c1fd843b2c82f2b`  
		Last Modified: Wed, 01 Apr 2020 01:58:17 GMT  
		Size: 26.6 MB (26572086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f168b45b74f200ce321daa878dd49c8711c924165d7b44d6457ba1349deede`  
		Last Modified: Wed, 01 Apr 2020 01:58:10 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c41e29406af0345d4c36f5f76fe1ac1b83db5b35ce761227a349bd5674d17c2`  
		Last Modified: Wed, 01 Apr 2020 01:58:10 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10502195f0e6b257f828ca176ce39d6a87c11a63ae379b72acd97110448ccf1c`  
		Last Modified: Wed, 01 Apr 2020 01:58:10 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6-data-alpine`

```console
$ docker pull influxdb@sha256:f51fc6d7713bdc8f2c15aab1d51be52000e011625035b8ee98855070f3b1c49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2de0016b2ef4b8b3aae9e18bbbd0c69ce264fa1c040d664c84f148ebca5e5c5b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31082210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b7416db022c81033acdb0769f087d71797e95be591ae5221e065852079f4cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:45 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Thu, 23 Jan 2020 19:04:52 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:52 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:04:52 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:04:53 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:53 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:53 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:04:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee5a3c7ffbad06c5f2dc9cbdfe7d7f7e2dfb86669ad668682a7b447f26482a6`  
		Last Modified: Thu, 23 Jan 2020 19:08:18 GMT  
		Size: 26.5 MB (26452432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3809d3ef5db1ec9ee254ae86da4919cd2106320ad70c4079ec13e747bcf4e9d0`  
		Last Modified: Thu, 23 Jan 2020 19:08:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68df561574e02cac655e37af87f36eec1442e47592ec23533456764749f6b08c`  
		Last Modified: Thu, 23 Jan 2020 19:08:10 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c80f847536ae5085e3e2437ca2d567776548c98d908624546cb808d76967bc`  
		Last Modified: Thu, 23 Jan 2020 19:08:10 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6-meta`

```console
$ docker pull influxdb@sha256:6c7d37c9cddeb269da9cf0cbb3c243608cd4502b7e7d0a25f682ad0f59190f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:f01dc5990e4bc7b291a140d5ce68bd4d840371fea8135c5518f621b9f5f9c2ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73065871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3382645d3b799bfb231ec21fa24a97683b2e906566970cc5cec356c447a13a99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:55:23 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Wed, 01 Apr 2020 01:55:45 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 01 Apr 2020 01:55:45 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 01 Apr 2020 01:55:46 GMT
EXPOSE 8091
# Wed, 01 Apr 2020 01:55:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:55:47 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:55:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:55:47 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255fead21f054f94e3eb4f552c9bb8c242d79a849a786fd732c61612624a8526`  
		Last Modified: Wed, 01 Apr 2020 01:58:26 GMT  
		Size: 12.5 MB (12549153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6183626a6903e3e322142d44b191818868f355fe4a8bc80bae9472dfd1437e`  
		Last Modified: Wed, 01 Apr 2020 01:58:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237c836b032f5c6d4e2f3eb72733e53a4ae345791a5f62d1f916f29eb82abe03`  
		Last Modified: Wed, 01 Apr 2020 01:58:23 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6-meta-alpine`

```console
$ docker pull influxdb@sha256:f61c44d51eaa6cb19ce9e9d843ea7af742638550865de9c520bfe2830a4843c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:df5bfa4f8a27751e5982ad0204f65a2890e507185996dd5910501655429d84e0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17133215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636882454a88a2ac32cb337b9cea0a68e6213fea058dadd5e2594b1859f76e19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:45 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Thu, 23 Jan 2020 19:05:07 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:05:07 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 23 Jan 2020 19:05:08 GMT
EXPOSE 8091
# Thu, 23 Jan 2020 19:05:08 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:05:08 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:05:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:05:09 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1444ac986dfc2da3021e80d7f77108c243e6dd5fdc69f2fb00c7db43659f982b`  
		Last Modified: Thu, 23 Jan 2020 19:08:32 GMT  
		Size: 12.5 MB (12504639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d95a63d52ff0d2fd2bcff5cdd2bd5d68cf7aa680a6d1f465a4bb7041ff7b0`  
		Last Modified: Thu, 23 Jan 2020 19:08:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefc3206ef8d05db423379f56204ab63424a340f63f75fa7864d04550fa15922`  
		Last Modified: Thu, 23 Jan 2020 19:08:24 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7`

```console
$ docker pull influxdb@sha256:f13ba72e09d89185e0901110c0ab2b457ff568af54a0956da0ad66fafcae0bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7` - linux; amd64

```console
$ docker pull influxdb@sha256:f38f5d7eff02d10c48801791ef741286468270f28af1d39ce5c4921f4ec13d7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124614816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88696c3ec771f302ff25ca7253787cce05bfdea4e2781f9731e0c9f7eec8a71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:55:58 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 01 Apr 2020 01:56:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 01 Apr 2020 01:56:08 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 01 Apr 2020 01:56:08 GMT
EXPOSE 8086
# Wed, 01 Apr 2020 01:56:08 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:56:09 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:56:09 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 01 Apr 2020 01:56:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:56:10 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1b96554da0ba8fcedde11aca5ec97c822615cb990dfbe923257e0ab03330d1`  
		Last Modified: Wed, 01 Apr 2020 01:58:43 GMT  
		Size: 64.1 MB (64096952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4724d32515be80c17a780b3b6f524a57f9548f535808a64d68c4214acb07dc15`  
		Last Modified: Wed, 01 Apr 2020 01:58:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d110c7dfc9268d676588ca2e5bc12c321350ef95659e3f22d6e3bc09a6c14f15`  
		Last Modified: Wed, 01 Apr 2020 01:58:30 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4ab55e07b667296f3c75f644a74d686647a99f6bc5824b94e8cb8fc6e08ae0`  
		Last Modified: Wed, 01 Apr 2020 01:58:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:420077e21d5d71d6008012a9f5cb54233234212c9445f745d57d66f1773de75e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116157240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90850b57f992fe74c09d6ce972a3c19673a66869bf26086cb5486a055fcad677`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:24 GMT
ADD file:b047b0c4dbfbcc048385195e807283b9386c4aac13a4841112cb3f76cd932b06 in / 
# Tue, 31 Mar 2020 01:52:26 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:53:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 23:27:41 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 23:28:33 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 31 Mar 2020 23:28:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 23:28:45 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 31 Mar 2020 23:28:46 GMT
EXPOSE 8086
# Tue, 31 Mar 2020 23:28:46 GMT
VOLUME [/var/lib/influxdb]
# Tue, 31 Mar 2020 23:28:48 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 31 Mar 2020 23:28:49 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 31 Mar 2020 23:28:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 23:28:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:eb3768893937e6b455f98cd8db65949a6aa5c54ebd94fca3039af9833187ce10`  
		Last Modified: Tue, 31 Mar 2020 01:59:52 GMT  
		Size: 42.1 MB (42100090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb68590923b075c8f49c4470341451f9d874afc84c5fc916278815a1064243`  
		Last Modified: Tue, 31 Mar 2020 04:04:43 GMT  
		Size: 9.5 MB (9498284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743981b4cf60d4ed8ddd6610e4d1d75256ddb63a7d83d540a96e1faf8ba8a315`  
		Last Modified: Tue, 31 Mar 2020 04:04:42 GMT  
		Size: 3.9 MB (3918805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39848df21e0940ce448bbc5a30bb53f1ae2d3a23b774be8add8462388496176d`  
		Last Modified: Tue, 31 Mar 2020 23:29:03 GMT  
		Size: 2.8 KB (2805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cdec4d9877a345bd4d0eeed63fc6032d748c105ecbd8cfe24f7def1fe99323`  
		Last Modified: Tue, 31 Mar 2020 23:29:49 GMT  
		Size: 60.6 MB (60635541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f487a5278dbc614e551e4b5a518dfec2009aeecdafb33b4dd5d336971a3868`  
		Last Modified: Tue, 31 Mar 2020 23:29:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0ccb10615426229fede770a8a9010d5cbc01475511e9c6c46d6b4ac01f2f9f`  
		Last Modified: Tue, 31 Mar 2020 23:29:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6ab3423dee06091a4fbb44d97ba75aa5acea4e04b5d2b97c7bebc9fc6b3ed2`  
		Last Modified: Tue, 31 Mar 2020 23:29:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bd16c6f810d30776080f1d3f0c9478f757343e02b8ebb5e8909f786a7c26b53b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117133230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c8d6bd59e1d1f008c13f43d538a228f8edbea59366c83b31d0309c741cb53d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:21:37 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 21:22:11 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 31 Mar 2020 21:22:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 21:22:21 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 31 Mar 2020 21:22:22 GMT
EXPOSE 8086
# Tue, 31 Mar 2020 21:22:22 GMT
VOLUME [/var/lib/influxdb]
# Tue, 31 Mar 2020 21:22:23 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 31 Mar 2020 21:22:23 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 31 Mar 2020 21:22:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 21:22:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4b0dbd0d8c4ebbcb0bd21245e7f3bfa3f1dcaa045d058597cb38fd62aa3c95`  
		Last Modified: Tue, 31 Mar 2020 21:22:36 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5955d9f7eca8b5aedca7a39fd5077979902b985ab851573a57cd3f07b9b6b079`  
		Last Modified: Tue, 31 Mar 2020 21:23:18 GMT  
		Size: 60.1 MB (60127737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07da9d58eae83ad8c7679b533d4869b03ed814eb1f50baa63a6c6367f183c0a5`  
		Last Modified: Tue, 31 Mar 2020 21:23:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a529b6b5daf8c8a3986f7328c65f4e672d7a6874892668539b39a0aa26ac92`  
		Last Modified: Tue, 31 Mar 2020 21:23:02 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a294964f2e9d24cd7e2bb755c6eb40d422d255796caa521bd38ce0624d75ea7e`  
		Last Modified: Tue, 31 Mar 2020 21:23:02 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10`

```console
$ docker pull influxdb@sha256:f13ba72e09d89185e0901110c0ab2b457ff568af54a0956da0ad66fafcae0bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7.10` - linux; amd64

```console
$ docker pull influxdb@sha256:f38f5d7eff02d10c48801791ef741286468270f28af1d39ce5c4921f4ec13d7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124614816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88696c3ec771f302ff25ca7253787cce05bfdea4e2781f9731e0c9f7eec8a71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:55:58 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 01 Apr 2020 01:56:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 01 Apr 2020 01:56:08 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 01 Apr 2020 01:56:08 GMT
EXPOSE 8086
# Wed, 01 Apr 2020 01:56:08 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:56:09 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:56:09 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 01 Apr 2020 01:56:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:56:10 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1b96554da0ba8fcedde11aca5ec97c822615cb990dfbe923257e0ab03330d1`  
		Last Modified: Wed, 01 Apr 2020 01:58:43 GMT  
		Size: 64.1 MB (64096952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4724d32515be80c17a780b3b6f524a57f9548f535808a64d68c4214acb07dc15`  
		Last Modified: Wed, 01 Apr 2020 01:58:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d110c7dfc9268d676588ca2e5bc12c321350ef95659e3f22d6e3bc09a6c14f15`  
		Last Modified: Wed, 01 Apr 2020 01:58:30 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4ab55e07b667296f3c75f644a74d686647a99f6bc5824b94e8cb8fc6e08ae0`  
		Last Modified: Wed, 01 Apr 2020 01:58:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.10` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:420077e21d5d71d6008012a9f5cb54233234212c9445f745d57d66f1773de75e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116157240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90850b57f992fe74c09d6ce972a3c19673a66869bf26086cb5486a055fcad677`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:24 GMT
ADD file:b047b0c4dbfbcc048385195e807283b9386c4aac13a4841112cb3f76cd932b06 in / 
# Tue, 31 Mar 2020 01:52:26 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:53:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 23:27:41 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 23:28:33 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 31 Mar 2020 23:28:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 23:28:45 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 31 Mar 2020 23:28:46 GMT
EXPOSE 8086
# Tue, 31 Mar 2020 23:28:46 GMT
VOLUME [/var/lib/influxdb]
# Tue, 31 Mar 2020 23:28:48 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 31 Mar 2020 23:28:49 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 31 Mar 2020 23:28:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 23:28:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:eb3768893937e6b455f98cd8db65949a6aa5c54ebd94fca3039af9833187ce10`  
		Last Modified: Tue, 31 Mar 2020 01:59:52 GMT  
		Size: 42.1 MB (42100090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb68590923b075c8f49c4470341451f9d874afc84c5fc916278815a1064243`  
		Last Modified: Tue, 31 Mar 2020 04:04:43 GMT  
		Size: 9.5 MB (9498284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743981b4cf60d4ed8ddd6610e4d1d75256ddb63a7d83d540a96e1faf8ba8a315`  
		Last Modified: Tue, 31 Mar 2020 04:04:42 GMT  
		Size: 3.9 MB (3918805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39848df21e0940ce448bbc5a30bb53f1ae2d3a23b774be8add8462388496176d`  
		Last Modified: Tue, 31 Mar 2020 23:29:03 GMT  
		Size: 2.8 KB (2805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cdec4d9877a345bd4d0eeed63fc6032d748c105ecbd8cfe24f7def1fe99323`  
		Last Modified: Tue, 31 Mar 2020 23:29:49 GMT  
		Size: 60.6 MB (60635541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f487a5278dbc614e551e4b5a518dfec2009aeecdafb33b4dd5d336971a3868`  
		Last Modified: Tue, 31 Mar 2020 23:29:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0ccb10615426229fede770a8a9010d5cbc01475511e9c6c46d6b4ac01f2f9f`  
		Last Modified: Tue, 31 Mar 2020 23:29:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6ab3423dee06091a4fbb44d97ba75aa5acea4e04b5d2b97c7bebc9fc6b3ed2`  
		Last Modified: Tue, 31 Mar 2020 23:29:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.10` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bd16c6f810d30776080f1d3f0c9478f757343e02b8ebb5e8909f786a7c26b53b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117133230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c8d6bd59e1d1f008c13f43d538a228f8edbea59366c83b31d0309c741cb53d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:21:37 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 21:22:11 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 31 Mar 2020 21:22:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 21:22:21 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 31 Mar 2020 21:22:22 GMT
EXPOSE 8086
# Tue, 31 Mar 2020 21:22:22 GMT
VOLUME [/var/lib/influxdb]
# Tue, 31 Mar 2020 21:22:23 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 31 Mar 2020 21:22:23 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 31 Mar 2020 21:22:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 21:22:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4b0dbd0d8c4ebbcb0bd21245e7f3bfa3f1dcaa045d058597cb38fd62aa3c95`  
		Last Modified: Tue, 31 Mar 2020 21:22:36 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5955d9f7eca8b5aedca7a39fd5077979902b985ab851573a57cd3f07b9b6b079`  
		Last Modified: Tue, 31 Mar 2020 21:23:18 GMT  
		Size: 60.1 MB (60127737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07da9d58eae83ad8c7679b533d4869b03ed814eb1f50baa63a6c6367f183c0a5`  
		Last Modified: Tue, 31 Mar 2020 21:23:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a529b6b5daf8c8a3986f7328c65f4e672d7a6874892668539b39a0aa26ac92`  
		Last Modified: Tue, 31 Mar 2020 21:23:02 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a294964f2e9d24cd7e2bb755c6eb40d422d255796caa521bd38ce0624d75ea7e`  
		Last Modified: Tue, 31 Mar 2020 21:23:02 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-alpine`

```console
$ docker pull influxdb@sha256:db1bbd2776aa7a8c3b089f7b32b80765c90b49179dadd89aac423bc0ec7c33af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:213f19092ddac0e75e1709ce6f687c29428ecf7fd57f24bf2043e662299d7552
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68521230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11022dc8112fc93d26bcb9d7c4bcac7f115b57890fff650d8a29afdd735cecd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 25 Feb 2020 01:21:50 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 25 Feb 2020 01:21:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 25 Feb 2020 01:21:57 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 25 Feb 2020 01:21:57 GMT
EXPOSE 8086
# Tue, 25 Feb 2020 01:21:57 GMT
VOLUME [/var/lib/influxdb]
# Tue, 25 Feb 2020 01:21:58 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 25 Feb 2020 01:21:58 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 25 Feb 2020 01:21:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2020 01:21:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596f24252014ca2dc760ecf20947aa59bdc752a4014062a15767913edcfe75a8`  
		Last Modified: Tue, 25 Feb 2020 01:23:29 GMT  
		Size: 63.9 MB (63891510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0104a2d9f4d8ca1e1bed307f4828e96ebe4dbf18e73b76353fd5c73b32387de2`  
		Last Modified: Tue, 25 Feb 2020 01:23:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ff92f4e9a9184c2a500f4c39aefd1cbf9dfb0353e7160d3ac1cf7acd7a349`  
		Last Modified: Tue, 25 Feb 2020 01:23:20 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94535d69e85267353aff6b49fafc3df78032a03d78bb42b256539b5a3faee6b`  
		Last Modified: Tue, 25 Feb 2020 01:23:20 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-data`

```console
$ docker pull influxdb@sha256:c856417e9723c589231b4d0b004c3bf3e0313305c443cc3d931a136df5ebabe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data` - linux; amd64

```console
$ docker pull influxdb@sha256:696813b3b0bc79d23915cb139cf17c5b4383fdfc2c08194071532bf8999930fe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148430199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c460f5b2836aa43e5b014960a8b050afa145435a304cfed3c479d49dc129b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:56:21 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 01 Apr 2020 01:56:30 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 01 Apr 2020 01:56:30 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 01 Apr 2020 01:56:30 GMT
EXPOSE 8086
# Wed, 01 Apr 2020 01:56:30 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:56:31 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:56:31 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 01 Apr 2020 01:56:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:56:31 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ef5fa9a7ce28c6f0473c3dab607d519420a639380420a279b6b399bf0d84fd`  
		Last Modified: Wed, 01 Apr 2020 01:59:07 GMT  
		Size: 87.9 MB (87912277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27777eba072e66d34253efc0ef7f4dfee89724a6e7306dfd17738d044cc79323`  
		Last Modified: Wed, 01 Apr 2020 01:58:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c634d2bef7c851e277d29a77a3f198db0bf52dda488d784116f336aa0b799fe6`  
		Last Modified: Wed, 01 Apr 2020 01:58:50 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8525dd5fc4d8587bdb1363e3afc7201f8c0cd91e33cb721c8ababa8fa129835e`  
		Last Modified: Wed, 01 Apr 2020 01:58:50 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-data-alpine`

```console
$ docker pull influxdb@sha256:ade2ee58127f17cd42846484f06c6014e66bdd3a9ecf563aa4e153c60e7187b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ad50898a5f3cd3a5d0bfdd9231111e803fdbbdd838eae3e7e08d1163b438cb82
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92299087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84763cde3a71238942846a39a4887c2a16be13a2ded02dd2689359d5220fd8a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 25 Feb 2020 01:22:18 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Tue, 25 Feb 2020 01:22:27 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 25 Feb 2020 01:22:28 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 25 Feb 2020 01:22:28 GMT
EXPOSE 8086
# Tue, 25 Feb 2020 01:22:29 GMT
VOLUME [/var/lib/influxdb]
# Tue, 25 Feb 2020 01:22:29 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 25 Feb 2020 01:22:29 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 25 Feb 2020 01:22:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2020 01:22:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c9c59b5d2a9ea8da3c7e9548176b7c5d650f93dce7c1b678292f3ee5aa6f77`  
		Last Modified: Tue, 25 Feb 2020 01:24:06 GMT  
		Size: 87.7 MB (87669308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e7409222c3f0694c6261c8c439680a1073c32c20f080787e63224b56d680e3`  
		Last Modified: Tue, 25 Feb 2020 01:23:53 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0d21ddf433669aae470cc2243fb53317d67c10b3b506d1ec7288bf5cf58f2b`  
		Last Modified: Tue, 25 Feb 2020 01:23:53 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750af7d287a00fdb813a7d85b77b1ea371b943de38a98408b1afef8e0b43035a`  
		Last Modified: Tue, 25 Feb 2020 01:23:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-meta`

```console
$ docker pull influxdb@sha256:35b2fb03ab27b23cda5b78ace63f5b30c1765cb8716a1fe6f57aa52a64d96378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8cc8420079d23b6af7eda2fa74bf79f2165f2c9b2bddebf0b7b8003479b0b666
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83649352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f24934d73750209464f0080e2475a3694f6cc672e9b8e69b18597915b26d64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:56:21 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 01 Apr 2020 01:56:44 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 01 Apr 2020 01:56:45 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 01 Apr 2020 01:56:45 GMT
EXPOSE 8091
# Wed, 01 Apr 2020 01:56:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:56:46 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:56:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:56:47 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325f69af8a622017dc6a68abe33842d1beb8e02c13a750e2e6e2f76b93457138`  
		Last Modified: Wed, 01 Apr 2020 01:59:19 GMT  
		Size: 23.1 MB (23132633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d3f9ce723fce8ed7d741079028754f50c668f60f69c4d3d908fc9bae7c895e`  
		Last Modified: Wed, 01 Apr 2020 01:59:14 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a189662bb7c84e17a1c76056bf221af9c1234aa02d29ee27e2db8a390b0542`  
		Last Modified: Wed, 01 Apr 2020 01:59:15 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.10-meta-alpine`

```console
$ docker pull influxdb@sha256:935f23f3eeb2a62b0f56b0fb8a301832fa58a46b39e086b63a8bba73bf2d50d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.10-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7eb37763f5ab368fba1e10479811f58ededd3693e5a204003be5700423b2eb45
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27694267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e87a59d350cbcf0fbb8662e04824c54057297c4d35182555d0eedcf77e46099`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 25 Feb 2020 01:22:18 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Tue, 25 Feb 2020 01:22:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 25 Feb 2020 01:22:46 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 25 Feb 2020 01:22:47 GMT
EXPOSE 8091
# Tue, 25 Feb 2020 01:22:47 GMT
VOLUME [/var/lib/influxdb]
# Tue, 25 Feb 2020 01:22:47 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 25 Feb 2020 01:22:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2020 01:22:47 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391ad404de14e9eb4440bd3e91c95c9b876e6216d32c357b488b7c85388e7255`  
		Last Modified: Tue, 25 Feb 2020 01:24:22 GMT  
		Size: 23.1 MB (23065691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09da99d11e68e36fd2aeb608ec27f778a57a27e712b2c89abb183bc36991f6bc`  
		Last Modified: Tue, 25 Feb 2020 01:24:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6ea3b07bb562ab605a9a2023f069c6131458e25f15e392785f126b2db62250`  
		Last Modified: Tue, 25 Feb 2020 01:24:19 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-alpine`

```console
$ docker pull influxdb@sha256:db1bbd2776aa7a8c3b089f7b32b80765c90b49179dadd89aac423bc0ec7c33af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:213f19092ddac0e75e1709ce6f687c29428ecf7fd57f24bf2043e662299d7552
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68521230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11022dc8112fc93d26bcb9d7c4bcac7f115b57890fff650d8a29afdd735cecd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 25 Feb 2020 01:21:50 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 25 Feb 2020 01:21:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 25 Feb 2020 01:21:57 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 25 Feb 2020 01:21:57 GMT
EXPOSE 8086
# Tue, 25 Feb 2020 01:21:57 GMT
VOLUME [/var/lib/influxdb]
# Tue, 25 Feb 2020 01:21:58 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 25 Feb 2020 01:21:58 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 25 Feb 2020 01:21:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2020 01:21:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596f24252014ca2dc760ecf20947aa59bdc752a4014062a15767913edcfe75a8`  
		Last Modified: Tue, 25 Feb 2020 01:23:29 GMT  
		Size: 63.9 MB (63891510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0104a2d9f4d8ca1e1bed307f4828e96ebe4dbf18e73b76353fd5c73b32387de2`  
		Last Modified: Tue, 25 Feb 2020 01:23:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ff92f4e9a9184c2a500f4c39aefd1cbf9dfb0353e7160d3ac1cf7acd7a349`  
		Last Modified: Tue, 25 Feb 2020 01:23:20 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94535d69e85267353aff6b49fafc3df78032a03d78bb42b256539b5a3faee6b`  
		Last Modified: Tue, 25 Feb 2020 01:23:20 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data`

```console
$ docker pull influxdb@sha256:c856417e9723c589231b4d0b004c3bf3e0313305c443cc3d931a136df5ebabe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:696813b3b0bc79d23915cb139cf17c5b4383fdfc2c08194071532bf8999930fe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148430199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c460f5b2836aa43e5b014960a8b050afa145435a304cfed3c479d49dc129b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:56:21 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 01 Apr 2020 01:56:30 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 01 Apr 2020 01:56:30 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 01 Apr 2020 01:56:30 GMT
EXPOSE 8086
# Wed, 01 Apr 2020 01:56:30 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:56:31 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:56:31 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 01 Apr 2020 01:56:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:56:31 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ef5fa9a7ce28c6f0473c3dab607d519420a639380420a279b6b399bf0d84fd`  
		Last Modified: Wed, 01 Apr 2020 01:59:07 GMT  
		Size: 87.9 MB (87912277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27777eba072e66d34253efc0ef7f4dfee89724a6e7306dfd17738d044cc79323`  
		Last Modified: Wed, 01 Apr 2020 01:58:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c634d2bef7c851e277d29a77a3f198db0bf52dda488d784116f336aa0b799fe6`  
		Last Modified: Wed, 01 Apr 2020 01:58:50 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8525dd5fc4d8587bdb1363e3afc7201f8c0cd91e33cb721c8ababa8fa129835e`  
		Last Modified: Wed, 01 Apr 2020 01:58:50 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data-alpine`

```console
$ docker pull influxdb@sha256:ade2ee58127f17cd42846484f06c6014e66bdd3a9ecf563aa4e153c60e7187b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ad50898a5f3cd3a5d0bfdd9231111e803fdbbdd838eae3e7e08d1163b438cb82
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92299087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84763cde3a71238942846a39a4887c2a16be13a2ded02dd2689359d5220fd8a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 25 Feb 2020 01:22:18 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Tue, 25 Feb 2020 01:22:27 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 25 Feb 2020 01:22:28 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 25 Feb 2020 01:22:28 GMT
EXPOSE 8086
# Tue, 25 Feb 2020 01:22:29 GMT
VOLUME [/var/lib/influxdb]
# Tue, 25 Feb 2020 01:22:29 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 25 Feb 2020 01:22:29 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 25 Feb 2020 01:22:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2020 01:22:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c9c59b5d2a9ea8da3c7e9548176b7c5d650f93dce7c1b678292f3ee5aa6f77`  
		Last Modified: Tue, 25 Feb 2020 01:24:06 GMT  
		Size: 87.7 MB (87669308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e7409222c3f0694c6261c8c439680a1073c32c20f080787e63224b56d680e3`  
		Last Modified: Tue, 25 Feb 2020 01:23:53 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0d21ddf433669aae470cc2243fb53317d67c10b3b506d1ec7288bf5cf58f2b`  
		Last Modified: Tue, 25 Feb 2020 01:23:53 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750af7d287a00fdb813a7d85b77b1ea371b943de38a98408b1afef8e0b43035a`  
		Last Modified: Tue, 25 Feb 2020 01:23:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta`

```console
$ docker pull influxdb@sha256:35b2fb03ab27b23cda5b78ace63f5b30c1765cb8716a1fe6f57aa52a64d96378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8cc8420079d23b6af7eda2fa74bf79f2165f2c9b2bddebf0b7b8003479b0b666
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83649352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f24934d73750209464f0080e2475a3694f6cc672e9b8e69b18597915b26d64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:56:21 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 01 Apr 2020 01:56:44 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 01 Apr 2020 01:56:45 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 01 Apr 2020 01:56:45 GMT
EXPOSE 8091
# Wed, 01 Apr 2020 01:56:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:56:46 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:56:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:56:47 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325f69af8a622017dc6a68abe33842d1beb8e02c13a750e2e6e2f76b93457138`  
		Last Modified: Wed, 01 Apr 2020 01:59:19 GMT  
		Size: 23.1 MB (23132633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d3f9ce723fce8ed7d741079028754f50c668f60f69c4d3d908fc9bae7c895e`  
		Last Modified: Wed, 01 Apr 2020 01:59:14 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a189662bb7c84e17a1c76056bf221af9c1234aa02d29ee27e2db8a390b0542`  
		Last Modified: Wed, 01 Apr 2020 01:59:15 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta-alpine`

```console
$ docker pull influxdb@sha256:935f23f3eeb2a62b0f56b0fb8a301832fa58a46b39e086b63a8bba73bf2d50d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7eb37763f5ab368fba1e10479811f58ededd3693e5a204003be5700423b2eb45
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27694267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e87a59d350cbcf0fbb8662e04824c54057297c4d35182555d0eedcf77e46099`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 25 Feb 2020 01:22:18 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Tue, 25 Feb 2020 01:22:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 25 Feb 2020 01:22:46 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 25 Feb 2020 01:22:47 GMT
EXPOSE 8091
# Tue, 25 Feb 2020 01:22:47 GMT
VOLUME [/var/lib/influxdb]
# Tue, 25 Feb 2020 01:22:47 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 25 Feb 2020 01:22:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2020 01:22:47 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391ad404de14e9eb4440bd3e91c95c9b876e6216d32c357b488b7c85388e7255`  
		Last Modified: Tue, 25 Feb 2020 01:24:22 GMT  
		Size: 23.1 MB (23065691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09da99d11e68e36fd2aeb608ec27f778a57a27e712b2c89abb183bc36991f6bc`  
		Last Modified: Tue, 25 Feb 2020 01:24:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6ea3b07bb562ab605a9a2023f069c6131458e25f15e392785f126b2db62250`  
		Last Modified: Tue, 25 Feb 2020 01:24:19 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:db1bbd2776aa7a8c3b089f7b32b80765c90b49179dadd89aac423bc0ec7c33af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:213f19092ddac0e75e1709ce6f687c29428ecf7fd57f24bf2043e662299d7552
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68521230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11022dc8112fc93d26bcb9d7c4bcac7f115b57890fff650d8a29afdd735cecd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 25 Feb 2020 01:21:50 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 25 Feb 2020 01:21:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 25 Feb 2020 01:21:57 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 25 Feb 2020 01:21:57 GMT
EXPOSE 8086
# Tue, 25 Feb 2020 01:21:57 GMT
VOLUME [/var/lib/influxdb]
# Tue, 25 Feb 2020 01:21:58 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 25 Feb 2020 01:21:58 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 25 Feb 2020 01:21:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2020 01:21:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596f24252014ca2dc760ecf20947aa59bdc752a4014062a15767913edcfe75a8`  
		Last Modified: Tue, 25 Feb 2020 01:23:29 GMT  
		Size: 63.9 MB (63891510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0104a2d9f4d8ca1e1bed307f4828e96ebe4dbf18e73b76353fd5c73b32387de2`  
		Last Modified: Tue, 25 Feb 2020 01:23:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ff92f4e9a9184c2a500f4c39aefd1cbf9dfb0353e7160d3ac1cf7acd7a349`  
		Last Modified: Tue, 25 Feb 2020 01:23:20 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94535d69e85267353aff6b49fafc3df78032a03d78bb42b256539b5a3faee6b`  
		Last Modified: Tue, 25 Feb 2020 01:23:20 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data`

```console
$ docker pull influxdb@sha256:c856417e9723c589231b4d0b004c3bf3e0313305c443cc3d931a136df5ebabe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:696813b3b0bc79d23915cb139cf17c5b4383fdfc2c08194071532bf8999930fe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148430199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c460f5b2836aa43e5b014960a8b050afa145435a304cfed3c479d49dc129b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:56:21 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 01 Apr 2020 01:56:30 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 01 Apr 2020 01:56:30 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 01 Apr 2020 01:56:30 GMT
EXPOSE 8086
# Wed, 01 Apr 2020 01:56:30 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:56:31 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:56:31 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 01 Apr 2020 01:56:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:56:31 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ef5fa9a7ce28c6f0473c3dab607d519420a639380420a279b6b399bf0d84fd`  
		Last Modified: Wed, 01 Apr 2020 01:59:07 GMT  
		Size: 87.9 MB (87912277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27777eba072e66d34253efc0ef7f4dfee89724a6e7306dfd17738d044cc79323`  
		Last Modified: Wed, 01 Apr 2020 01:58:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c634d2bef7c851e277d29a77a3f198db0bf52dda488d784116f336aa0b799fe6`  
		Last Modified: Wed, 01 Apr 2020 01:58:50 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8525dd5fc4d8587bdb1363e3afc7201f8c0cd91e33cb721c8ababa8fa129835e`  
		Last Modified: Wed, 01 Apr 2020 01:58:50 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:ade2ee58127f17cd42846484f06c6014e66bdd3a9ecf563aa4e153c60e7187b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ad50898a5f3cd3a5d0bfdd9231111e803fdbbdd838eae3e7e08d1163b438cb82
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92299087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84763cde3a71238942846a39a4887c2a16be13a2ded02dd2689359d5220fd8a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 25 Feb 2020 01:22:18 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Tue, 25 Feb 2020 01:22:27 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 25 Feb 2020 01:22:28 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Tue, 25 Feb 2020 01:22:28 GMT
EXPOSE 8086
# Tue, 25 Feb 2020 01:22:29 GMT
VOLUME [/var/lib/influxdb]
# Tue, 25 Feb 2020 01:22:29 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Tue, 25 Feb 2020 01:22:29 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 25 Feb 2020 01:22:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2020 01:22:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c9c59b5d2a9ea8da3c7e9548176b7c5d650f93dce7c1b678292f3ee5aa6f77`  
		Last Modified: Tue, 25 Feb 2020 01:24:06 GMT  
		Size: 87.7 MB (87669308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e7409222c3f0694c6261c8c439680a1073c32c20f080787e63224b56d680e3`  
		Last Modified: Tue, 25 Feb 2020 01:23:53 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0d21ddf433669aae470cc2243fb53317d67c10b3b506d1ec7288bf5cf58f2b`  
		Last Modified: Tue, 25 Feb 2020 01:23:53 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750af7d287a00fdb813a7d85b77b1ea371b943de38a98408b1afef8e0b43035a`  
		Last Modified: Tue, 25 Feb 2020 01:23:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:f13ba72e09d89185e0901110c0ab2b457ff568af54a0956da0ad66fafcae0bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:f38f5d7eff02d10c48801791ef741286468270f28af1d39ce5c4921f4ec13d7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124614816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88696c3ec771f302ff25ca7253787cce05bfdea4e2781f9731e0c9f7eec8a71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:55:58 GMT
ENV INFLUXDB_VERSION=1.7.10
# Wed, 01 Apr 2020 01:56:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Wed, 01 Apr 2020 01:56:08 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Wed, 01 Apr 2020 01:56:08 GMT
EXPOSE 8086
# Wed, 01 Apr 2020 01:56:08 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:56:09 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:56:09 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 01 Apr 2020 01:56:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:56:10 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1b96554da0ba8fcedde11aca5ec97c822615cb990dfbe923257e0ab03330d1`  
		Last Modified: Wed, 01 Apr 2020 01:58:43 GMT  
		Size: 64.1 MB (64096952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4724d32515be80c17a780b3b6f524a57f9548f535808a64d68c4214acb07dc15`  
		Last Modified: Wed, 01 Apr 2020 01:58:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d110c7dfc9268d676588ca2e5bc12c321350ef95659e3f22d6e3bc09a6c14f15`  
		Last Modified: Wed, 01 Apr 2020 01:58:30 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4ab55e07b667296f3c75f644a74d686647a99f6bc5824b94e8cb8fc6e08ae0`  
		Last Modified: Wed, 01 Apr 2020 01:58:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:420077e21d5d71d6008012a9f5cb54233234212c9445f745d57d66f1773de75e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116157240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90850b57f992fe74c09d6ce972a3c19673a66869bf26086cb5486a055fcad677`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:24 GMT
ADD file:b047b0c4dbfbcc048385195e807283b9386c4aac13a4841112cb3f76cd932b06 in / 
# Tue, 31 Mar 2020 01:52:26 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:53:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 23:27:41 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 23:28:33 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 31 Mar 2020 23:28:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 23:28:45 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 31 Mar 2020 23:28:46 GMT
EXPOSE 8086
# Tue, 31 Mar 2020 23:28:46 GMT
VOLUME [/var/lib/influxdb]
# Tue, 31 Mar 2020 23:28:48 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 31 Mar 2020 23:28:49 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 31 Mar 2020 23:28:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 23:28:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:eb3768893937e6b455f98cd8db65949a6aa5c54ebd94fca3039af9833187ce10`  
		Last Modified: Tue, 31 Mar 2020 01:59:52 GMT  
		Size: 42.1 MB (42100090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb68590923b075c8f49c4470341451f9d874afc84c5fc916278815a1064243`  
		Last Modified: Tue, 31 Mar 2020 04:04:43 GMT  
		Size: 9.5 MB (9498284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743981b4cf60d4ed8ddd6610e4d1d75256ddb63a7d83d540a96e1faf8ba8a315`  
		Last Modified: Tue, 31 Mar 2020 04:04:42 GMT  
		Size: 3.9 MB (3918805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39848df21e0940ce448bbc5a30bb53f1ae2d3a23b774be8add8462388496176d`  
		Last Modified: Tue, 31 Mar 2020 23:29:03 GMT  
		Size: 2.8 KB (2805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cdec4d9877a345bd4d0eeed63fc6032d748c105ecbd8cfe24f7def1fe99323`  
		Last Modified: Tue, 31 Mar 2020 23:29:49 GMT  
		Size: 60.6 MB (60635541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f487a5278dbc614e551e4b5a518dfec2009aeecdafb33b4dd5d336971a3868`  
		Last Modified: Tue, 31 Mar 2020 23:29:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0ccb10615426229fede770a8a9010d5cbc01475511e9c6c46d6b4ac01f2f9f`  
		Last Modified: Tue, 31 Mar 2020 23:29:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6ab3423dee06091a4fbb44d97ba75aa5acea4e04b5d2b97c7bebc9fc6b3ed2`  
		Last Modified: Tue, 31 Mar 2020 23:29:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bd16c6f810d30776080f1d3f0c9478f757343e02b8ebb5e8909f786a7c26b53b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117133230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c8d6bd59e1d1f008c13f43d538a228f8edbea59366c83b31d0309c741cb53d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:21:37 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 21:22:11 GMT
ENV INFLUXDB_VERSION=1.7.10
# Tue, 31 Mar 2020 21:22:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Tue, 31 Mar 2020 21:22:21 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Tue, 31 Mar 2020 21:22:22 GMT
EXPOSE 8086
# Tue, 31 Mar 2020 21:22:22 GMT
VOLUME [/var/lib/influxdb]
# Tue, 31 Mar 2020 21:22:23 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Tue, 31 Mar 2020 21:22:23 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Tue, 31 Mar 2020 21:22:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 21:22:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4b0dbd0d8c4ebbcb0bd21245e7f3bfa3f1dcaa045d058597cb38fd62aa3c95`  
		Last Modified: Tue, 31 Mar 2020 21:22:36 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5955d9f7eca8b5aedca7a39fd5077979902b985ab851573a57cd3f07b9b6b079`  
		Last Modified: Tue, 31 Mar 2020 21:23:18 GMT  
		Size: 60.1 MB (60127737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07da9d58eae83ad8c7679b533d4869b03ed814eb1f50baa63a6c6367f183c0a5`  
		Last Modified: Tue, 31 Mar 2020 21:23:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a529b6b5daf8c8a3986f7328c65f4e672d7a6874892668539b39a0aa26ac92`  
		Last Modified: Tue, 31 Mar 2020 21:23:02 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a294964f2e9d24cd7e2bb755c6eb40d422d255796caa521bd38ce0624d75ea7e`  
		Last Modified: Tue, 31 Mar 2020 21:23:02 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:35b2fb03ab27b23cda5b78ace63f5b30c1765cb8716a1fe6f57aa52a64d96378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8cc8420079d23b6af7eda2fa74bf79f2165f2c9b2bddebf0b7b8003479b0b666
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83649352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f24934d73750209464f0080e2475a3694f6cc672e9b8e69b18597915b26d64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Apr 2020 01:54:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 01:56:21 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Wed, 01 Apr 2020 01:56:44 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 01 Apr 2020 01:56:45 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 01 Apr 2020 01:56:45 GMT
EXPOSE 8091
# Wed, 01 Apr 2020 01:56:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 01 Apr 2020 01:56:46 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 01 Apr 2020 01:56:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 01:56:47 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635572a000dfb22bf7811df4f45babad6a6cf960bf059819bfd0c66d0b6f319f`  
		Last Modified: Wed, 01 Apr 2020 01:57:26 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325f69af8a622017dc6a68abe33842d1beb8e02c13a750e2e6e2f76b93457138`  
		Last Modified: Wed, 01 Apr 2020 01:59:19 GMT  
		Size: 23.1 MB (23132633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d3f9ce723fce8ed7d741079028754f50c668f60f69c4d3d908fc9bae7c895e`  
		Last Modified: Wed, 01 Apr 2020 01:59:14 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a189662bb7c84e17a1c76056bf221af9c1234aa02d29ee27e2db8a390b0542`  
		Last Modified: Wed, 01 Apr 2020 01:59:15 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:935f23f3eeb2a62b0f56b0fb8a301832fa58a46b39e086b63a8bba73bf2d50d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:7eb37763f5ab368fba1e10479811f58ededd3693e5a204003be5700423b2eb45
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27694267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e87a59d350cbcf0fbb8662e04824c54057297c4d35182555d0eedcf77e46099`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 25 Feb 2020 01:22:18 GMT
ENV INFLUXDB_VERSION=1.7.10-c1.7.10
# Tue, 25 Feb 2020 01:22:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 25 Feb 2020 01:22:46 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 25 Feb 2020 01:22:47 GMT
EXPOSE 8091
# Tue, 25 Feb 2020 01:22:47 GMT
VOLUME [/var/lib/influxdb]
# Tue, 25 Feb 2020 01:22:47 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 25 Feb 2020 01:22:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2020 01:22:47 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391ad404de14e9eb4440bd3e91c95c9b876e6216d32c357b488b7c85388e7255`  
		Last Modified: Tue, 25 Feb 2020 01:24:22 GMT  
		Size: 23.1 MB (23065691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09da99d11e68e36fd2aeb608ec27f778a57a27e712b2c89abb183bc36991f6bc`  
		Last Modified: Tue, 25 Feb 2020 01:24:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6ea3b07bb562ab605a9a2023f069c6131458e25f15e392785f126b2db62250`  
		Last Modified: Tue, 25 Feb 2020 01:24:19 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
