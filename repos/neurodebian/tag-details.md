<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bionic`](#neurodebianbionic)
-	[`neurodebian:bionic-non-free`](#neurodebianbionic-non-free)
-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:buster`](#neurodebianbuster)
-	[`neurodebian:buster-non-free`](#neurodebianbuster-non-free)
-	[`neurodebian:focal`](#neurodebianfocal)
-	[`neurodebian:focal-non-free`](#neurodebianfocal-non-free)
-	[`neurodebian:impish`](#neurodebianimpish)
-	[`neurodebian:impish-non-free`](#neurodebianimpish-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd`](#neurodebiannd)
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
-	[`neurodebian:nd100`](#neurodebiannd100)
-	[`neurodebian:nd100-non-free`](#neurodebiannd100-non-free)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd16.04`](#neurodebiannd1604)
-	[`neurodebian:nd16.04-non-free`](#neurodebiannd1604-non-free)
-	[`neurodebian:nd18.04`](#neurodebiannd1804)
-	[`neurodebian:nd18.04-non-free`](#neurodebiannd1804-non-free)
-	[`neurodebian:nd20.04`](#neurodebiannd2004)
-	[`neurodebian:nd20.04-non-free`](#neurodebiannd2004-non-free)
-	[`neurodebian:nd21.10`](#neurodebiannd2110)
-	[`neurodebian:nd21.10-non-free`](#neurodebiannd2110-non-free)
-	[`neurodebian:nd90`](#neurodebiannd90)
-	[`neurodebian:nd90-non-free`](#neurodebiannd90-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)
-	[`neurodebian:stretch`](#neurodebianstretch)
-	[`neurodebian:stretch-non-free`](#neurodebianstretch-non-free)
-	[`neurodebian:xenial`](#neurodebianxenial)
-	[`neurodebian:xenial-non-free`](#neurodebianxenial-non-free)

## `neurodebian:bionic`

```console
$ docker pull neurodebian@sha256:555b2b08bcc094b7afaaf84ea8f9f3de19fdb00e5b7b74fd5cf3c043c02f751d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bionic` - linux; amd64

```console
$ docker pull neurodebian@sha256:1645e3310909d3d6c6dde18620034c1e16bdfca4885f0894fc6f5aa345510ff7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31765044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a36c0147ecfedd99a00877d541298700840da0442491b2969da977ad015403`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:10:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:11:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:11:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:11:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13c025ea06346b83ad7c49fa15da8d4003fa73e23df204b6615c244e8664759`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 4.8 MB (4813174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24aca53dc4332fc343fe1b8f11288687747e5786de455f96b33b6a2334850c2`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 3.2 KB (3157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683e3441e3e903fbe30910de4ebe852baf583864320da739381072d9dd6b1611`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6c2c9ecc51b2cff0024e1d1c3b3067892739d7f423e5eb2dedd1e03ed3d93`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 239.8 KB (239834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:e91546d2c3afd4b1f57e9e44a564fbcd005a454b254b732490e8f3538a2d2a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:945ccae98ba2d0695cf90a01077ff27e2d7a0a0a59ce3c97ae4c7fb3861be2ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31765300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb1855f361d51ed1c9c6c2bc86b5438783484993d1a7392435053c6a48bb19a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:10:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:11:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:11:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:11:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:11:46 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13c025ea06346b83ad7c49fa15da8d4003fa73e23df204b6615c244e8664759`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 4.8 MB (4813174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24aca53dc4332fc343fe1b8f11288687747e5786de455f96b33b6a2334850c2`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 3.2 KB (3157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683e3441e3e903fbe30910de4ebe852baf583864320da739381072d9dd6b1611`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6c2c9ecc51b2cff0024e1d1c3b3067892739d7f423e5eb2dedd1e03ed3d93`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 239.8 KB (239834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978320cc501a425c41115d59e2a6244b6544c46fde53245a986adfbe51826bba`  
		Last Modified: Fri, 18 Mar 2022 08:16:23 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:de594c46719d0ba1458f76fdfb286a3433a0e7452cb4b56ab0421f5fbdd43d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:ed48b69529db675da02b2b4f238b49f3581004f13cde3611d20d758f513a390c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67431726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fbf964901f08d2e3ea3f31040a1a36c617a687d9bc38237baa749a46404b55`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:22 GMT
ADD file:2a92eda55857403475e71c7e72e14b8332b700683b753b80998c67de8059b01b in / 
# Thu, 17 Mar 2022 04:03:23 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66fb1aabb4c03c1a8502c7ab4d442a4602f465cee7eccf27eb706178ce2859a6`  
		Last Modified: Thu, 17 Mar 2022 04:08:59 GMT  
		Size: 55.8 MB (55754297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edd9cb2b95dbf7f48618c8e86c46c24ebbd1e88faa80bb6299f17474bdd2b3d`  
		Last Modified: Fri, 18 Mar 2022 08:18:22 GMT  
		Size: 11.4 MB (11367941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7fb7a823070655e625d406d231cc6a2f192054cc327c4730783974f7e9c0a4`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7330b95115cc239fdebf118defcb0e3cf76bcabf611950715ce2cf8cbd7acd81`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89deb3ade5987120d2bba15db10e8be7a48a9fa3517fb6395fc5952e4bad04a2`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 307.5 KB (307473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:2284e71395ebbe264bfb288fc422101f6c3e7feff66633f373f68ae621ec1783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:409c2332daa7272d31aa886e9658768f7ef8203669036c3a11c48852a8d06899
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67432092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81109e92014c733ae52e6b4661be0aab21dfbffe6e1428e2b4ed57138ad3c7e7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:22 GMT
ADD file:2a92eda55857403475e71c7e72e14b8332b700683b753b80998c67de8059b01b in / 
# Thu, 17 Mar 2022 04:03:23 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:15:01 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:66fb1aabb4c03c1a8502c7ab4d442a4602f465cee7eccf27eb706178ce2859a6`  
		Last Modified: Thu, 17 Mar 2022 04:08:59 GMT  
		Size: 55.8 MB (55754297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edd9cb2b95dbf7f48618c8e86c46c24ebbd1e88faa80bb6299f17474bdd2b3d`  
		Last Modified: Fri, 18 Mar 2022 08:18:22 GMT  
		Size: 11.4 MB (11367941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7fb7a823070655e625d406d231cc6a2f192054cc327c4730783974f7e9c0a4`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7330b95115cc239fdebf118defcb0e3cf76bcabf611950715ce2cf8cbd7acd81`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89deb3ade5987120d2bba15db10e8be7a48a9fa3517fb6395fc5952e4bad04a2`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 307.5 KB (307473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be8b0b9c55260fa6b3d724c6f7075078c1f4b90a2fb916071bed9314952e804`  
		Last Modified: Fri, 18 Mar 2022 08:18:31 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:d7eec8fa14e57d96fac163f21b5c2089e7e90d3005e0dfafa26419b692cc33f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:1f4d0bf44f56fa11b9319886194c15bf12fb012cbfbf136c0375ef8ea7dda206
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66545767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7129776696eee1bff34034c7d989fbd4f438506ac3e82f2eeb8e80186a96dca3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4228642e82a30a73f7cbd7f0c7392aa1ac2cddf752825f306aed5b081edd3566`  
		Last Modified: Fri, 18 Mar 2022 08:17:58 GMT  
		Size: 11.3 MB (11309638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2beeba079089ff348059b8341a20ef560d1314eb37238be288f1f368d62a9550`  
		Last Modified: Fri, 18 Mar 2022 08:17:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2635a2803078eea28ecbb9fee59ca31830242961f360a1bc71b1cfa2ab21492c`  
		Last Modified: Fri, 18 Mar 2022 08:17:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b234e87955266b3dcd5b20731e0134b3084225781a695fd865e490fda0dc4db`  
		Last Modified: Fri, 18 Mar 2022 08:17:57 GMT  
		Size: 311.3 KB (311282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:d74aac0a9a2b499a43320fbe77c4903f16eb51e5d4cc11157befa779b7bccb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:df5228a7cc9869e9dd2cc21f322d93c3c8aa40704ec8440f6c405f7fc96d0396
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66546132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f211e5eb1c6485556c22e86cd196252ac3b85d5ab096431ce311386099e4b4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:41 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4228642e82a30a73f7cbd7f0c7392aa1ac2cddf752825f306aed5b081edd3566`  
		Last Modified: Fri, 18 Mar 2022 08:17:58 GMT  
		Size: 11.3 MB (11309638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2beeba079089ff348059b8341a20ef560d1314eb37238be288f1f368d62a9550`  
		Last Modified: Fri, 18 Mar 2022 08:17:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2635a2803078eea28ecbb9fee59ca31830242961f360a1bc71b1cfa2ab21492c`  
		Last Modified: Fri, 18 Mar 2022 08:17:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b234e87955266b3dcd5b20731e0134b3084225781a695fd865e490fda0dc4db`  
		Last Modified: Fri, 18 Mar 2022 08:17:57 GMT  
		Size: 311.3 KB (311282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c8fe6f006217cfab491cd75a0eb55ea7d173a5b5d2cf62499f9ce9d22897c4`  
		Last Modified: Fri, 18 Mar 2022 08:18:09 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:a0d38cfe7c6d0f00aa0f3bc50932656eafd6c4b0d87e2fb1eb5dc84b36459885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:772b38593089c43c268056d92cc101159576bba644c7d3d03453070401059a07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0d32afb8bcba41d46b8a727c7a405cbee36e3ea7e712c5cfb89ad969198f3d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ec994af2fba75a71b03c6d8aae2fa9b1c9834c433bd718542f28d53d6ef4d`  
		Last Modified: Fri, 18 Mar 2022 08:17:38 GMT  
		Size: 10.5 MB (10500126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b41055a634223424a74ca6ea5157b314b0f74a079d3004eb330292300a1f568`  
		Last Modified: Fri, 18 Mar 2022 08:17:37 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbbf308ade92d3f1fa2549452dfc57ac2538ed49b1d8970e2b6b05f8299fb2f`  
		Last Modified: Fri, 18 Mar 2022 08:17:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4327d02480acb39abce6d97b37d5996718d5793ea6975af13786e865d327d8bf`  
		Last Modified: Fri, 18 Mar 2022 08:17:37 GMT  
		Size: 302.8 KB (302779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:ca7fb88979297d419d44f23c027c70be69eb1f5732ee94ded5d12ffedea44e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:207cc8b477e2978dd6d3f95576075a94fdca3d8a0a63ac02cb323a7d50151a71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2815aa25a09193b63b716be72d59bb146666b016690b250b67ed31df8fa59f08`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:22 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ec994af2fba75a71b03c6d8aae2fa9b1c9834c433bd718542f28d53d6ef4d`  
		Last Modified: Fri, 18 Mar 2022 08:17:38 GMT  
		Size: 10.5 MB (10500126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b41055a634223424a74ca6ea5157b314b0f74a079d3004eb330292300a1f568`  
		Last Modified: Fri, 18 Mar 2022 08:17:37 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbbf308ade92d3f1fa2549452dfc57ac2538ed49b1d8970e2b6b05f8299fb2f`  
		Last Modified: Fri, 18 Mar 2022 08:17:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4327d02480acb39abce6d97b37d5996718d5793ea6975af13786e865d327d8bf`  
		Last Modified: Fri, 18 Mar 2022 08:17:37 GMT  
		Size: 302.8 KB (302779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d8980030f3b3934d2394516fc7ba58239f3362d079ac5f328eaab4be50e7f1`  
		Last Modified: Fri, 18 Mar 2022 08:17:47 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:4edb28dcbd20d4d4edfedc8c1c78de5933e918c2cd537025fa8e7795216226a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:fcc9975228aa54c9b819de450a91c96d06a3723e3a6e7b653cb568dd2393fe7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34294517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aeaa060e12baeb84bf1b41aa26cdbf4c2c53d3726e69e0ed086522a7175f6a4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:12:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:12:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:12:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:12:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181b23a20725abd31982685ba6ef94f9c18f9b4715d5413a59cf785746d88b23`  
		Last Modified: Fri, 18 Mar 2022 08:16:33 GMT  
		Size: 5.5 MB (5488532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc0a34dbeb5ca294abf88cbffaceed4bcb3a84170048e12e84e38d9c8675d22`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09414e5157753ac2e1ab73492fccc7b48fb65f1937bbfe26e3e959a1fae9e0e`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87dcb7d6ca3e3b5c1f15c6c7bf23a38ad1e13b919a24a1b6169b625a3a7ee9a`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 238.1 KB (238061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:7afa91a1b2a0b7d718b7fcd1931847e6856f29d0b8c14698ba696f60881ebdfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d1f00395c2f2448b4e7f04ec19a232ad71985b77dc66d616d5455c169bd86fbe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34294775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7c25d0ce101c6a6aa21cd974d08e34855d820cf6e50c4e28c7b033ea5539a5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:12:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:12:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:12:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:12:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:12:58 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181b23a20725abd31982685ba6ef94f9c18f9b4715d5413a59cf785746d88b23`  
		Last Modified: Fri, 18 Mar 2022 08:16:33 GMT  
		Size: 5.5 MB (5488532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc0a34dbeb5ca294abf88cbffaceed4bcb3a84170048e12e84e38d9c8675d22`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09414e5157753ac2e1ab73492fccc7b48fb65f1937bbfe26e3e959a1fae9e0e`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87dcb7d6ca3e3b5c1f15c6c7bf23a38ad1e13b919a24a1b6169b625a3a7ee9a`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 238.1 KB (238061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f18a59ac046a70833ff45efdfd55fdb47431829ea19991eaf19f806b0f08bfc`  
		Last Modified: Fri, 18 Mar 2022 08:16:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:impish`

```console
$ docker pull neurodebian@sha256:7d57bb08153ba7f05a7822ae8947842e4584304f538848c4377b10cbe09fb69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:impish` - linux; amd64

```console
$ docker pull neurodebian@sha256:3af8a75a0545139db54dc00aba8a4845416e87f8cb884b6a64300c518f6ddead
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34389098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f0ca849eadea70a74806f43758c3e847c8bc58853b69057d0223e2a90dafbf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:54 GMT
ADD file:dc66b6b0841e395b5cf9d65976a75c3a46a19eb2c0fda4556ac6b4c5b0fe4dea in / 
# Fri, 18 Mar 2022 05:30:55 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:13:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:13:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:13:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian impish main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel impish main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:13:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:49dc71d53e6dff9c7147b85fbe167470cff447114548e6df43606b75526c1451`  
		Last Modified: Fri, 18 Mar 2022 05:32:45 GMT  
		Size: 30.4 MB (30385910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02dcdc2dc3c600bc75fef3a31d1a5e174b094ca75baf90ba6d19587937596f`  
		Last Modified: Fri, 18 Mar 2022 08:16:52 GMT  
		Size: 3.8 MB (3751774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5a2abb4afa38d503f13785e4ddec9cf8c7dfecbc32a1044e17d914465c297`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c82d2f42bf7700d6f3b7a7d0a2cb65df389e99fc8590f8ea57f38faa9953606`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd139379a494abeceaea7b99b395b2dfa5d3171218e66e5b2a861bead4ef1e26`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 249.4 KB (249399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:impish-non-free`

```console
$ docker pull neurodebian@sha256:3d2e187fe6b51ab8920ae14f64a641b9f9e0c63773b5bdda1c767c7ca9a1d7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:impish-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:95d4f32310f9a745ed1872824b5291c47bf8eb3cd79406514131e23090c75e1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34389358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157f768d72636f7b777a6e298a6eb924161750b6ddc10ef17b8bb027d2c7e14e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:54 GMT
ADD file:dc66b6b0841e395b5cf9d65976a75c3a46a19eb2c0fda4556ac6b4c5b0fe4dea in / 
# Fri, 18 Mar 2022 05:30:55 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:13:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:13:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:13:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian impish main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel impish main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:13:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:13:41 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:49dc71d53e6dff9c7147b85fbe167470cff447114548e6df43606b75526c1451`  
		Last Modified: Fri, 18 Mar 2022 05:32:45 GMT  
		Size: 30.4 MB (30385910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02dcdc2dc3c600bc75fef3a31d1a5e174b094ca75baf90ba6d19587937596f`  
		Last Modified: Fri, 18 Mar 2022 08:16:52 GMT  
		Size: 3.8 MB (3751774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5a2abb4afa38d503f13785e4ddec9cf8c7dfecbc32a1044e17d914465c297`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c82d2f42bf7700d6f3b7a7d0a2cb65df389e99fc8590f8ea57f38faa9953606`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd139379a494abeceaea7b99b395b2dfa5d3171218e66e5b2a861bead4ef1e26`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 249.4 KB (249399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e4a25da4e998243c62595ed39cb7923223ddc183fb90108283b18a76655a42`  
		Last Modified: Fri, 18 Mar 2022 08:17:01 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:d7eec8fa14e57d96fac163f21b5c2089e7e90d3005e0dfafa26419b692cc33f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:1f4d0bf44f56fa11b9319886194c15bf12fb012cbfbf136c0375ef8ea7dda206
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66545767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7129776696eee1bff34034c7d989fbd4f438506ac3e82f2eeb8e80186a96dca3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4228642e82a30a73f7cbd7f0c7392aa1ac2cddf752825f306aed5b081edd3566`  
		Last Modified: Fri, 18 Mar 2022 08:17:58 GMT  
		Size: 11.3 MB (11309638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2beeba079089ff348059b8341a20ef560d1314eb37238be288f1f368d62a9550`  
		Last Modified: Fri, 18 Mar 2022 08:17:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2635a2803078eea28ecbb9fee59ca31830242961f360a1bc71b1cfa2ab21492c`  
		Last Modified: Fri, 18 Mar 2022 08:17:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b234e87955266b3dcd5b20731e0134b3084225781a695fd865e490fda0dc4db`  
		Last Modified: Fri, 18 Mar 2022 08:17:57 GMT  
		Size: 311.3 KB (311282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:ccea1662fe9f22ebeb8004edabf1bcfcd02c260b3a365f3bb4117fe1d836c849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:297460e2945c00d57e88ddf9d1c6db065ed8f24ebdf8cd614708c320464255d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67668467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df9c2bc96bce88be296b8467626e67880626f7769cccc6db72524fa0fb439ca`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:05:54 GMT
ADD file:20b1068c276c223839818edd0aca3981a1b8139130064d19f9ec38e26a94ff27 in / 
# Thu, 17 Mar 2022 04:05:54 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:15:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:15:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:15:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:15:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab40a96ab944197ee11d696f776db9c1130db9825e9996a5e8939611fcf5e470`  
		Last Modified: Thu, 17 Mar 2022 04:12:27 GMT  
		Size: 56.0 MB (55984715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9128aac36dac7e03aa34a5c0e125dfcec841942698bf8aef01012ee2f596a8d8`  
		Last Modified: Fri, 18 Mar 2022 08:18:41 GMT  
		Size: 11.4 MB (11374011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a999bb7dcc545cc51773d4c7aab4a9bc7f387800fe7ff8f40d0aee6f60935a94`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a2eaf0fa50faf1fc453bdf807f0e1a9494babfceea5a2e064bb97c9388c1d6`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abe8889081ee40a2d3cf24eb140b00e5f18e6b538f091c567f4aabc0120f07e`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 307.7 KB (307730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:bc0c39aae86597def0f27272b2af65ebfb2a3ff877f39260caa95adc57f75727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:883c47ac6a8575a1c24758747419c7dfc9bfa63d851681293b8bf1aeae1e0b97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67668783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf847e6fb8d6afdf487f58c8abd7bc69ca58a9f16dd4f10643c9da5332728bdf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:05:54 GMT
ADD file:20b1068c276c223839818edd0aca3981a1b8139130064d19f9ec38e26a94ff27 in / 
# Thu, 17 Mar 2022 04:05:54 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:15:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:15:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:15:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:15:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:15:20 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:ab40a96ab944197ee11d696f776db9c1130db9825e9996a5e8939611fcf5e470`  
		Last Modified: Thu, 17 Mar 2022 04:12:27 GMT  
		Size: 56.0 MB (55984715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9128aac36dac7e03aa34a5c0e125dfcec841942698bf8aef01012ee2f596a8d8`  
		Last Modified: Fri, 18 Mar 2022 08:18:41 GMT  
		Size: 11.4 MB (11374011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a999bb7dcc545cc51773d4c7aab4a9bc7f387800fe7ff8f40d0aee6f60935a94`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a2eaf0fa50faf1fc453bdf807f0e1a9494babfceea5a2e064bb97c9388c1d6`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abe8889081ee40a2d3cf24eb140b00e5f18e6b538f091c567f4aabc0120f07e`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 307.7 KB (307730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ebcdd130a728f8e1585d398f32840253f3e7aa5b9beba3b1023d239433e0e0`  
		Last Modified: Fri, 18 Mar 2022 08:18:50 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:a0d38cfe7c6d0f00aa0f3bc50932656eafd6c4b0d87e2fb1eb5dc84b36459885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:772b38593089c43c268056d92cc101159576bba644c7d3d03453070401059a07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0d32afb8bcba41d46b8a727c7a405cbee36e3ea7e712c5cfb89ad969198f3d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ec994af2fba75a71b03c6d8aae2fa9b1c9834c433bd718542f28d53d6ef4d`  
		Last Modified: Fri, 18 Mar 2022 08:17:38 GMT  
		Size: 10.5 MB (10500126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b41055a634223424a74ca6ea5157b314b0f74a079d3004eb330292300a1f568`  
		Last Modified: Fri, 18 Mar 2022 08:17:37 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbbf308ade92d3f1fa2549452dfc57ac2538ed49b1d8970e2b6b05f8299fb2f`  
		Last Modified: Fri, 18 Mar 2022 08:17:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4327d02480acb39abce6d97b37d5996718d5793ea6975af13786e865d327d8bf`  
		Last Modified: Fri, 18 Mar 2022 08:17:37 GMT  
		Size: 302.8 KB (302779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:ca7fb88979297d419d44f23c027c70be69eb1f5732ee94ded5d12ffedea44e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:207cc8b477e2978dd6d3f95576075a94fdca3d8a0a63ac02cb323a7d50151a71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2815aa25a09193b63b716be72d59bb146666b016690b250b67ed31df8fa59f08`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:22 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ec994af2fba75a71b03c6d8aae2fa9b1c9834c433bd718542f28d53d6ef4d`  
		Last Modified: Fri, 18 Mar 2022 08:17:38 GMT  
		Size: 10.5 MB (10500126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b41055a634223424a74ca6ea5157b314b0f74a079d3004eb330292300a1f568`  
		Last Modified: Fri, 18 Mar 2022 08:17:37 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbbf308ade92d3f1fa2549452dfc57ac2538ed49b1d8970e2b6b05f8299fb2f`  
		Last Modified: Fri, 18 Mar 2022 08:17:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4327d02480acb39abce6d97b37d5996718d5793ea6975af13786e865d327d8bf`  
		Last Modified: Fri, 18 Mar 2022 08:17:37 GMT  
		Size: 302.8 KB (302779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d8980030f3b3934d2394516fc7ba58239f3362d079ac5f328eaab4be50e7f1`  
		Last Modified: Fri, 18 Mar 2022 08:17:47 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:d7eec8fa14e57d96fac163f21b5c2089e7e90d3005e0dfafa26419b692cc33f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:1f4d0bf44f56fa11b9319886194c15bf12fb012cbfbf136c0375ef8ea7dda206
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66545767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7129776696eee1bff34034c7d989fbd4f438506ac3e82f2eeb8e80186a96dca3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4228642e82a30a73f7cbd7f0c7392aa1ac2cddf752825f306aed5b081edd3566`  
		Last Modified: Fri, 18 Mar 2022 08:17:58 GMT  
		Size: 11.3 MB (11309638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2beeba079089ff348059b8341a20ef560d1314eb37238be288f1f368d62a9550`  
		Last Modified: Fri, 18 Mar 2022 08:17:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2635a2803078eea28ecbb9fee59ca31830242961f360a1bc71b1cfa2ab21492c`  
		Last Modified: Fri, 18 Mar 2022 08:17:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b234e87955266b3dcd5b20731e0134b3084225781a695fd865e490fda0dc4db`  
		Last Modified: Fri, 18 Mar 2022 08:17:57 GMT  
		Size: 311.3 KB (311282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:d74aac0a9a2b499a43320fbe77c4903f16eb51e5d4cc11157befa779b7bccb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:df5228a7cc9869e9dd2cc21f322d93c3c8aa40704ec8440f6c405f7fc96d0396
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66546132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f211e5eb1c6485556c22e86cd196252ac3b85d5ab096431ce311386099e4b4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:41 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4228642e82a30a73f7cbd7f0c7392aa1ac2cddf752825f306aed5b081edd3566`  
		Last Modified: Fri, 18 Mar 2022 08:17:58 GMT  
		Size: 11.3 MB (11309638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2beeba079089ff348059b8341a20ef560d1314eb37238be288f1f368d62a9550`  
		Last Modified: Fri, 18 Mar 2022 08:17:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2635a2803078eea28ecbb9fee59ca31830242961f360a1bc71b1cfa2ab21492c`  
		Last Modified: Fri, 18 Mar 2022 08:17:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b234e87955266b3dcd5b20731e0134b3084225781a695fd865e490fda0dc4db`  
		Last Modified: Fri, 18 Mar 2022 08:17:57 GMT  
		Size: 311.3 KB (311282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c8fe6f006217cfab491cd75a0eb55ea7d173a5b5d2cf62499f9ce9d22897c4`  
		Last Modified: Fri, 18 Mar 2022 08:18:09 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:de594c46719d0ba1458f76fdfb286a3433a0e7452cb4b56ab0421f5fbdd43d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:ed48b69529db675da02b2b4f238b49f3581004f13cde3611d20d758f513a390c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67431726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fbf964901f08d2e3ea3f31040a1a36c617a687d9bc38237baa749a46404b55`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:22 GMT
ADD file:2a92eda55857403475e71c7e72e14b8332b700683b753b80998c67de8059b01b in / 
# Thu, 17 Mar 2022 04:03:23 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66fb1aabb4c03c1a8502c7ab4d442a4602f465cee7eccf27eb706178ce2859a6`  
		Last Modified: Thu, 17 Mar 2022 04:08:59 GMT  
		Size: 55.8 MB (55754297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edd9cb2b95dbf7f48618c8e86c46c24ebbd1e88faa80bb6299f17474bdd2b3d`  
		Last Modified: Fri, 18 Mar 2022 08:18:22 GMT  
		Size: 11.4 MB (11367941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7fb7a823070655e625d406d231cc6a2f192054cc327c4730783974f7e9c0a4`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7330b95115cc239fdebf118defcb0e3cf76bcabf611950715ce2cf8cbd7acd81`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89deb3ade5987120d2bba15db10e8be7a48a9fa3517fb6395fc5952e4bad04a2`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 307.5 KB (307473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:2284e71395ebbe264bfb288fc422101f6c3e7feff66633f373f68ae621ec1783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:409c2332daa7272d31aa886e9658768f7ef8203669036c3a11c48852a8d06899
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67432092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81109e92014c733ae52e6b4661be0aab21dfbffe6e1428e2b4ed57138ad3c7e7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:22 GMT
ADD file:2a92eda55857403475e71c7e72e14b8332b700683b753b80998c67de8059b01b in / 
# Thu, 17 Mar 2022 04:03:23 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:15:01 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:66fb1aabb4c03c1a8502c7ab4d442a4602f465cee7eccf27eb706178ce2859a6`  
		Last Modified: Thu, 17 Mar 2022 04:08:59 GMT  
		Size: 55.8 MB (55754297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edd9cb2b95dbf7f48618c8e86c46c24ebbd1e88faa80bb6299f17474bdd2b3d`  
		Last Modified: Fri, 18 Mar 2022 08:18:22 GMT  
		Size: 11.4 MB (11367941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7fb7a823070655e625d406d231cc6a2f192054cc327c4730783974f7e9c0a4`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7330b95115cc239fdebf118defcb0e3cf76bcabf611950715ce2cf8cbd7acd81`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89deb3ade5987120d2bba15db10e8be7a48a9fa3517fb6395fc5952e4bad04a2`  
		Last Modified: Fri, 18 Mar 2022 08:18:21 GMT  
		Size: 307.5 KB (307473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be8b0b9c55260fa6b3d724c6f7075078c1f4b90a2fb916071bed9314952e804`  
		Last Modified: Fri, 18 Mar 2022 08:18:31 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd16.04`

```console
$ docker pull neurodebian@sha256:4f8f3b02888f61824d206a937db34a20819de9cf11a2a0161dcfa463c4cba1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd16.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:d80e83bfcc000dd04b02c778a1297c7ad2540cb555ab96c90ec154c6a4f0f495
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46729666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60902017c278b0db41b17f8f1de27469127d1ea4898b2469f52647585af6120`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 03:57:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Mar 2022 17:27:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Mar 2022 17:27:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Mar 2022 17:27:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84732b274efc4bdfc5e30a12f05cbd1a9936e3ed5e8952879d6ee935df35eb79`  
		Last Modified: Tue, 31 Aug 2021 04:00:24 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3505bfdde8eb1415423d95064ff6b92c835526022feb1d95009ab5ec04c115`  
		Last Modified: Wed, 16 Mar 2022 17:35:34 GMT  
		Size: 3.2 KB (3155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f3fae1c80c2541f9a1f6a2df3ea6faa8f5c9797dda86103383518675981d44`  
		Last Modified: Wed, 16 Mar 2022 17:35:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a78747ad8c43a648a10d04a1c586defca6040cc6c5a4acf404d3962d361631a`  
		Last Modified: Wed, 16 Mar 2022 17:35:35 GMT  
		Size: 227.0 KB (226984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd16.04-non-free`

```console
$ docker pull neurodebian@sha256:79afd2bee6d4c71c226efc18ed02df20d4b960303d3726749e5316d6e833137b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd16.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2614aec9e563f0b111961f993de935a0fbb9620cdb11473ac31ec813dac0323e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46729923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4763f90a405bf63daed0435933c43c39b39f71793a896d5ed656d45e8fb9242`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 03:57:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Mar 2022 17:27:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Mar 2022 17:27:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Mar 2022 17:27:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Mar 2022 17:27:29 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84732b274efc4bdfc5e30a12f05cbd1a9936e3ed5e8952879d6ee935df35eb79`  
		Last Modified: Tue, 31 Aug 2021 04:00:24 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3505bfdde8eb1415423d95064ff6b92c835526022feb1d95009ab5ec04c115`  
		Last Modified: Wed, 16 Mar 2022 17:35:34 GMT  
		Size: 3.2 KB (3155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f3fae1c80c2541f9a1f6a2df3ea6faa8f5c9797dda86103383518675981d44`  
		Last Modified: Wed, 16 Mar 2022 17:35:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a78747ad8c43a648a10d04a1c586defca6040cc6c5a4acf404d3962d361631a`  
		Last Modified: Wed, 16 Mar 2022 17:35:35 GMT  
		Size: 227.0 KB (226984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374df1832948bd22b70477d80f3e38c6fb69de53d87a19787be363131e99a16f`  
		Last Modified: Wed, 16 Mar 2022 17:35:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04`

```console
$ docker pull neurodebian@sha256:555b2b08bcc094b7afaaf84ea8f9f3de19fdb00e5b7b74fd5cf3c043c02f751d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd18.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:1645e3310909d3d6c6dde18620034c1e16bdfca4885f0894fc6f5aa345510ff7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31765044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a36c0147ecfedd99a00877d541298700840da0442491b2969da977ad015403`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:10:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:11:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:11:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:11:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13c025ea06346b83ad7c49fa15da8d4003fa73e23df204b6615c244e8664759`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 4.8 MB (4813174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24aca53dc4332fc343fe1b8f11288687747e5786de455f96b33b6a2334850c2`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 3.2 KB (3157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683e3441e3e903fbe30910de4ebe852baf583864320da739381072d9dd6b1611`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6c2c9ecc51b2cff0024e1d1c3b3067892739d7f423e5eb2dedd1e03ed3d93`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 239.8 KB (239834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04-non-free`

```console
$ docker pull neurodebian@sha256:e91546d2c3afd4b1f57e9e44a564fbcd005a454b254b732490e8f3538a2d2a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd18.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:945ccae98ba2d0695cf90a01077ff27e2d7a0a0a59ce3c97ae4c7fb3861be2ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31765300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb1855f361d51ed1c9c6c2bc86b5438783484993d1a7392435053c6a48bb19a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:10:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:11:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:11:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:11:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:11:46 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13c025ea06346b83ad7c49fa15da8d4003fa73e23df204b6615c244e8664759`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 4.8 MB (4813174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24aca53dc4332fc343fe1b8f11288687747e5786de455f96b33b6a2334850c2`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 3.2 KB (3157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683e3441e3e903fbe30910de4ebe852baf583864320da739381072d9dd6b1611`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6c2c9ecc51b2cff0024e1d1c3b3067892739d7f423e5eb2dedd1e03ed3d93`  
		Last Modified: Fri, 18 Mar 2022 08:16:13 GMT  
		Size: 239.8 KB (239834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978320cc501a425c41115d59e2a6244b6544c46fde53245a986adfbe51826bba`  
		Last Modified: Fri, 18 Mar 2022 08:16:23 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:4edb28dcbd20d4d4edfedc8c1c78de5933e918c2cd537025fa8e7795216226a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:fcc9975228aa54c9b819de450a91c96d06a3723e3a6e7b653cb568dd2393fe7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34294517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aeaa060e12baeb84bf1b41aa26cdbf4c2c53d3726e69e0ed086522a7175f6a4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:12:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:12:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:12:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:12:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181b23a20725abd31982685ba6ef94f9c18f9b4715d5413a59cf785746d88b23`  
		Last Modified: Fri, 18 Mar 2022 08:16:33 GMT  
		Size: 5.5 MB (5488532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc0a34dbeb5ca294abf88cbffaceed4bcb3a84170048e12e84e38d9c8675d22`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09414e5157753ac2e1ab73492fccc7b48fb65f1937bbfe26e3e959a1fae9e0e`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87dcb7d6ca3e3b5c1f15c6c7bf23a38ad1e13b919a24a1b6169b625a3a7ee9a`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 238.1 KB (238061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:7afa91a1b2a0b7d718b7fcd1931847e6856f29d0b8c14698ba696f60881ebdfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d1f00395c2f2448b4e7f04ec19a232ad71985b77dc66d616d5455c169bd86fbe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34294775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7c25d0ce101c6a6aa21cd974d08e34855d820cf6e50c4e28c7b033ea5539a5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:12:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:12:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:12:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:12:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:12:58 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181b23a20725abd31982685ba6ef94f9c18f9b4715d5413a59cf785746d88b23`  
		Last Modified: Fri, 18 Mar 2022 08:16:33 GMT  
		Size: 5.5 MB (5488532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc0a34dbeb5ca294abf88cbffaceed4bcb3a84170048e12e84e38d9c8675d22`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09414e5157753ac2e1ab73492fccc7b48fb65f1937bbfe26e3e959a1fae9e0e`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87dcb7d6ca3e3b5c1f15c6c7bf23a38ad1e13b919a24a1b6169b625a3a7ee9a`  
		Last Modified: Fri, 18 Mar 2022 08:16:32 GMT  
		Size: 238.1 KB (238061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f18a59ac046a70833ff45efdfd55fdb47431829ea19991eaf19f806b0f08bfc`  
		Last Modified: Fri, 18 Mar 2022 08:16:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd21.10`

```console
$ docker pull neurodebian@sha256:7d57bb08153ba7f05a7822ae8947842e4584304f538848c4377b10cbe09fb69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd21.10` - linux; amd64

```console
$ docker pull neurodebian@sha256:3af8a75a0545139db54dc00aba8a4845416e87f8cb884b6a64300c518f6ddead
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34389098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f0ca849eadea70a74806f43758c3e847c8bc58853b69057d0223e2a90dafbf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:54 GMT
ADD file:dc66b6b0841e395b5cf9d65976a75c3a46a19eb2c0fda4556ac6b4c5b0fe4dea in / 
# Fri, 18 Mar 2022 05:30:55 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:13:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:13:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:13:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian impish main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel impish main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:13:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:49dc71d53e6dff9c7147b85fbe167470cff447114548e6df43606b75526c1451`  
		Last Modified: Fri, 18 Mar 2022 05:32:45 GMT  
		Size: 30.4 MB (30385910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02dcdc2dc3c600bc75fef3a31d1a5e174b094ca75baf90ba6d19587937596f`  
		Last Modified: Fri, 18 Mar 2022 08:16:52 GMT  
		Size: 3.8 MB (3751774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5a2abb4afa38d503f13785e4ddec9cf8c7dfecbc32a1044e17d914465c297`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c82d2f42bf7700d6f3b7a7d0a2cb65df389e99fc8590f8ea57f38faa9953606`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd139379a494abeceaea7b99b395b2dfa5d3171218e66e5b2a861bead4ef1e26`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 249.4 KB (249399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd21.10-non-free`

```console
$ docker pull neurodebian@sha256:3d2e187fe6b51ab8920ae14f64a641b9f9e0c63773b5bdda1c767c7ca9a1d7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd21.10-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:95d4f32310f9a745ed1872824b5291c47bf8eb3cd79406514131e23090c75e1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34389358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157f768d72636f7b777a6e298a6eb924161750b6ddc10ef17b8bb027d2c7e14e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:54 GMT
ADD file:dc66b6b0841e395b5cf9d65976a75c3a46a19eb2c0fda4556ac6b4c5b0fe4dea in / 
# Fri, 18 Mar 2022 05:30:55 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:13:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:13:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:13:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian impish main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel impish main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:13:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:13:41 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:49dc71d53e6dff9c7147b85fbe167470cff447114548e6df43606b75526c1451`  
		Last Modified: Fri, 18 Mar 2022 05:32:45 GMT  
		Size: 30.4 MB (30385910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02dcdc2dc3c600bc75fef3a31d1a5e174b094ca75baf90ba6d19587937596f`  
		Last Modified: Fri, 18 Mar 2022 08:16:52 GMT  
		Size: 3.8 MB (3751774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5a2abb4afa38d503f13785e4ddec9cf8c7dfecbc32a1044e17d914465c297`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c82d2f42bf7700d6f3b7a7d0a2cb65df389e99fc8590f8ea57f38faa9953606`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd139379a494abeceaea7b99b395b2dfa5d3171218e66e5b2a861bead4ef1e26`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 249.4 KB (249399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e4a25da4e998243c62595ed39cb7923223ddc183fb90108283b18a76655a42`  
		Last Modified: Fri, 18 Mar 2022 08:17:01 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd90`

```console
$ docker pull neurodebian@sha256:c639f10e3961d5ef134d710e51572558571eb7cfcb5af5b03f287ae658642b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd90` - linux; amd64

```console
$ docker pull neurodebian@sha256:885c22209eea6f2b258985759202f0942afa8bfaa00c3f37a05fba0e932933fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52296079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a433eb47ba6a3467e2914103e8f537b34f50601420a90cea549de94ba55fdc45`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:37 GMT
ADD file:0d1703dd365e8d6f8625b40addc388cab8f0423af2bca03b0baea5d27f585a9c in / 
# Thu, 17 Mar 2022 04:06:37 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:13:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:13:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:13:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:13:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d172ccdc78ea7d453ae5fa3feafee94e3837e6f8e282d8501e668329c49551ed`  
		Last Modified: Thu, 17 Mar 2022 04:13:38 GMT  
		Size: 45.4 MB (45427778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be042bfa7a0b55e2682cd3788568190ac9be01e50fa1b6cf821dc4e6a947c75d`  
		Last Modified: Fri, 18 Mar 2022 08:17:11 GMT  
		Size: 6.6 MB (6572658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c261c726a69dfb82b29305d696a5f9f9f2e8eb82a894e5219b96687d1227a6`  
		Last Modified: Fri, 18 Mar 2022 08:17:10 GMT  
		Size: 3.2 KB (3159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b6863580e6fd41b0211773626ac34742647f168e91152dda28aa3fcfdce666`  
		Last Modified: Fri, 18 Mar 2022 08:17:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76abd5f1f23cc1325465778afc3d7cb8517fad26d4eda5715c3a9fdb2df4d1d8`  
		Last Modified: Fri, 18 Mar 2022 08:17:11 GMT  
		Size: 292.2 KB (292240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd90-non-free`

```console
$ docker pull neurodebian@sha256:b519907c1c159c34e0e8019a6b75aa1194a0eecbe5916794d7dd3e9383d5275f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd90-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:565b9ea4f0645a44b0738ff3956adb05e176ab38a137fd49a8811f441b16b186
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52296443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77669f19123e9ed2f887485717b627f8182eaff8551b84ff614303db87becdc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:37 GMT
ADD file:0d1703dd365e8d6f8625b40addc388cab8f0423af2bca03b0baea5d27f585a9c in / 
# Thu, 17 Mar 2022 04:06:37 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:13:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:13:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:13:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:13:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:00 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:d172ccdc78ea7d453ae5fa3feafee94e3837e6f8e282d8501e668329c49551ed`  
		Last Modified: Thu, 17 Mar 2022 04:13:38 GMT  
		Size: 45.4 MB (45427778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be042bfa7a0b55e2682cd3788568190ac9be01e50fa1b6cf821dc4e6a947c75d`  
		Last Modified: Fri, 18 Mar 2022 08:17:11 GMT  
		Size: 6.6 MB (6572658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c261c726a69dfb82b29305d696a5f9f9f2e8eb82a894e5219b96687d1227a6`  
		Last Modified: Fri, 18 Mar 2022 08:17:10 GMT  
		Size: 3.2 KB (3159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b6863580e6fd41b0211773626ac34742647f168e91152dda28aa3fcfdce666`  
		Last Modified: Fri, 18 Mar 2022 08:17:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76abd5f1f23cc1325465778afc3d7cb8517fad26d4eda5715c3a9fdb2df4d1d8`  
		Last Modified: Fri, 18 Mar 2022 08:17:11 GMT  
		Size: 292.2 KB (292240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719897ab8fcba86f33284aac6712bae782b28ace5211fa00f84ddc03d6f3f4fa`  
		Last Modified: Fri, 18 Mar 2022 08:17:27 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:d74aac0a9a2b499a43320fbe77c4903f16eb51e5d4cc11157befa779b7bccb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:df5228a7cc9869e9dd2cc21f322d93c3c8aa40704ec8440f6c405f7fc96d0396
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66546132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f211e5eb1c6485556c22e86cd196252ac3b85d5ab096431ce311386099e4b4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:14:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:14:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:14:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:41 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4228642e82a30a73f7cbd7f0c7392aa1ac2cddf752825f306aed5b081edd3566`  
		Last Modified: Fri, 18 Mar 2022 08:17:58 GMT  
		Size: 11.3 MB (11309638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2beeba079089ff348059b8341a20ef560d1314eb37238be288f1f368d62a9550`  
		Last Modified: Fri, 18 Mar 2022 08:17:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2635a2803078eea28ecbb9fee59ca31830242961f360a1bc71b1cfa2ab21492c`  
		Last Modified: Fri, 18 Mar 2022 08:17:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b234e87955266b3dcd5b20731e0134b3084225781a695fd865e490fda0dc4db`  
		Last Modified: Fri, 18 Mar 2022 08:17:57 GMT  
		Size: 311.3 KB (311282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c8fe6f006217cfab491cd75a0eb55ea7d173a5b5d2cf62499f9ce9d22897c4`  
		Last Modified: Fri, 18 Mar 2022 08:18:09 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:ccea1662fe9f22ebeb8004edabf1bcfcd02c260b3a365f3bb4117fe1d836c849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:297460e2945c00d57e88ddf9d1c6db065ed8f24ebdf8cd614708c320464255d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67668467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df9c2bc96bce88be296b8467626e67880626f7769cccc6db72524fa0fb439ca`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:05:54 GMT
ADD file:20b1068c276c223839818edd0aca3981a1b8139130064d19f9ec38e26a94ff27 in / 
# Thu, 17 Mar 2022 04:05:54 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:15:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:15:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:15:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:15:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab40a96ab944197ee11d696f776db9c1130db9825e9996a5e8939611fcf5e470`  
		Last Modified: Thu, 17 Mar 2022 04:12:27 GMT  
		Size: 56.0 MB (55984715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9128aac36dac7e03aa34a5c0e125dfcec841942698bf8aef01012ee2f596a8d8`  
		Last Modified: Fri, 18 Mar 2022 08:18:41 GMT  
		Size: 11.4 MB (11374011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a999bb7dcc545cc51773d4c7aab4a9bc7f387800fe7ff8f40d0aee6f60935a94`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a2eaf0fa50faf1fc453bdf807f0e1a9494babfceea5a2e064bb97c9388c1d6`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abe8889081ee40a2d3cf24eb140b00e5f18e6b538f091c567f4aabc0120f07e`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 307.7 KB (307730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:bc0c39aae86597def0f27272b2af65ebfb2a3ff877f39260caa95adc57f75727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:883c47ac6a8575a1c24758747419c7dfc9bfa63d851681293b8bf1aeae1e0b97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67668783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf847e6fb8d6afdf487f58c8abd7bc69ca58a9f16dd4f10643c9da5332728bdf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:05:54 GMT
ADD file:20b1068c276c223839818edd0aca3981a1b8139130064d19f9ec38e26a94ff27 in / 
# Thu, 17 Mar 2022 04:05:54 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:15:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:15:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:15:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:15:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:15:20 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:ab40a96ab944197ee11d696f776db9c1130db9825e9996a5e8939611fcf5e470`  
		Last Modified: Thu, 17 Mar 2022 04:12:27 GMT  
		Size: 56.0 MB (55984715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9128aac36dac7e03aa34a5c0e125dfcec841942698bf8aef01012ee2f596a8d8`  
		Last Modified: Fri, 18 Mar 2022 08:18:41 GMT  
		Size: 11.4 MB (11374011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a999bb7dcc545cc51773d4c7aab4a9bc7f387800fe7ff8f40d0aee6f60935a94`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a2eaf0fa50faf1fc453bdf807f0e1a9494babfceea5a2e064bb97c9388c1d6`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abe8889081ee40a2d3cf24eb140b00e5f18e6b538f091c567f4aabc0120f07e`  
		Last Modified: Fri, 18 Mar 2022 08:18:40 GMT  
		Size: 307.7 KB (307730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ebcdd130a728f8e1585d398f32840253f3e7aa5b9beba3b1023d239433e0e0`  
		Last Modified: Fri, 18 Mar 2022 08:18:50 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:stretch`

```console
$ docker pull neurodebian@sha256:c639f10e3961d5ef134d710e51572558571eb7cfcb5af5b03f287ae658642b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:stretch` - linux; amd64

```console
$ docker pull neurodebian@sha256:885c22209eea6f2b258985759202f0942afa8bfaa00c3f37a05fba0e932933fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52296079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a433eb47ba6a3467e2914103e8f537b34f50601420a90cea549de94ba55fdc45`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:37 GMT
ADD file:0d1703dd365e8d6f8625b40addc388cab8f0423af2bca03b0baea5d27f585a9c in / 
# Thu, 17 Mar 2022 04:06:37 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:13:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:13:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:13:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:13:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d172ccdc78ea7d453ae5fa3feafee94e3837e6f8e282d8501e668329c49551ed`  
		Last Modified: Thu, 17 Mar 2022 04:13:38 GMT  
		Size: 45.4 MB (45427778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be042bfa7a0b55e2682cd3788568190ac9be01e50fa1b6cf821dc4e6a947c75d`  
		Last Modified: Fri, 18 Mar 2022 08:17:11 GMT  
		Size: 6.6 MB (6572658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c261c726a69dfb82b29305d696a5f9f9f2e8eb82a894e5219b96687d1227a6`  
		Last Modified: Fri, 18 Mar 2022 08:17:10 GMT  
		Size: 3.2 KB (3159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b6863580e6fd41b0211773626ac34742647f168e91152dda28aa3fcfdce666`  
		Last Modified: Fri, 18 Mar 2022 08:17:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76abd5f1f23cc1325465778afc3d7cb8517fad26d4eda5715c3a9fdb2df4d1d8`  
		Last Modified: Fri, 18 Mar 2022 08:17:11 GMT  
		Size: 292.2 KB (292240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:b519907c1c159c34e0e8019a6b75aa1194a0eecbe5916794d7dd3e9383d5275f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:565b9ea4f0645a44b0738ff3956adb05e176ab38a137fd49a8811f441b16b186
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52296443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77669f19123e9ed2f887485717b627f8182eaff8551b84ff614303db87becdc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:37 GMT
ADD file:0d1703dd365e8d6f8625b40addc388cab8f0423af2bca03b0baea5d27f585a9c in / 
# Thu, 17 Mar 2022 04:06:37 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:13:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:13:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:13:54 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:13:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:14:00 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:d172ccdc78ea7d453ae5fa3feafee94e3837e6f8e282d8501e668329c49551ed`  
		Last Modified: Thu, 17 Mar 2022 04:13:38 GMT  
		Size: 45.4 MB (45427778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be042bfa7a0b55e2682cd3788568190ac9be01e50fa1b6cf821dc4e6a947c75d`  
		Last Modified: Fri, 18 Mar 2022 08:17:11 GMT  
		Size: 6.6 MB (6572658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c261c726a69dfb82b29305d696a5f9f9f2e8eb82a894e5219b96687d1227a6`  
		Last Modified: Fri, 18 Mar 2022 08:17:10 GMT  
		Size: 3.2 KB (3159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b6863580e6fd41b0211773626ac34742647f168e91152dda28aa3fcfdce666`  
		Last Modified: Fri, 18 Mar 2022 08:17:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76abd5f1f23cc1325465778afc3d7cb8517fad26d4eda5715c3a9fdb2df4d1d8`  
		Last Modified: Fri, 18 Mar 2022 08:17:11 GMT  
		Size: 292.2 KB (292240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719897ab8fcba86f33284aac6712bae782b28ace5211fa00f84ddc03d6f3f4fa`  
		Last Modified: Fri, 18 Mar 2022 08:17:27 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:xenial`

```console
$ docker pull neurodebian@sha256:4f8f3b02888f61824d206a937db34a20819de9cf11a2a0161dcfa463c4cba1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:xenial` - linux; amd64

```console
$ docker pull neurodebian@sha256:d80e83bfcc000dd04b02c778a1297c7ad2540cb555ab96c90ec154c6a4f0f495
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46729666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60902017c278b0db41b17f8f1de27469127d1ea4898b2469f52647585af6120`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 03:57:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Mar 2022 17:27:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Mar 2022 17:27:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Mar 2022 17:27:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84732b274efc4bdfc5e30a12f05cbd1a9936e3ed5e8952879d6ee935df35eb79`  
		Last Modified: Tue, 31 Aug 2021 04:00:24 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3505bfdde8eb1415423d95064ff6b92c835526022feb1d95009ab5ec04c115`  
		Last Modified: Wed, 16 Mar 2022 17:35:34 GMT  
		Size: 3.2 KB (3155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f3fae1c80c2541f9a1f6a2df3ea6faa8f5c9797dda86103383518675981d44`  
		Last Modified: Wed, 16 Mar 2022 17:35:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a78747ad8c43a648a10d04a1c586defca6040cc6c5a4acf404d3962d361631a`  
		Last Modified: Wed, 16 Mar 2022 17:35:35 GMT  
		Size: 227.0 KB (226984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:xenial-non-free`

```console
$ docker pull neurodebian@sha256:79afd2bee6d4c71c226efc18ed02df20d4b960303d3726749e5316d6e833137b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:xenial-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2614aec9e563f0b111961f993de935a0fbb9620cdb11473ac31ec813dac0323e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46729923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4763f90a405bf63daed0435933c43c39b39f71793a896d5ed656d45e8fb9242`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 03:57:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Mar 2022 17:27:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Mar 2022 17:27:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Mar 2022 17:27:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Mar 2022 17:27:29 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84732b274efc4bdfc5e30a12f05cbd1a9936e3ed5e8952879d6ee935df35eb79`  
		Last Modified: Tue, 31 Aug 2021 04:00:24 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3505bfdde8eb1415423d95064ff6b92c835526022feb1d95009ab5ec04c115`  
		Last Modified: Wed, 16 Mar 2022 17:35:34 GMT  
		Size: 3.2 KB (3155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f3fae1c80c2541f9a1f6a2df3ea6faa8f5c9797dda86103383518675981d44`  
		Last Modified: Wed, 16 Mar 2022 17:35:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a78747ad8c43a648a10d04a1c586defca6040cc6c5a4acf404d3962d361631a`  
		Last Modified: Wed, 16 Mar 2022 17:35:35 GMT  
		Size: 227.0 KB (226984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374df1832948bd22b70477d80f3e38c6fb69de53d87a19787be363131e99a16f`  
		Last Modified: Wed, 16 Mar 2022 17:35:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
